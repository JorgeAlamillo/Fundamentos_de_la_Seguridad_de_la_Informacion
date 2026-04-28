### rail-fence

### Descripción

A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it?Download the message [here](https://artifacts.picoctf.net/c/189/message.txt).Put the decoded message in the picoCTF flag format, `picoCTF{decoded_message}`.
### Solución

┌──(JorgeMSI㉿MSI)-[~/tarea4crypto]
└─$ mkdir ~/tarea4crypto/06
cd ~/tarea4crypto/06
wget https://artifacts.picoctf.net/c/189/message.txt
cat message.txt
--2026-04-27 08:39:53--  https://artifacts.picoctf.net/c/189/message.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.120, 13.225.222.125, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 56 [application/octet-stream]
Saving to: ‘message.txt’

message.txt                   100%[=================================================>]      56  --.-KB/s    in 0s

2026-04-27 08:39:54 (17.1 MB/s) - ‘message.txt’ saved [56/56]

Ta _7N6D8Dhlg:W3D_H3C31N__387ef sHR053F38N43DFD i33___N6

https://gchq.github.io/CyberChef/#recipe=Rail_Fence_Cipher_Decode(4,0)&input=VGEgXzdONkQ4RGhsZzpXM0RfSDNDMzFOX18zODdlZiBzSFIwNTNGMzhONDNERkQgaTMzX19fTjY

The flag is: picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7}
### Notas
### Referencias