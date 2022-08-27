# __Essential-Google-Colab-Notebook__

All __Essential Cells__ in one Google Colab Notebook!.
You can handle your __Google Drive__ files __more convenient than before__.

<a href="https://colab.research.google.com/github/dropcreations/Essential-Google-Colab-Notebook/blob/main/All-in-One-Colab-Notebook.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab"/></a>
<br>
- Click on the __"Open in Colab"__ button to open this notebook in google colab

## __Mount Google Drive__
- You can mount and unmount your Google Drive to the runtime.
## __Manage Files & Folders__
- You can manage your folders and files with below cells.
### __Copy Files & Folders__
* `sourcePath`: add source file's or folder's path.
* You can add more source paths and seperate each by **a comma and a space**.
> **eg**: `sourcePath: [file01], [file02], [folder01], [folder02], [file03], [file04]`
* `onlyContent`: use this when coping the **content of a folder**.
> * when adding *`/content/testFolder`* will copy the content in *`testFolder`* folder, not the entire *`testFolder`*.
> * If you have added more folder paths, this will copy **only the content** in all those folders.
* `Update`: copy only when the **source file is newer than the destination file** or when **the destination file is missing**.
### __Move Files & Folders__
* `sourcePath`: add source file's or folder's path.
* You can add more source paths and seperate each by **a comma and a space**.
> **eg**: `sourcePath: [file01], [file02], [folder01], [folder02], [file03], [file04]`
* `onlyContent`: use this when moving the **content of a folder**.
> * when adding *`/content/testFolder`* will move the content in *`testFolder`* folder, not the entire *`testFolder`*.
> * If you have added more folder paths, this will copy **only the content** in all those folders.
* `Update`: move only when the **source file is newer than the destination file** or when **the destination file is missing**.
### __Delete Files & Folders__
* `sourcePath`: add source file's or folder's path.
* You can add more source paths and seperate each by **a comma and a space**.
> **eg**: `sourcePath: [file01], [file02], [folder01], [folder02], [file03], [file04]`
* `onlyContent`: use this when deleting the **content of a folder**.
> * when adding *`/content/testFolder`* will delete the content in *`testFolder`* folder, not the entire *`testFolder`*.
> * If you have added more folder paths, this will remove **only the content** in all those folders.
### __View Folder Size__
* This will show the size of **folders and sub folders only**. to view all files **select** `viewContent`.
* `modificationTime` : Use this to **view time information** of files.
* If `Summary` is selected, only shows the **total size** of the folder, So ***uncheck*** it to use `viewContent` option.
## __7-Zip__
- 7zip archiving program in colab.
### __Compress Files and Folders__
* Create **zip, tar, 7z, gz, bz2, xz, wim** files.
* If you want you can add **password** or **split** the archive.
* If you want to save archive in **another** location **uncheck** `saveToSourceLocation`.
### __Uncompress Files__
* To **list content** of the file, use `viewFile`. ***Uncheck this after viewing the content***.
* Can also extract **splited** archives.
* `saveToSourceLocation`: Extracts files to source location.
* If you want to extract files from archive **without using directory names**, uncheck `directoryNames`.
> * NOTE : ***Don't uncheck*** `directoryNames` at normal use.
>
>  ![directory_names](https://raw.githubusercontent.com/dropcreations/Essential-Google-Colab-Notebook/main/cell_logos/directory_names.png) ![without_directory_names](https://raw.githubusercontent.com/dropcreations/Essential-Google-Colab-Notebook/main/cell_logos/without_directory_names.png)
>
> * Without `directoryNames`, extracts files as **2nd figure**.
## __Transfer files to Google Drive__
- Import files to colab
### __Transfer files between two Google drives__
- Mount Google Drives and copy files.
### __Transfer files from direct links__
#### __wget__
* Transfer files from **direct links** to google drive.
* Enter the folder path where you want to save the file.
* Run cell to add direct link.
#### __JDownloader__
* Run cell to install **JDownloader** to get **WEB-UI**.
### __Transfer files from MEGA__
* Run cell to **start** transfer.
* If you have a **Mega Pro** account, select `megaProAccount` to **sign in** to use its bandwidth (transfer quota)
* You can also add a **public link** without a Pro account, but it has **transfer limits**.
* If `savePath` is not provided, files will be transfered to `/content/MEGAdownloads`.
* Sometimes this cell doesn't stop itself after the completion of the transfer. In case of that **stop the cell manually**.
### __Transfer files from Torrents__
#### __libtorrent__
* Run cell to **install libtorrent** to the runtime.
* `savePath`: add folder path where you want to download.
* `torrentFile`: use a torrent file to download.
* `magnetLink`: use a magnet link to download.
#### __qBittorrent__
* Run cell to install qBittorrent to get **WEB-UI**.
### __Redsea Tidal Downloader__
* Enter folder path where you want to **save** files.
* Run cell to **clone** and **install** dependencies for Redsea respository.
* Run cell to manage **sessions**.
* `list` - Lists stored sessions if any exist.
* `remove` - Removes a stored session from the sessions file by name.
* `default` - Set a default account for redsea to use when the -a flag has not been passed.
* `reauth` - Reauthenticates with server to get new sessionId.
* `add` - Prompts for a TV, Mobile or Desktop session. The TV option displays a 6 digit key which should be entered inside link.tidal.com where the user can login. The Mobile/Desktop option prompts for a Tidal username and password. Both options authorize a session which then gets stored in the sessions file.
* Enter **sessionName** that you created in above cell.
* Enter **album/track/playlist/video link** or **links** to download.
* Separate multiple urls by **spaces**.
> **eg:** `url: [url_01] [url_02] [url_03] [url_04]...`
* Files will be in **"RedSea/downloads"** in your save location.
* You can **explore** for available **atmos / 360 albums and tracks**.
* Check "explore" and select a "**explore_type**".
* You can also search for **track/album/video**, use **search options**.
* You can use explore or search, **not both at once**.
* If you have **already cloned and used** Redsea reop, enter the "**RedSea**" folder path and run below cell.
* Then you can run cells again **without authentication**. **[Session & Download cells]**
### __youtube-dl__
* `videoLink`: YouTube and other supported website URLs are working.
* `outputFolder`: Set the download directory.
* `Preset`: All presets are working for YouTube URLs, but if you entering an another website's URL set `Preset: Choose Codecs`.
> You can add formatCodes as `{video_code}+{audio_code}` to get a full output.
* `mergeFile`: Merge final output to an another container format.
* `viewFormats`: You can view all available formats to download.
* Please uncheck `viewFormats` while downloading.
## __Mediainfo__
* Run cell to **get** mediainfo.
## __FFmpeg__
* Run cell to **Install** FFmpeg.
### __Remux Video Files__
* **REMUX** video files without **RE-ENCODING**.
* Make sure that `outputFormat` that you have selected is supported for all tracks in the `inputFile`.
* `WebM` only support `VP9`, `VP8`, `AV1` video and `Vorbis`, `Opus` audio and `WebVTT` subtitles.
### __Trim Video Files__
* **TRIM** video files without **RE-ENCODING**.
* `inputFile`: video file's path and set `startTime` and `endTime` to trim.
* Trimed video will be saved as same as the **source's format**.
### __Extract Audio__
* **EXTRACT** audio tracks from video files.
* `DTS`, `DTS-HD`, `DTS-MA`, `TrueHD` tracks will be muxed as a `.mka` file.
### __Remove Bitstream Metadata__
* For `H.264`/`AVC` tracks run first cell.
* For `H.265`/`HEVC` tracks run second cell.
### __Encode H.264__
* `CRF` and `2-Pass` encoding available.
* This cell only encodes the **first video track** from the input file.
### __HDR to SDR__
* Convert `HDR` video to `SDR` video.
* `toneMap`: Select tone mapping method.
### __HDR10 Encoding__
* Only `x265`/`HEVC` tracks are supported.
* `extractColors`: View the color information of the footage.
* When encoding, make sure `extractColors` is **deselected**.
## __H.264 Encoder__
* This encodes **video track** only.
* Use ffmpeg or any other to **merge** video with audios.
* Run cell to **install** x264.
* Set `inputFile` and `outputFolder`.
* This cell is taking the output name as same as the input filename. So, you need to set the output folder only.
* Change **settings** as you want.
## __MP4Box__
* Run cell to **install** MP4Box.
### __Create MP4/M4A Files__
* Enter **tracks** while running the cell.
* Tracks must be in **raw format**. `(eg: .h264, .hevc, .aac, .eac3,....)`
* If you don't want to add **track title** and **track language** leave them blank.
### __Tag MP4 / M4A Files__
* Enter **MP4 or M4A** file path in **`inputFile`**.
* `updateFile`: Update the exsisting file with tags.
* Recommended to use **Mutagen MP4/M4A tagger** for advanced use.
## __MKVToolNix__
* Run cell to **install** MKVToolNix.
* You can use any version, to do that enter the version correctly in `Version`.
### __mkvmerge__
* You can **input tracks** while running the cell.
* Don't use `#` and `"` in `mkvTitle`.
* Add XML file path for `globalTags`, `segmentInfo`.
* Choose a `splitMode` and add `splitArgument` **according** to the `splitMode`.
* Chapter are accpeted **both** `XML` and `OGM_txt` files.
* When adding a language use **laguage codes**.
* If you don't want to fill a field, leave it blank.
* If you don't know what is the relevant `mime-type`, also leave it blank in `attachmentmimeType`.
* When adding track `default`, `forced` flags, If you leave it blank, it's value will be '**No**'.
* For all inputs **'y'** for **'yes'** and **'n'** for **'no'**. 
* `webmCompliantFile`: Create a WebM compliant file instead of mkv.
* Add tracks while running the cell and after adding all tracks you want, type **'done'** in `inputFile` to continue.
### __mkvextract__
* You can extract **all tracks, attachments, chapters, tags, cues, cue sheet, timecodes** from below cell.
* Also you can extract a **single track** by selecting `extractMode: Single Track` option.
### __mkvpropedit__
* You can edit **segment info, track info, chapters, attachments, tags** in a mkv file.
* If you want to **delete statistic tags** from tracks select `deleteTrackStatisticsTags`
### __Matroska/WebM Tags__
* Enter **mkv file's path** in `mkvFile`.
* If you want to delete `Title` type **"delete"** in `Title`.
* If you want to add **multiple values**, separate tags by a **comma** and a **space**.
> `Eg: Artist: Artist1, Artist2, Artist3`
* You can add **tags** using a **text document**. Text document's content must be as formatted as below.
> `Tag name 1: Tag value 1, Tag value 2, Tag value 3`<br>
> `Tag name 2: Tag value 1, Tag value 2, Tag value 3`<br>
* Explainations are available while running the cell.
## __Mutagen__
* Mutagen is a python based multimedia **tagging** library.
* Run cell to **install** Mutagen.
### __FLAC__
* Enter **FLAC** file path in `inputFLAC`.
* If you want to add **multiple values**, separate tags by a **comma** and a **space**.
> `Eg: Artist: Artist1, Artist2, Artist3`
* You can add **more custom tags** using a **text file**. Text file's content must be as formatted as below.
> `Tag name 1: Tag value 1, Tag value 2, Tag value 3`<br>
> `Tag name 2: Tag value 1, Tag value 2, Tag value 3`<br>
* Explainations are available while running the cell.
### __MP4 / M4A__
* Enter **MP4/M4A** file path in `inputMP4`.
* If you want to add **multiple values**, separate tags by a **comma** and a **space**.
> `Eg: Artist: Artist1, Artist2, Artist3`
* You can add **more custom tags** using a **text file**. Text file's content must be as formatted as below.
> `Tag name 1: Tag value 1, Tag value 2, Tag value 3`<br>
> `Tag name 2: Tag value 1, Tag value 2, Tag value 3`<br>
* Explainations are available while running the cell.
