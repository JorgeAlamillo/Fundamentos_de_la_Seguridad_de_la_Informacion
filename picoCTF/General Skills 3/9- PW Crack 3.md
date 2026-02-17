### PW Crack 3

### Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
### Solución

### Solucion 1 - Usando Consola

```
$ wget -q https://artifacts.picoctf.net/c/16/level3.py
JorgeAlamillo-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/16/level3.flag.txt.enc
JorgeAlamillo-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/16/level3.hash.bin
JorgeAlamillo-picoctf@webshell:~$ nano level3.py

"Modificamos la funcion level_3_pw_check para poner un ciclo for y que ejecute todas hasta que nos de la correcta"

def level_3_pw_check():
    pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]
   #user_pw = input("Please enter correct password for flag: ")
    for user_pw in pos_pw_list:
        user_pw_hash = hash_pw(user_pw)
        if( user_pw_hash == correct_pw_hash ):
            print(f"Correct Password: {user_pw}")
            decryption = str_xor(flag_enc.decode(), user_pw)
            print(decryption)
            return
            

python level3.py
Correct Password: 865e
picoCTF{m45h_fl1ng1ng_2b072a90}

```

