# Google Drive Downloader
[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)   [![forthebadge](https://forthebadge.com/images/badges/uses-git.svg)](https://forthebadge.com) [![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)

![alt text](https://github.com/haindvn/GDrive-Folder-Downloader/blob/master/myDLv2.PNG?raw=true)

## Getting Started / Required Packages

* Please install `google-api-python-client google-auth-httplib2 google-auth-oauthlib apiclient termcolor oauth2client tqdm` via pip3 first

```
pip3 install google-api-python-client google-auth-httplib2 google-auth-oauthlib apiclient termcolor oauth2client tqdm
```

* You need to enable the Drive API to use the script, the enabling instructions can be found on [Python Quickstart](https://developers.google.com/drive/api/v3/quickstart/python).
* The script requires 2 generated files `credentials.json` and `token.json` from the Drive API enable processes in the same working directory of the script for Google Drive authorization.

**Notes:** please use correct version
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
$ python3 download_v3.py <text_file>
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
