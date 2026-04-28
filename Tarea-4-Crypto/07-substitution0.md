### substitution0
### Descripción

A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher?Download the message [here](https://artifacts.picoctf.net/c/153/message.txt).
### Solución

┌──(JorgeMSI㉿MSI)-[~/tarea4crypto/07]
└─$ python3 -c "
import sys
abc = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
key = 'OHNFUMWSVZLXEGCPTAJDYIRKQB'

with open('message.txt', 'r') as f:
    text = f.read()

trans = str.maketrans(key + key.lower(), abc + abc.lower())
print(text.translate(trans))
"
ABCDEFGHIJKLMNOPQRSTUVWXYZ

Hereupon Legrand arose, with a grave and stately air, and brought me the beetle
from a glass case in which it was enclosed. It was a beautiful scarabaeus, and, at
that time, unknown to naturalists—of course a great prize in a scientific point
of view. There were two round black spots near one extremity of the back, and a
long one near the other. The scales were exceedingly hard and glossy, with all the
appearance of burnished gold. The weight of the insect was very remarkable, and,
taking all things into consideration, I could hardly blame Jupiter for his opinion
respecting it.

The flag is: 
picoCTF{5UB5717U710N_3V0LU710N_03055505}
### Notas
### Referencias
