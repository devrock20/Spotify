# Spotify
This project is part of the Knowledge Discovery in Databases (ITCS - 6162) course from University of North Carolina at Charlotte.

#### -- Project Status: [Pending]

## Introduction to Problem
Since the Covid-19 pandemic has affected people's lives in many ways, one of the things that might have affected is the preference in music. There are many factors that affect preference in music like danceability, intensity etc. Our aim for this project is to analyze those factors and merge this analysis with a Covid-19 dataset to identify how preference in music has changed.

## Research Question
How has Covid-19 affected Spotify users' preference in music across top genres and different generations of music through the change in Covid-19 cases and comparing against pre-pandemic, by analyzing various song metrics from the weekly top charted songs on Spotify in the United States.

## Data and Source Description 
  Sno. | Source | Data and Source Description
  :---: | :----: | :------------------------
  1\. | [Spotify Charts](https://spotifycharts.com/regional) | To get the weekly top charts for the United States
  2\. | [Spotify API](https://api.spotify.com) | To get different features of the songs, such as genre and audio features, through the API
  3\. | [Spotify Dataset - Kaggle](https://www.kaggle.com/theoverman/the-spotify-hit-predictor-dataset?select=dataset-of-00s.csv) | A dataset of all the songs from the year 2000 to the year 2019
  4\. | [Covid-19 Dataset](https://covid19-lake.s3.amazonaws.com/index.html) | Public Covid-19 dataset hosted by AWS

### Metadata - Spotify Dataset
*Below are the columns that store different information related to the song:*
Sno. | Column Name | Description 
:---: | :----------: | :-----------
1\. | **position** | The position(1-200) of the song in the specified week's top charts
2\. | **streams** | The number of streams by Spotify users in the specified week's top charts
3\. | **artist** | The name of the artist
4\. | **release_date** | The date the album was first released
5\. | **genres** | A list of the genres the artist is associated with. If not yet classified, the array is empty
6\. | **region** | The country of the top charts song
7\. | **track** | The country of the top charts song

*Below are the columns that specify various features related to the song:*
Sno. | Column Name | Description 
:---: | :----------: | :-----------
1\. | **danceability** | Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable
2\. | **energy** | Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy
3\. | **key** | The estimated overall key of the track. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C/D, 2 = D, and so on. If no key was detected, the value is -1
4\. | **loudness** | The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typical range between -60 and 0 db
5\. | **mode** | Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0
6\. | **speechiness** | Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks
7\. | **acousticness** | A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic
8\. | **instrumentalness** | Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0
9\. | **liveness** | Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live
10\. | **valence** | A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry)
11\. | **tempo** | The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration

## CRISP-DM Model
### 1. Exploratory Data Analysis
The Spotify and Covid-19 datasets are collected, cleaned, and engineered using the Cross-Industry Standard Process of Data Mining (CRISP-DM), yielding a significant amount of insights.

Comparing impact on the listening pattern for different genres due to Covid-19 across the US:

<img src=https://github.com/devrock20/Spotify/blob/main/img/contemporary%20country.png width="800px">

<img src=https://github.com/devrock20/Spotify/blob/main/img/electropop.png width="800px">

<img src=https://github.com/devrock20/Spotify/blob/main/img/rap.png width="800px">


From the graphs, we can infer that song genres contemporary country and pop were having more active listeners when Covid-19 was at its peak.

Song genres like rap, hip hop, southern hip hop, trap, dance pop saw a huge decrease in their daily listeners count during the peak season of Covid-19.

Comparing impact on the listening pattern for different genres due to various events during Covid-19 impact across the US:

To analyze the impact of various events during Covid-19, we have plotted the event markers for the following events:

First Covid-19 case
First states shutdown
First public vaccination
Vaccinated people can be without masks
Comparing contemporary country pattern with the event markers we can see that this genre saw the highest number of listeners after the first public vaccination started.

Another genre impacted is electropop, where the number of listeners to the song belonging to this genre started decreasing after the states started shutdown and started to increase after vaccinated people were allowed to be without masks.

Similar to electropop, rap saw its lowest listeners after the state's shutdown started and the pattern became normal after vaccinated people were allowed to be without masks.


### 2. Data Preparation

### 3. Modeling

## Future Work:
1. We can extend the work to "How different phases of lockdown affected the preference in music".
2. We could predict the top genres across different countries given the future scenario in terms of change in Covid-19 cases.
3. Identifying the preference in music after Covid-19 is over and comparing to the preference in music before and during Covid-19.

## Contributing Project Members

|Team 2| 
|---------|
|[Satyadev Tummala](https://github.com/devrock20)| 
|[Sourabh Pandey](https://github.com/spandey5992) |    
|[Cody Hunt](https://github.com/chunt52) |
|[Manaswani Polkampally](https://github.com/manaswinipolkampally)|

