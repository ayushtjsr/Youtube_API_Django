 YouTube_API_Django
This Project is developed in Django Python.

 Project Goal - 
To make an API to fetch latest videos sorted in reverse chronological order of their publishing date-time from YouTube for a given tag/search query in a paginated response.

 Project Detail - 
Implemented this project using Django with the latest Async views. Created an app api inside the django project.Under the views of the api enabled the latest django async features. Also created a model for the videos with a GET API which returns the stored video data sorted in descending order of published datetime.t


 Result - 
After running this django project in your local system the final paginated response will look like this - 

![alt text]((https://github.com/ayushtjsr/Youtube_API_Django/edit/main/README.md))

 Functionality Covered -
```buildoutcfg
- Server call the YouTube API continuously in background with some interval (here - 10 seconds)
- Fetch the latest videos for a predefined search query (here - "Football")
- Stores the data of videosin a database with proper indexes (here - Index starts with 1)
- A GET API which returns the stored video data in a paginated response sorted in descending order of published datetime.
- Scalable and optimised.
- Added support for supplying multiple API keys so that if quota is exhausted on one, it automatically uses the next available key.
```

 Key Files Used - 
```buildoutvfg
mysite/yt/views.py
mysite/yt/templates/yt/home.html
```
- "views.py" contains the code for the API usage and data extraction.
- "home.html" contains the code for the UI of the web page in which the final paginated response from API will be displayed.

 Instructions to start Django Server on Localhost - 

1. Download ZIP file of this repo and extract it in local system.
2. Open the extracted file in Pyhton IDE.
3. Then in your terminal direct to the folder which has this project.
4. Then type the below commands in your terminal for the web server to start.
```buildoutcfg
cd mysite
python manage.py runserver
```
5. Do this in your terminal to run the program in your web browser.
6. You will get a link of your web page open that link to see the final paginated response.

API -
```buildoutcfg
https://www.googleapis.com/youtube/v3/search?part=snippet&q=football&maxResults=1&type=video&eventType=completed&order=date&key=AIzaSyB9QNacHSAQ4deQp4RjVf3gXZOKXtMCwJk
```
 NOTE - Here in above API maxResults is set is to 1
API keys used in this project -
```buildoutcfg
AIzaSyB9QNacHSAQ4deQp4RjVf3gXZOKXtMCwJk
AIzaSyDK-WNR6d2LayUqiemCKOcMYPlDV6jvTh0
AIzaSyCmLgeX3GtUgfn7ZjkkWHfOWCMb1MkDEpU
AIzaSyAip91VlvxNxaw7Fd1mF1s0lUtegg5WtPU
AIzaSyDAYksLzTBkPf9TQC6th2c9iBSXZ6-Dl8I
AIzaSyDa1vWMOyRYGq4Qv4Lg_AelhTAiHw4E7OQ
