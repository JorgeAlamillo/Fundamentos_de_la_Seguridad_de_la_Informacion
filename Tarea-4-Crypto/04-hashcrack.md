### hashcrack

### Descripción

A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?Access the server using `nc verbal-sleep.picoctf.net 61339`
### Solución

┌──(JorgeMSI㉿MSI)-[~/tarea4crypto/04]
└─$ nc verbal-sleep.picoctf.net 61339
Welcome!! Looking For the Secret?

We have identified a hash: 482c811da5d5b4bc6d497ffa98491e38
Enter the password for identified hash: password123
Correct! You've cracked the MD5 hash with no secret found!

Flag is yet to be revealed!! Crack this hash: b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3
Enter the password for the identified hash:
Incorrect. Goodbye.

┌──(JorgeMSI㉿MSI)-[~/tarea4crypto/04]
└─$ echo "b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3" > hash_sha1.txt

┌──(JorgeMSI㉿MSI)-[~/tarea4crypto/04]
└─$ john --format=Raw-SHA1 --wordlist=/usr/share/wordlists/rockyou.txt hash_sha1.txt
Using default input encoding: UTF-8
Loaded 1 password hash (Raw-SHA1 [SHA1 256/256 AVX2 8x])
Warning: no OpenMP support for this hash type, consider --fork=16
Press 'q' or Ctrl-C to abort, almost any other key for status
letmein          (?)
1g 0:00:00:00 DONE (2026-04-27 08:20) 50.00g/s 25600p/s 25600c/s 25600C/s stupid..letmein
Use the "--show --format=Raw-SHA1" options to display all of the cracked passwords reliably
Session completed.

┌──(JorgeMSI㉿MSI)-[~/tarea4crypto/04]
└─$ nc verbal-sleep.picoctf.net 61339
Welcome!! Looking For the Secret?

We have identified a hash: 482c811da5d5b4bc6d497ffa98491e38
Enter the password for identified hash: password123
Correct! You've cracked the MD5 hash with no secret found!

Flag is yet to be revealed!! Crack this hash: b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3
Enter the password for the identified hash: letmein
Correct! You've cracked the SHA-1 hash with no secret found!

Almost there!! Crack this hash: 916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745
Enter the password for the identified hash:
Incorrect. Goodbye.

┌──(JorgeMSI㉿MSI)-[~/tarea4crypto/04]
└─$ echo "916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745" > hash_sha256.txt

┌──(JorgeMSI㉿MSI)-[~/tarea4crypto/04]
└─$ john --format=Raw-SHA256 --wordlist=/usr/share/wordlists/rockyou.txt hash_sha256.txt
Using default input encoding: UTF-8
Loaded 1 password hash (Raw-SHA256 [SHA256 256/256 AVX2 8x])
Warning: poor OpenMP scalability for this hash type, consider --fork=16
Will run 16 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
qwerty098        (?)
1g 0:00:00:00 DONE (2026-04-27 08:21) 6.666g/s 5242Kp/s 5242Kc/s 5242KC/s chaddy12..sonirustiani
Use the "--show --format=Raw-SHA256" options to display all of the cracked passwords reliably
Session completed.

┌──(JorgeMSI㉿MSI)-[~/tarea4crypto/04]
└─$ nc verbal-sleep.picoctf.net 61339
Welcome!! Looking For the Secret?

We have identified a hash: 482c811da5d5b4bc6d497ffa98491e38
Enter the password for identified hash: password123
Correct! You've cracked the MD5 hash with no secret found!

Flag is yet to be revealed!! Crack this hash: b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3
Enter the password for the identified hash: letmein
Correct! You've cracked the SHA-1 hash with no secret found!

Almost there!! Crack this hash: 916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745
Enter the password for the identified hash: qwerty098
Correct! You've cracked the SHA-256 hash with a secret found.
The flag is: picoCTF{UseStr0nG_h@shEs_&PaSswDs!_5b836723}


### Notas
### Referencias