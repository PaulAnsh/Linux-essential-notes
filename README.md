# Linux-essential-notes
This Repository is documentary of my learning Linux essesntials certification. 

## Intro to Linux

An open source OS based on an older OS called Unix. 

A family of open source unix-like OS, typically packaged into a distribution. eg: ubuntu, debia, etc.

## Open source philosophy

Cocept of making source code availble for public use or modification from its orginial design. 
Major open source application: Openoffice, firefox, Thunderbird, Chronium, Apache, Sambma, NFS, MY SQL, Post.fx, libreoffice. 

There are different types of software licenese used in the open source:
  1. GNU (General Public Licenese) 
  2. Apache License
  3. MIT
  4. Unlicense

## Linux Distribution

Each distro consists of:
  1. Linux Kernel
  2. Supporting software and libraries
  3. Configuration files, etc. 

Kernel - A low-level computer program which functions as the bridge between the user and the computer's resources. 


## Command line basics

Shell - The program oroviding traditional text interface to the linux system. 

Commands: 
  1. ls ( list)
      ls -l (permission, Date-time of file)
  
  2. Cat ( Display content of file)

  3. echo (echo anything)
  
  4. a= hello
        enter
          echo $a
            result= hello
      
  5. ls *.txt (for dispalying files ending with .txt)
    
  6. -/Documents $echo $Path ( Shows rhe path where cmnds are stored)
  
  7. which ls ( which- shows where 'ls' cmd is stored) 
      /bin/ls (directory path)
      
  8. history (provides recent history of cmnds used) 
  
  
  ## Using command line to get help
  
  cmnds used: man, man -k, info, whatis, whereis, less for /user/share/doc
  
  Commands:
   1. ls --help ( to get help and info)

   2. man ls ( to read man page(user command summary) about ls)
       man echo ( to read man page(user command summary) about echo)
       
   3. man -k echo ( to see which program have word echo in it)
   
   4. Whatis cat ( whatis- descirbes about cat command)
   
   5. Whatis ping ( describes about ping cmd)
   
   6. whereis man ( whereis- shows where the mannual or binary page is. it shows location of man page on device)

   7. inf man( provides documentation of the page)
  
  
  ## Using Directories and listing files
  
  cmnds used: cd, pwd, ls, mv. 
  
  Commands:
   1. pwd ( present working directory)
    
   2. cd .. ( '..' takes back to one folder in heirachy) 
   
   3. cd ~/Folder1 (' ~ ' takes you firectly to folder no matter the relative path)
   
   4. cd /etc (changes directory to the directory specified after the slash /)
   
   5. cd ../home/spowers/Folder1/..
        result- /home/spowers. 



      



