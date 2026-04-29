### vault-door-4
### Descripción

This vault uses ASCII encoding for the password.The source code for this vault is here: [VaultDoor4.java](https://challenge-files.picoctf.net/c_fickle_tempest/f587295139ec9c3d23e1299b831596c3243b0e042bec63dd21168e996c0f7c8c/VaultDoor4.java)
### Solución

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing/04]
└─$ wget https://challenge-files.picoctf.net/c_fickle_tempest/f587295139ec9c3d23e1299b831596c3243b0e042bec63dd21168e996c0f7c8c/VaultDoor4.java
--2026-04-29 10:41:48--  https://challenge-files.picoctf.net/c_fickle_tempest/f587295139ec9c3d23e1299b831596c3243b0e042bec63dd21168e996c0f7c8c/VaultDoor4.java

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing/04]
└─$ cat VaultDoor4.java
import java.util.*;

class VaultDoor4 {
    public static void main(String args[]) {
        VaultDoor4 vaultDoor = new VaultDoor4();
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

    // I made myself dizzy converting all of these numbers into different bases,
    // so I just *know* that this vault will be impenetrable. This will make Dr.
    // Evil like me better than all of the other minions--especially Minion
    // #5620--I just know it!
    //
    //  .:::.   .:::.
    // :::::::.:::::::
    // :::::::::::::::
    // ':::::::::::::'
    //   ':::::::::'
    //     ':::::'
    //       ':'
    // -Minion #7781
    public boolean checkPassword(String password) {
        byte[] passBytes = password.getBytes();
        byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 067 , 065 ,
            '9' , '6' , '0' , '0' , 'a' , 'b' , 'c' , '3' ,
        };
        for (int i=0; i<32; i++) {
            if (passBytes[i] != myBytes[i]) {
                return false;
            }
        }
        return true;
    }
}
┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing/04]
└─$ nano solve.py
```
my_bytes = [
    106, 85, 53, 116, 95, 52, 95, 98,
    0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
    0o142, 0o131, 0o164, 0o63, 0o163, 0o137, 0o67, 0o65,
    ord('9'), ord('6'), ord('0'), ord('0'), ord('a'), ord('b'), ord('c'), ord('3')
]

print("picoCTF{" + "".join([chr(b) for b in my_bytes]) + "}")
```

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing/04]
└─$ python3 solve.py
picoCTF{jU5t_4_bUnCh_0f_bYt3s_759600abc3}
### Notas
### Referencias