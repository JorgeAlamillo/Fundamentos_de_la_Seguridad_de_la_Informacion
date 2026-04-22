### Mind your Ps and Qs

### Descripción

In RSA, a small e value can be problematic, but what about N? Can you decrypt this?[values](https://challenge-files.picoctf.net/c_wily_courier/2bbb4086ce95d3e431695877b72b7ea062756cb58e97fb4b5a9f3b61ae21ce28/values)
### Solución
┌──(JorgeMSI㉿MSI)-[~/picoCTF/Mind]
└─$ wget -q https://challenge-files.picoctf.net/c_wily_courier/2bbb4086ce95d3e431695877b72b7ea062756cb58e97fb4b5a9f3b61ae21ce28/values

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Mind]
└─$ nano exploti_rsa.py
```
import re
import os
import urllib.request
import json
import sys

print("[*] Leyendo el archivo 'values'...")
if not os.path.exists('values'):
    print("[-] Error: No se encontró el archivo 'values' en este directorio.")
    sys.exit()

with open('values', 'r') as f:
    content = f.read()

try:
    N = int(re.search(r'(?:N|n):\s*(\d+)', content).group(1))
    e = int(re.search(r'(?:e|E):\s*(\d+)', content).group(1))
    c = int(re.search(r'(?:c|ciphertext):\s*(\d+)', content, re.IGNORECASE).group(1))
except AttributeError:
    print("[-] Error: Formato de archivo irreconocible.")
    sys.exit()

print(f"[+] Valores extraídos. N tiene {N.bit_length()} bits (¡muy pequeño!).")

print("[*] Consultando FactorDB para hackear N y sacar p y q...")
url = f"http://factordb.com/api?query={N}"
try:
    req = urllib.request.urlopen(url)
    res = json.loads(req.read().decode())
    
    factors = res.get("factors")
    if not factors or res.get("status") not in ["FF", "CF"]:
        print("[-] FactorDB no tiene la respuesta. Tocaría usar una herramienta local como YAFU.")
        sys.exit()
        
    flat_factors = []
    for fact, exp in factors:
        for _ in range(exp):
            flat_factors.append(int(fact))
            
    if len(flat_factors) == 2:
        p, q = flat_factors
        print(f"[+] ¡N factorizado con éxito!\n    p = {p}\n    q = {q}")
    else:
        print("[-] FactorDB no devolvió 2 factores primos.")
        sys.exit()
except Exception as ex:
    print(f"[-] Error al consultar FactorDB: {ex}")
    sys.exit()

print("[*] Reconstruyendo la llave privada secreta (d)...")
phi = (p - 1) * (q - 1)

d = pow(e, -1, phi)

print("[*] Desencriptando el texto cifrado...")
m = pow(c, d, N)

byte_length = (m.bit_length() + 7) // 8
flag = m.to_bytes(byte_length, 'big')

print(f"\n[+] 🎉 Flag encontrada: {flag.decode('utf-8', errors='ignore')}")
```



┌──(JorgeMSI㉿MSI)-[~/picoCTF/Mind]
└─$ python3 exploti_rsa.py
[*] Leyendo el archivo 'values'...
[+] Valores extraídos. N tiene 269 bits (¡muy pequeño!).
[*] Consultando FactorDB para hackear N y sacar p y q...
[+] ¡N factorizado con éxito!
    p = 1891771437429478964908181306574287207137
    q = 501332739776173570344039681219489434626477
[*] Reconstruyendo la llave privada secreta (d)...
[*] Desencriptando el texto cifrado...

[+] 🎉 Flag encontrada:
}19ea7cd1_do0g_0n_N_11ams{FTCocip

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Mind]
└─$

}19ea7cd1_do0g_0n_N_11ams{FTCocip
picoCTF{sma11_N_n0_g0od_1dc7ae91}
### Notas
### Referencias