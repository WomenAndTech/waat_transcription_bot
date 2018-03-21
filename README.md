# Women&&Tech Transcription Bot

This bot will help us upload audio files (interviews) to an Azure Blob Storage Account and kick off the process for transcription.

## Workflow

1. Got to #audiotranscription channel
2. Upload a file into that channel
3. Bot will pick it up and save it to an Azure Blob Storage Account (like dropbox but less bells and whistles…more primitive)
4. Once upload is complete an Azure function (which is bound to the storage account) will notice that a new file has been uploaded
5. The function will then send the audio file off to Azure Cognitive services for processing (Speech API)
6. Cognitive services will process the file and return text
7. Text will then be stored somewhere (TBD) and returned to the slack channel (maybe…might just send a link to the text file…not sure yet)
8. Great Success!