# Python---Exploratory-Data-Analysis-on-Spotify-2023-Dataset_MUNSON

Author: Lucas Munson (homiekwkm)



This deliverable tasks the student to perform an exploratory data analysis (EDA) on a provided data set containing the most popular tracks of Spotify in 2023. With this dataset, it is expected that the output consists of the statistics, visualizations, and observations prompted by the guide questions.

## Dependencies
The program requires the following dependencies in order to accomplish its purpose:

1. Pandas
2. Matplotlib.pyplot
3. Seaborn
4. spotify-2023.csv

## Introduction to Dataset
The dataset is that of the *Most Streamed Spotify Songs 2023*. It expresses numerically the data of the most popular tracks that have been uploaded on streaming services. It covers a wide array of information, ranging from streaming statistics, to the musically technical aspects of the tracks. In regards to the properties of the dataset itself, it consists of a large amount of columns and rows to fully display information on over 950 tracks, with numerous datatypes to observe. A snippet of the first 10 entries of the actual .xlsx file itself can be seen below:

![image](https://github.com/user-attachments/assets/fd4386da-6173-49ef-8509-3ec252db894b)

## Program Analysis

To begin the program, the required dependencies were imported and loaded. To load the .csv file without issue, encoding='latin-1' was made use of in order to include any non-English characters.

![image](https://github.com/user-attachments/assets/522c68e9-839b-43b3-adb6-6b9626f4b3ec)

After the dataset—data, was loaded into the program, analysis began as the guide questions were answered with the appropriate codes.

The following information will be in the format of the question, the observation, the code, and then the result yielded from the code.

## Guide Questions 

### Overview of Dataset
#### > How many rows and columns does the dataset contain?
Using data.shape, it was obtained that the amount of rows in the dataset is 953, while the amount of columns is 24. 

![image](https://github.com/user-attachments/assets/6109846d-30f5-49fc-90c5-9c978d46b43b)

#### > What are the data types of each column? Are there any missing values?
The data types in the dataset consist of integers and objects. There are two data types with missing values: in_shazam_charts and key. The missing values in in_shazam_charts are 50, and the missing values in key are 95. The datatypes and missing values are presented by the code below:

![image](https://github.com/user-attachments/assets/2c84d7ba-187e-49b8-a863-750c573c872d)


### Basic Descriptive Statistics
#### What are the mean, median, and standard deviation of the streams column?
The mean of the streams column is 514137424.93907565, the median is 290530915.0, and standard deviation of the streams column is 566856949.0388832. Using the attributes .mean, .median, and .std, each individual value of data was derived.

![image](https://github.com/user-attachments/assets/6af0cff1-2f1c-4d43-840d-1997be3b9034)


#### > What is the distribution of released_year and artist_count? Are there any noticeable trends or outliers?
In terms of distribution of released_year, the tracks per year are generally in the single digit to double digit range, with the amount of tracks generally increasing the more recent the year. The outliers here are the years 2023, 2022, and 2021, as the amounts of tracks streamed in those years go past the hundreds. By the graph below, the noticeable trend is that the number of tracks played per released year increase as it approaches the present. In terms of distribution of artist_count, a majority of the streamed tracks are by a single artist, with the major outliers being the two tracks including 7 artists, and the 8 tracks including 8 artists. It can be concluded that users of the platforms have the most interest in recently released music, as the tracks included increase overtime. It can also be concluded that solo acts are most popular with users.

![image](https://github.com/user-attachments/assets/94e76347-bae2-44c0-850c-d161689a5525)
![image](https://github.com/user-attachments/assets/6fbb4680-22e3-4350-aa93-0ce5b04e5fdc)

### Top Performers
#### > Which track has the highest number of streams? Display the top 5 most streamed tracks.
The track with the highest number of streams is "Blinding Lights" by The Weeknd, with 3,703,895,074 
streams. The four other tracks are displayed below:

![image](https://github.com/user-attachments/assets/e9cb8721-494b-4583-8483-b3eebd6004cc)

#### > Who are the top 5 most frequent artists based on the number of tracks in the dataset?
The five most frequents artists are as shown:

![image](https://github.com/user-attachments/assets/7a027f97-0a16-4538-b6a5-44b0faf002d3)

### Temporal Trends
#### > Analyze the trends in the number of tracks released over time. Plot the number of tracks released per year.
As recency is the main appeal for users, the trend is that the number of tracks released increase over time. The years up until 2021 do not go past 100 or more tracks.

![image](https://github.com/user-attachments/assets/c4a7fe03-2a23-4c01-bda5-dccf4245256a)
![image](https://github.com/user-attachments/assets/b097749f-3a18-4992-adbc-e92f085aa08b)

#### > Does the number of tracks released per month follow any noticeable patterns? Which month sees the most releases?
The most number of tracks released are in the month of January. The noticeable pattern is that track releases peak in the first half of the year. 

![image](https://github.com/user-attachments/assets/4676d6a2-860a-4c4b-aa64-fbb65e33b668)

### Genre and Music Characteristics
#### > Examine the correlation between streams and musical attributes like bpm, danceability_%, and energy_%. Which attributes seem to influence streams the most?
Given the negative correlation as seen below, it can be concluded that the three attributes have no correlation with streams, thus none have a conclusive influence with streams over the other.

![image](https://github.com/user-attachments/assets/2f104e67-77fc-4e73-9ac3-03b1288e2547)

#### > Is there a correlation between danceability_% and energy_%? How about valence_% and acousticness_%?
Valence and acousticness has a negative correlation, but danceability and energy has a 0.1980948483762567 correlation.

![image](https://github.com/user-attachments/assets/3b20cc4e-1fa6-4fb9-b16e-4356ec708b00)

### Platform Popularity
#### > How do the numbers of tracks in spotify_playlists, spotify_charts, and apple_playlists compare? Which platform seems to favor the most popular tracks?
Given the averages obtained through getting the mean of each individual platform's playlists, it is clear that Spotify favors the most popular tracks. This can mean that for general listening many users opt for Spotify over any other platform, or that overall Spotify just has a much larger userbase than the other two platforms, so much so that even with just the top tracks it manages to beat Apple and Deezer.

![image](https://github.com/user-attachments/assets/aef141db-7dde-4921-9eab-291742397073)

### Advanced Analysis
#### > Based on the streams data, can you identify any patterns among tracks with the same key or mode (Major vs. Minor)? 
For the key, the most streamed tracks are those in the key of C#. Between major and minor, the more streamed tracks are major. In terms of mode, the pattern is that it is likely users prefer more upbeat and cheery music to enjoy leisurely.

![image](https://github.com/user-attachments/assets/6b189a48-2ce7-4600-a73f-1aba2caa3db6)

#### > Do certain genres or artists consistently appear in more playlists or charts? Perform an analysis to compare the most frequently appearing artists in playlists or charts.
Certain artists do consistently appear in more playlists and charts, as proven by the obtained values below displaying the artists with the most appearances across all platforms. Consistency such as this can be attributed to the quality of the artist's music, and their talent for making top songs that reach their audiences well; The Weeknd is by far the most frequent in playlists and charts, likely for these reasons as well.

![image](https://github.com/user-attachments/assets/99868350-c6bd-4290-a1f5-b445d5eae7b1)

## Author Notes

Thank you for reading this README file. It was personally an interesting experience creating this program, not just for the experience of coding each individual prompt, but to learn about the different streaming statistics of songs I enjoy. I hope this repository inspires you to work harder on more Python codes, and serves as a good piece of reference. 

Lucas Daniel D. Munson

2ECE-A
