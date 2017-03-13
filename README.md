# nptel-youtube-scripts

### Steps to upload and publish transcripts/captions

- Open Google Cloud Console: https://console.cloud.google.com
- Create a new project
- Enable YouTube Data API: https://console.developers.google.com/apis/api/youtubeanalytics.googleapis.com/overview
- Create OAuth Client ID: https://console.developers.google.com/apis/credentials (Choose Application Type as Other)
- Download `client_secret.json` for the credentials to the same folder
- `$ python my_uploads.py` 
  - Google login window will open, login with correct course account
  - `videos.csv` will be written to the same folder, contains names and ids for all videos in the channel
  - Edit this file and change name of video to transcript file name with extension
- Keep all *cleaned* transcript text files in one folder 
- `$ python captions.py --data=./videos.csv --files=<complete-path-to-transcripts-folder>`
  - Wait until uploads are complete
- This will upload and publish all transcripts by automatically timing them to the speech
- Instead of transcript, srt file can also be given, in that case, timings will be taken from the srt file
  
