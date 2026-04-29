### vault-door-3
### Descripción

This vault uses for-loops and byte arrays.The source code for this vault is here: [VaultDoor3.java](https://challenge-files.picoctf.net/c_fickle_tempest/5351a2aa13dcef1a4a661eccae345babfce30ae13eea5f3b35f4a4ae5cbb23da/VaultDoor3.java)
### Solución
┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing/03]
└─$ wget https://challenge-files.picoctf.net/c_fickle_tempest/5351a2aa13dcef1a4a661eccae345babfce30ae13eea5f3b35f4a4ae5cbb23da/VaultDoor3.java
--2026-04-29 10:33:54--  https://challenge-files.picoctf.net/c_fickle_tempest/5351a2aa13dcef1a4a661eccae345babfce30ae13eea5f3b35f4a4ae5cbb23da/VaultDoor3.java
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 18.238.132.26, 18.238.132.115, 18.238.132.88, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|18.238.132.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1473 (1.4K) [application/octet-stream]
Saving to: ‘VaultDoor3.java’

VaultDoor3.java               100%[=================================================>]   1.44K  --.-KB/s    in 0s

2026-04-29 10:33:55 (12.3 MB/s) - ‘VaultDoor3.java’ saved [1473/1473]


┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing/03]
└─$ cat VaultDoor3.java
import java.util.*;

class VaultDoor3 {
    public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
        String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
        if (vaultDoor.checkPassword(input)) {
            System.out.println("Access granted.");
        } else {
            System.out.println("Access denied!");
        }
    }

    // Our security monitoring team has noticed some intrusions on some of the
    // less secure doors. Dr. Evil has asked me specifically to build a stronger
    // vault door to protect his Doomsday plans. I just *know* this door will
    // keep all of those nosy agents out of our business. Mwa ha!
    //
    // -Minion #2671
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        return s.equals("jU5t_a_sna_3lpm18gb4c_u_4_m2r640");
    }
}
┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing/03]
└─$ nano solve.py

```
scrambled = "jU5t_a_sna_3lpm18gb4c_u_4_m2r640"
password = [None] * 32

for i in range(0, 8):
    password[i] = scrambled[i]

for i in range(8, 16):
    password[23-i] = scrambled[i]

for i in range(16, 32, 2):
    password[46-i] = scrambled[i]

for i in range(31, 16, -2):
    password[i] = scrambled[i]

print("picoCTF{" + "".join(password) + "}")
```


┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing/03]
└─$ python3 solve.py

picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_c2b680}

### Notas
### Referencias