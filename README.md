# 202334546_Lab5

## ***\*\*I/O Redirection : Standard Output">"***
> -화면에 나오는 파일들을 저장하는



ls -lh > 저장하고자 하는 파일이름  
=화면에 있는 파일들을 txt로 저장  

cat 파일.txt  
=txt 파일 여는 코드  

ls -lh >> 저장한 파일 이름  
=기존에 파일을 덮어쓰지 않고 그 뒤에 새로운 내용 추가  

---

## **Standard Input **"<"**  

-can mix **"<"**, **">"** together in a single line.

sort < ~~.txt > sorted_words.txt

= sort하고 이름을 sorted_words로 바꿈

cat sorted_words.txt

---

| : pipeline 
= 앞서했던 커맨드의 출력을 다음 커맨드의 입력으로 가져간다.

command1 | command2 | command3
= command1의 아웃풋이 command2의 인풋으로

---

ls | wc -l = 파일의 갯수
echo * = ls랑 비슷 
echo print out text = echo ~~ 프린트

-- : 약식을 쓰지 않는

---

**\*\*\*권한 : Permissions**

***-Linux is a multi-user system.   
-Files and directories have a permission assigned 
 differentle to owner / group / others***

-rwx/rwx/rwx
=owner/group/others

read write execute

-rwxr-xr-x
= owner 는 rwx 가능
= group 은 r, x 만 가능
= users 는 r, x 만 가능

chmod 로 권한 변경 가능
chmod 640 some_file
6 = 110 = rw- for owner
4 = 100 = r-- for group
0 = 000 = --- for others

*\*모든 유저 허용   
=777 = rwxrwxrwx   
=755 = rwxr-xr-x   
=700 = rwx------   
=666 = rw-rw-rw-   
=644 = rw-r--r--   
=600 = rw-------*

sudo some_command 
= Superuser 가 됌
*권장하진 않는다

"exit" = get out of Superuser

---

history = 과거의 내가 명령을 입력했던 리스트를 알려줌

$ cat history_comm.txt
    1  pwd  
    2  ls  
    3   cd OSS   
    4  pwd   
    5  ls   
    6  cd 1학기     
    7  cd 1학기               
    8  cd Oss             
    9  pwd            
   10  ls          
   11  ls |wc-l                   
   12  ls | wc -l                            
   13  echo *               
   14  echo ~          
   15  echo print           
   16  q           
   17  ls -l             
   18  ls -l--reverse --human-readable                   
   19  ls -l--reverse--human-readable                        
   20  ls -l --reverse --human-readable              
   21  ls -l /bin/bash           
   22  chmod 600                  
   23  chmod 600 AppData           
   24  chmod 600 AppData            
   25  ls             
   26  ls -l words.txt            
   27  ls -l 옾솟SW             
   28  pwd              
   29  ls -l /Desktop/오픈소스SW/words.txt            
   30  ls - l /Desktop            
   31  ls -l /Desktop            
   32  ls Desktop             
   33  ls '오픈소스SW'              
   34  ls 오픈소스SW               
   35  ls 오픈소스SW/            
   36  nano                       
   37  nano myscript.sh            
   38  sh myscript.sh               
   39  ;s               
   40  ls            
   41  sh myscript            
   42  sh myscript.sh           
   43  history          
   44  history > history_comm.txt           
