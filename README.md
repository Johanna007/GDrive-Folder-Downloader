# Google Drive Downloader

Google Drive Downloader

![alt text](https://github.com/duytran1406/gdrivedownloader/blob/master/myDl.png?raw=true)


## Getting Started

You need to enable the Drive API to use the script.
The enabling instructions can be found on [Python Quickstart](https://developers.google.com/drive/api/v3/quickstart/python).<br/>
The script requires `credentials.json` in the same working directory for Google Drive authorization.

**Notes:** *download_v3.py* script is for Python 3 users and the others are for Python 2 (some codes that I sent to author via email years ago, it seems that he has not mai$
* *download.py*: Python 2+ original script
* *download_v2*: Python 2+ original script with unattended download feature added
* *download_v3*: Python 3+ original script with unattended download feature added

### Usage

**Interactive Mode:** just run the script directly from command line "*python download_v2.py*" then follow instruction to input parameters to initialize download.

**Batch Mode:** if you love to use shell for unattended downloadings, this mode is for you. For each folder, you create one text file with the contents
* Local Path
* Local Folder Name
* Google Folder ID

Then initialize unattended downloading from shell/command line via 
```
$ python download_v3.py <text_file>
```

**Hint:** you can download many folders at once by creating many input files *<text_file_1>,<text_file_2>,<text_file_3>,<text_file_4>*..etc for many folders, then create a batch file (Windows) or bash shell cript (Linux) then call them at once (use **screen** in Linux if you connect via SSH / then you can safely log out/resume later without downloading interruption). 

Batch file *download.bat* or bash shell script *download.sh* content
```
python3 download_v3.py <text_file_1>
python3 download_v3.py <text_file_2>
python3 download_v3.py <text_file_3>
python3 download_v3.py <text_file_4>
```
Then
```
$ chmod +x download.sh
$ ./download.sh
```
