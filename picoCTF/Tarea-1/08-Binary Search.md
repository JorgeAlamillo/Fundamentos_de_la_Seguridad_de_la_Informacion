### Binary Search

### Descripción

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/18/challenge.zip)

`ssh -p 50321 ctf-player@atlas.picoctf.net`Using the password `84b12bae`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

Additional details will be available after launching your challenge instance.
### Solución

### Solucion 1 - Usando Consola

```
wget -q https://artifacts.picoctf.net/c_atlas/18/challenge.zip
JorgeAlamillo-picoctf@webshell:~$ unzip challenge.zip 
Archive:  challenge.zip
   creating: home/ctf-player/drop-in/
  inflating: home/ctf-player/drop-in/guessing_game.sh  
JorgeAlamillo-picoctf@webshell:~$ cd 
.local/ .ssh/   home/   
JorgeAlamillo-picoctf@webshell:~$ cd home/ctf-player/drop-in/

ssh -p 50321 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Higher! Try again.
Enter your guess: 850
Higher! Try again.
Enter your guess: 925
Lower! Try again.
Enter your guess: 888
Congratulations! You guessed the correct number: 888
Here's your flag: picoCTF{g00d_gu355_2e90d29b}
Connection to atlas.picoctf.net closed.
```

### Nota
- Se intento realizar algún script para solucionarlo, pero no me funciono. Entonces se realizo el juego hasta que nos dio la solución. 
