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
   
   5. cd ../home/' '/Folder1/..
        result- /home/' ' 
        
  Listing:
  
  1. ls -l ( provides text files in the present folder)
  
  2. ls -R ( Give directory listing in the file)
  
  3. ls -a (Displays hidden files)
  
  4. ls -la ( give long lisitng of all the files)
  
  5. ls file* ( globbing, displays all files starting with file*)
  
 ## Creating, moving, and deleting files
 
 cmnds used: touch, rm, mv, cp, mkdir, rmdir. 
 
 Commands:
 1. touch ( create empty file, or update timestamp).
 
 2. rm ( remove file, and folder if used recursively)
 
 3. mv ( moves files and folders)
 
 4. cp ( copies files, and folders if used recursively)
 
     ** eg: cp thing1.txt .. ('..' will copy thing1.txt into above directory in path)
      
         ** cp -R thing2 thing3 ( -R= recursively,  It will copy thing2 directory into thing3 dir, [directory cannot be copied if -R is not used.] ) 
 
 5. mkdir ( makes directory)
      
     ** eg: mv myfolder folder1 (myfolder= folder want to move. folder1= destination)
            [Now myfolder and folder 1 does not exist. So 'mv' cmd will make these folders ad mv myfolder into folder1]
 
 6. rmdir ( remove directory)
      
       ** eg: rmdir thing2 ( if dir is not empty it is going to give error)
              to avoid error:
                cd thing2
                  rm* (remove all)
                    cd ..
                      rmdir thing2 (it will del the folder succesfully)
                      
               rmdir thing3 (gives error if dir not empty: reason: hidden files)
                 to avoid error:
                   cd thing3
                    ls -a (shows hidden content)
                      cd ..
                        rm -rf thing3 ( ** IT DEL RECURSIVELY, AND FORCEFULLY ( CAREFUL ) DIR WILL BE DELTED.)
                        
               
               
## Archiving files on the command line . 

  Archiving = tar, zip
  compression = gzip, bzip2, zip
  
  { gzip= compression format, it takes file and compress it. 
    gunzip= to unzip compressed file. }
    
  { bzip2= offers greater compression and mostly used for big files.
    bunzip2= decompression tool, to decompress files. }
    
  { zip= offers archiving anf compression both, it will compress the files in a folder and archive the folder.
    unzip= to decompress files.}
    
  { tar= Tape archive, it will archive folder and then we can gzip it, or bzip it.
    
    tar= tar -cf (file.tar.gz)
         tar -xf (file.tgz)
         
    tar + compression
    tar-cfz (gzip) (file.tar.bz2)
    tar-cfj (bzip2) (file.tbz) 
    
    (cfz= create file gzip, cfj= create file bzip2) }
    
    Commands:
    
   
      zip file.zip thing1
   
      zip -R file.zip thing1
      (-R is used recursively, and cmnd shows the content and compress them as well)
      
      rm -rf thing1
      
      unzip file.zip
        (it will create thing1 qnd bring back the archived and compressed fiels into the folder)
        
      tar -cf files.tar file2.jpg file3.jpg (-cf= create file, files.tar= file name, file2.jpg file3.jpg= sub files in main file)
      
      tar -xf files.tar ( xf=extract files)
        (bring back the files which were archived)
        
      tar -xvf files.tar (v= shows the extracted files)
        (it will show files for content display)
        
      gzip files.tar
        (compress the tar file into much smaller space and gz is the format)
        
      gunzip files.tar.gz
        (unzip the file to back to its size.)
        
      bzip2 file.tar
        (compress file more than gzip.bz2)
        
      bunzip2 files.tar.bz2
        (unzip back to normal size.)
        
      tar -zxvf file.tgz ( file.tgz= file to extract)
        (compression on command line)
        
      tar -jcvf bzipfile.bz2 thing1 
      
      
## Searching and extracting data from files

    cmnds used: 
      
    less = read a file
    head/tail= view begining or end of file
    find= locate file on a syatem
    grep= search for strings in a file
    sort= organize text in a file
    cut= manipulate data by column
    wc= word count
    
    Reg ex= Regular expression
    
    ^= beginning of line
    $= end of line
    .=any single character 
    
    Commands:
    
    Cat abcfile.txt
      shows content of the file
      
    less abcfile.txt
    
    head -n 2 abcfile.txt ( Head= top of text, -n= num of lines, 2= 2 lines) 
      (show top 2 lines in file)
      
    tail -n 3 abcfile.txt
      (show last 3 lines in file)
    
    find
      (it provides all the files present in dir)
    
    find. -type f (type f= only files)
      (shows only files in the present directory)
    
    find. -type f | grep abc 
     ( takes result og '-type f' and | pipe will take result and search grep abc. )
     
    grep abc abcfile.txt
      (show abc from file)
     
    grep abc*
     ( show all the things with abc(including files, text )
   
    grep aa*
     ( show files, text starting with 'aa')
     
    sort file3.txt
      (It will sort the content alphabatically)
     
    Sort -r file3.txt
      (Sort recursevily)
    
    Sort -R file3.txt
      (sort file randomly)
      
    cut -c2-4 file1.txt 
     ( cut all the data and give result of '-c2-4' )  ( c= column)
     
    cut -d " " -f3 file2.txt | cut -c2 ( d= dilameter, -f2= field)
      (It will show f3 result and then cut -c2)
      
    cut -d " " -f3 file2.txt > newfile.txt
      (it will store the result in newfile.txt and you can cat the file to see the result)
      
    wc file3.txt (gives word count)
      4 18 84 file3.txt ( 4= LINE, 18= WORD, 84= CHARACTER)
      
    wc -w files3.txt
      only gives word count
      
    
                        
 
 
   
        



      



