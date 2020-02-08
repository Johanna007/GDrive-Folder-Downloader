# Google Drive Downloader
**Notes:** *download_v2.py* script is for Python 3 users and the others are for Python 2 (some codes that I sent to author via email years ago, it seems that he has not maintained the codes anymore since my pull requests are ignored).

Google Drive Downloader

![alt text](https://github.com/duytran1406/gdrivedownloader/blob/master/myDl.png?raw=true)


## Getting Started

You need to enable the Drive API to use the script.
The enabling instructions can be found on [Python Quickstart](https://developers.google.com/drive/api/v3/quickstart/python).<br/>
The script requires `credentials.json` in the same working directory for Google Drive authorization.

### Usage

**Interactive Mode:** just run the script directly from command line "*python download_v2.py*" then follow instruction to input parameters to initialize download.

**Batch Mode:** if you love to use shell for unattended downloadings, this mode is for you. For each folder, you create one text file with the contents
* Local Path
* Local Folder Name
* Google Folder ID

Then initialize unattended downloading from shell/command line via 
```
$ python download_v2.py <text_file>
```
