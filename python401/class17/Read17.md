# What Does Automation Mean?
  - Automation is the creation and application of technologies to produce and deliver goods and services with minimal human intervention
# Python Regular Expression Tutorial
   - In Python, regular expressions are supported by the re module. ```  import re ```

## Basic Patterns: Ordinary Characters
  - You can easily tackle many basic patterns in Python using ordinary characters
      ```  
            pattern = r"Cookie"
            sequence = "Cookie"
            if re.match(pattern, sequence):
                print("Match!")
            else: print("Not a match!")
   

## shutil 
  - The shutil module offers a number of high-level operations on files and collections of files. In particular, functions are provided which support file copying and removal. For operations on individual files, see also the os module.
  - copyfile() copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.
   
              ``` # shutil_copyfile.py 
                    import glob
                    import shutil

                    print('BEFORE:', glob.glob('shutil_copyfile.*'))

                    shutil.copyfile('shutil_copyfile.py', 'shutil_copyfile.py.copy')

                    print('AFTER:', glob.glob('shutil_copyfile.*'))
                    ######################

                    BEFORE: ['shutil_copyfile.py']
                    AFTER: ['shutil_copyfile.py', 'shutil_copyfile.py.copy']


## we can also dealing with 
  - Copying File Metadata¶
  - Working With Directory Trees
  - Finding Files
  - Archives
  - File System Space
              
              
              
          
             
