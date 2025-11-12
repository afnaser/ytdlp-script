
---

# Windows Powershell Script for YT-DLP

After extracting this folder wherever you want it.

### Converting RUN_SETUP.txt into a Powershell Script

1. Open the “RUN_SETUP.txt” file.

2. With the "RUN_SETUP.txt" file open in notepad, Select “File” > “Save As” and save it with:
* File name: RUN_SETUP.ps1
* Save as type: All Files

3. After the "RUN_SETUP.ps1" file is created, you can now right click it and select "Run with Powershell".
* This unzips the required executables in the `bin` folder, as well as creates the "ytdlp.ps1" script.

### Running the yt-dlp Script

4. Any Youtube (or other website) videos/audios you want to download, simply copy the Website's URL and paste it in the "urls.txt" file.

* ONE URL PER LINE
    - You can copy and paste multiple different URL's in the "urls.txt" file to download multiple videos at once. Make sure to only have one URL listed per line.

* You can either copy and paste the URL of single videos/audios, or a URL of an entire playlist
    - If you copy a playlist's URL, it will download all videos in the playlist and properly order/index them with a prefix (i.e. 1_VideoA, 2_VideoB, 3_VideoC)

5. Right click the `ytdlp.ps1` file, and choose “Run with PowerShell”. This will run the script and ask you what you want to do.
    - If you need to stop/cancel all downloads while in progress, press `ctrl + C`

### Explaining Additional Folders

6. All downloads will be completed and listed in the "Downloads" folder inside this overall folder.

7. All programs being used are in the "bin" folder. You should never need to access this folder after unzipping the executables into this folder via the initial "RUN_SETUP.ps1" script.

8. "archive.txt" file is found in the "archive" folder. If selected when you run the script, this will store the history of your downloads to prevent duplicates from being downloaded. You should not have to access this folder.

---

### OPTIONAL READING: ADDITIONAL EXPLANATION OF SCRIPT:

The script prompts that it asks the user should be self explanatory, but more detailed explanation can be found below if necessary.

* Question 1: What do you want to download?
    - "1. MP4 Videos": If you want to download the entire video from a URL.
    - "2. MP3 Audio": If you only want to download the audio from a URL, not the video.
    - "3. Subtitles Only": If you only want to download a Subtitle file for a video, and neither the video nor audio.

* Question 2: Do you want to skip URLs that you already downloaded?
    As you download from URLs, there will be an "archive.txt" file that saves the history of what is downloaded to prevent duplicate downloading. This "archive.txt" file can be found inside the "Archive" folder inside this overall folder. 
    - "1. Yes": Selecting Yes will save the history and prevent a duplicate download
    - "2. No": Selecting No will download a video without saving the history of it being downloaded, regardless of if it was downloaded in the past.

* Question 3: Use cookies from what internet browser? (Needed for age-restricted videos)
    - "1. Firefox": Choose this if you main internet browser is Firefox
    - "2. Chrome": Choose this if you main internet browser is Chrome
    - "3. Edge": Choose this if you main internet browser is Edge
    - "4. No Cookies": Only choose this if you are having trouble downloading something. You typically want to always use your browser's cookies

* Question 4: Do you want videos with...:
    - "1. No Subtitle": Use this if you do NOT want to have a separately downloaded subtitle file. (Only works/prompts user for videos).
    - "2. Subtitles": Use this if you DO want to have a separately downloaded subtitle file. (Only works/prompts user for videos).

---
