# secarmy-CTF-2.0
Writeups of secarmy CTF 2.0
my team : Krypton

### welcome 

#### 1) Welcome All
  ###### flag : secarmy{w3lc0me_y0u_all}

![Welcome All](https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/welcome.png)

#### 2) Netcat 
  ###### flag : secarmy{W3lc0m3_T0_S3c4RmyC7F0x02}
  
  ![netcat](https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/welcome%20nc.png)
  
 #### 3) InstaFamous
  ###### flag : secarmy{w3lc0me_1n$t@_f@m1ly}
  
  ![instafamous](https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/Welcomeinstafamous.jpg)

### starters

#### 1) "16+8"
  ###### flag : secarmy{Num3er_sys73m}
  we have given two files with numbers in it 
  1 )  73 65 63 61 72 6d 79 7b 
 
  2 )  116 165 155 63 145 162 137 163 171 163 67 63 155 175 
  
  as the name suggests the first part was hex and the second was octal so doing a simple conversion we got the flag 
  
#### 2) Die basis 
  ###### flag : secarmy{fl@g_1s__th3_b@s3}
  two files given 
  1) \*\*\*\*\*\*\**c2VjYXJteXtmbEBnXzFzXw==\*\*\*\*\*\*\*
  2) \*\*\*\*\*\*\*\*\*\*L52GQM27MJAHGM35\*\*\*\*\*\*\*\*\*
  
  the first one was base64 and the second one was base32 encoded
  
#### 3) Easy capture
  ###### flag : secarmy{h3r3_y0u_c@ptur3}
  one's and zeroes to be converted to text 
  
  01110011 01100101 01100011 01100001 01110010 01101101 01111001 01111011 01101000 
  00110011 01110010 00110011 01011111 01111001 00110000 01110101 01011111 01100011 
  01000000 01110000 01110100 01110101 01110010 00110011 01111101
  
#### 4) Image
  ###### flag : secarmy{th3_im@ge_s4ys_i7_a11}
  
  doing a simple zsteg revealed the flag
  
 ![here's the image](https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/Starters%20Image.png)
 
 
#### 5) Th3 G1f7
  ###### flag : secarmy{h3re_1s_th3_g1ft}
  
  same thing again the flag was revealed by a zsteg
  
  ![the gift](https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/Starters%20the%20gift.png)
  
### forensics

#### its all in your head
  ###### flag : secarmy{h3ad3rs_t3ll_a_l0t}
  
  a corrupted png file was given
  https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/forensics%20head%20orig.png
  
  so i tried hexdump but the magic bytes were different from png so i changed them with hexedit which revealed the flag.
  ![flag](https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/forensics%20head%20flag.png)
  
#### secret
  ###### flag : secarmy{ain’t_visible?}
  
  a pdf with a username and a password hidden by asterisks
  after using pdftotext tool the flag was found
  
  https://github.com/madhusudanbabar/secarmy-CTF-2.0/raw/master/Secret.pdf
  
#### the confusion
  ###### flag : secarmy{WA3_I7_s0_c0nfu3ing}
  
  flag was split and hidden in two images
  the first part was ROT13 and second was ROT47
  
#### the bin
  ###### flag : secarmy{PAST3_B1N_H@S_S0LUT10N}
  
  
  here you  have the flag :- 61 48 52 30 63 48 4d 36 4c 79 39 77 59 58 4e 30 5a 57 4a 70 62 69 35 6a 62 32 30 76 54 45 30 35 63 57 56 33 64 57 6b 3d|61 48 52 30 63 48 4d 36 4c 79 39 77 59 58 4e 30 5a 57 4a 70 62 69 35 6a 62 32 30 76 57 6d 52 71 54 6a 6
  
  hex to text conversion gave two links of pastebin out of which the second one was working flag 
  
#### Save them 
  ##### flag : secarmy{PAST3_B1N_H@S_S0LUT10N}
  
  
### Binary/Reversing 
#### Stringy
  ##### flag : secarmy{l00k_a7_th3_str1ng5!!}
  
  as the name suggests i did strings on the elf which gave me some weird strings 
  c2VjYXJtH
eXtsMDBrH
X2E3X3RoH
M19zdHIxH
bmc1ISF9H

i tried base64 but it didnt worked then i removed the H at the end and it gave me flag
  https://github.com/madhusudanbabar/secarmy-CTF-2.0/raw/master/stringy
  
#### Smash it
  ##### flag : secarmy{sm@sh1ng_st@ck_1s_t00_much_fun}
  here's the binary : https://github.com/madhusudanbabar/secarmy-CTF-2.0/raw/master/smash
  
  ![flag ](https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/binary%20smashit.png)
  
#### F-L-A-S-H
  ##### flag : secarmy{7h1s_w45_345y_p34zy}
  here's the binary : https://github.com/madhusudanbabar/secarmy-CTF-2.0/raw/master/F-L-A-S-H
  ![flag](https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/binary%20flash%20flag.png)
  
#### backyard cow
  ##### flag : secarmy{d0_y0u_l1k3_c0w_languag3____?}
  
 here's the binary : https://github.com/madhusudanbabar/secarmy-CTF-2.0/raw/master/moo
 on reversing it with radare2 gave me a link to google drive file which has moo written everywhere, then i decoded it with **cow interpreter**
 
 ![flag](https://raw.githubusercontent.com/madhusudanbabar/secarmy-CTF-2.0/master/binary%20backyardcowflag.png)
 
 
### web 

#### prizes 
  ##### flag : secarmy{s0urc3_i5_n3ces5ary}
  
  
#### web_salad 
  ##### flag : secarmy{w3b_buck3t_3nc0un7er3d}
  
  
#### Cookie Bank 
  ##### flag : secarmy{the_$hy_c00kie_w1th1n}
  
  
#### silly mangolian 2.0 
  ##### flag : secarmy{why_1s_th1s_m0ng0li@n_$uch_@_f00l}
  


 
