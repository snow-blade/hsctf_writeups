### Description
I found this file on my Keith's computer... what could be inside?

Author: AC
### Writeup
We were given a zip file, this zipfile contained 8 other zips.
This one was also easy as i figured out i just had to extract the comments from the zip files, i just made a python script which extracted them all<br>
This script is not 100% reliable as it only extracted the first comments but left out the last one, it was easy to know what the last character was as i know it would be a closing bracket<br>
```
from zipfile import ZipFile
with ZipFile('../Downloads/Comments.zip','r') as zz:
  zz.extractall()
  print(zz.getinfo('1.zip').comment)
count=1
while count!=9:
  with ZipFile(str(count)+'.zip','r') as zz:
     zz.extractall()
     try: 
       print(zz.getinfo(str(count+1)+'.zip').comment)
     except:
       pass
     count+=1


```
Here is the screenshot of the output
![Output](/output1.png)<br>
As you can see the flag is flag{4n6}
