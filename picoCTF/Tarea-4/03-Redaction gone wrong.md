### Redaction gone wrong
### Descripción

Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
### Solución

┌──(JorgeMSI㉿MSI)-[~/redaction]
└─$ sudo apt update && sudo apt install poppler-utils
Hit:1 http://http.kali.org/kali kali-last-snapshot InRelease
1025 packages can be upgraded. Run 'apt list --upgradable' to see them.
poppler-utils is already the newest version (25.03.0-11.1+b1).
The following package was automatically installed and is no longer required:
  libcrypt-dev
Use 'sudo apt autoremove' to remove it.

Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 1025

┌──(JorgeMSI㉿MSI)-[~/redaction]
└─$ wget -q https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf

┌──(JorgeMSI㉿MSI)-[~/redaction]
└─$ ls
Financial_Report_for_ABC_Labs.pdf

┌──(JorgeMSI㉿MSI)-[~/redaction]
└─$ pdftotext Financial_Report_for_ABC_Labs.pdf resultado.txt

┌──(JorgeMSI㉿MSI)-[~/redaction]
└─$ ls
Financial_Report_for_ABC_Labs.pdf  resultado.txt

┌──(JorgeMSI㉿MSI)-[~/redaction]
└─$ cat resultado.txt | grep "picoCTF"
picoCTF{C4n_Y0u_S33_m3_fully}

### Notas
### Referencias