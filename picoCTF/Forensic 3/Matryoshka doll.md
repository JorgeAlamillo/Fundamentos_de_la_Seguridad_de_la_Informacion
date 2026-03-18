### Matryoshka doll

### Descripción

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?Image: [dolls.jpg](https://challenge-files.picoctf.net/c_wily_courier/0f5ef9c383aa83d319ccb01805f4b9499934bf6a44fdcb5a9f2039de92b6c24a/dolls.jpg)
### Solución
┌──(JorgeMSI㉿MSI)-[~/matri]
└─$ binwalk dolls.jpg                                                                                                --------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378933, uncompressed size: 383920, name: base_images/2_c.jpg
651591        0x9F147         End of Zip archive, footer length: 22


┌──(JorgeMSI㉿MSI)-[~/matri]
└─$ unzip dolls.jpg
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg

┌──(JorgeMSI㉿MSI)-[~/matri]
└─$ ls
base_images  dolls.jpg

┌──(JorgeMSI㉿MSI)-[~/matri]
└─$ binwalk base_images

┌──(JorgeMSI㉿MSI)-[~/matri]
└─$ unzip base_images
unzip:  cannot find or open base_images, base_images.zip or base_images.ZIP.

┌──(JorgeMSI㉿MSI)-[~/matri]
└─$ ls
base_images  dolls.jpg

┌──(JorgeMSI㉿MSI)-[~/matri]
└─$ unzip dolls.jpg
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
replace base_images/2_c.jpg? [y]es, [n]o, [A]ll, [N]one, [r]ename: ^[
error:  invalid response [┌──(JorgeMSI㉿MSI)-[~/matri]
└─$ base_images
base_images: command not found

┌──(JorgeMSI㉿MSI)-[~/matri]
└─$ cd base_images/

┌──(JorgeMSI㉿MSI)-[~/matri/base_images]
└─$ ls
2_c.jpg

┌──(JorgeMSI㉿MSI)-[~/matri/base_images]
└─$ binwalk 2_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196025, uncompressed size: 201427, name: base_images/3_c.jpg
383787        0x5DB2B         End of Zip archive, footer length: 22
383898        0x5DB9A         End of Zip archive, footer length: 22


┌──(JorgeMSI㉿MSI)-[~/matri/base_images]
└─$ unzip 2_c.jpg
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg

┌──(JorgeMSI㉿MSI)-[~/matri/base_images]
└─$ ls
2_c.jpg  base_images

┌──(JorgeMSI㉿MSI)-[~/matri/base_images]
└─$ cd base_images/

┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images]
└─$ ls
3_c.jpg

┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images]
└─$ binwalk 3_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77633, uncompressed size: 79786, name: base_images/4_c.jpg
201405        0x312BD         End of Zip archive, footer length: 22


┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images]
└─$ unzip 3_c.jpg
Archive:  3_c.jpg
warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/4_c.jpg

┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images]
└─$ ls
3_c.jpg  base_images

┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images]
└─$ cd base_images/

┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images/base_images]
└─$ ls
4_c.jpg

┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images/base_images]
└─$ binwalk 4_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v1.0 to extract, compressed size: 42, uncompressed size: 42, name: flag.txt
79764         0x13794         End of Zip archive, footer length: 22


┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images/base_images]
└─$ unzip 4_c.jpg
Archive:  4_c.jpg
warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
  (attempting to process anyway)
 extracting: flag.txt

┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images/base_images]
└─$ ls
4_c.jpg  flag.txt

┌──(JorgeMSI㉿MSI)-[~/matri/base_images/base_images/base_images]
└─$ cat flag.txt
picoCTF{LL9lb1dR4QbGe4l4iWCvGq9pdtwt7392}



### Notas
### Referencias