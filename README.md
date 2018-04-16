# CS499 Semester Project

This website is for a project from the CS499 - Network Analysis/Characterization course at
Northern Arizona University.


## Project Desciption

### High-level Description
The problem we are solving is creating a network of Let's Play channels on YouTube based on the number
of videos they post for games to be a channel recommender for the Let's Play channels of simliar gaming
content.

The problem that we are solving is important because the Let's Play community on YouTube has been growing
as more people watch others play video games and smaller channels could possibly use this network to do
collaborations so they can gain more subscribers or larger channels that are under parent channels can
reach out to smaller channels to give them a jumpstart on their channel.

### Technical Description

Please check back later.


## Project Team

![Image of Alex Nelson](/Images/avatar.jpg)

Name: Alexanderia "Alex" Nelson

Degree Program: B.S. in Computer Science

Name: Hailey Ginther

Degree Program: B.S. in Computer Science

## Network Visualization
![Image of Dark Souls Network](/Images/DarkSoulsNetwork.PNG)

*Fig 1. Dark Souls Network*

![Image of Resident Evil VII Network](/Images/RE7Network.PNG)

*Fig 2. Resident Evil VII Network*

These two networks were generated with a sample of 20 nodes from the dictionary created from the CSV files. The networks
are ego networks for each game that was queried. The edges represent the channel has at least one video for the game and
is allowed into the game's ego network.The nodes were randomly selected from the list of keys (channels) from the dictionary
and are only added if they have videos for the game. We chose to do 20 sample nodes becuase there are a lot of channels in
the dcitonary and the resulting graph would be unreadable.

## Jupyter Notebook for Project

[Jupyter Notebook](https://github.com/Alex-Nelson/turbo-octo-happiness/blob/master/Notebook/CS499_Semester_Project.ipynb)

Click the link to view the Jupyter Notebook for this project on the Github repository.

### Computational Envrionment

Please come back later.


## Data Used

### Description

We collected the data using the YouTube Data API to do search queries using fifty video games
that have at least 10,000 videos containing footage of the game. Videos that contain the words
_trailer_, _song_, _theme_, and _tutorial_ were excluded from our data becaue these videos do not
pertain to what videos we are trying to collect for our project. Due to the nature of the YouTube Data API,
we could only receive a max of 50 results per page and had to save the JSON data into different CSV files.

Once the query was fully completed, we formatted the CSV files to remove unnecssary columns for our data and
combined each CSV file into one CSV file that our Jupter Notebook code filters through to create the dictionary,
like the one used to create the sample networks above.

### Link to Data

[Data](https://github.com/Alex-Nelson/turbo-octo-happiness/tree/master/Data)

Click the link to view the data files we used for this project.

Each folder contains the data that was collected represents each game we performed a query on. The fields that we kept
from the original JSON data were:
- Video ID
  - This is the id that corresponds to the video. This value is unique for all videos.
- Channel ID
  - This is the id that corresponds to the channel. Multiple videos can have the same channel id.
- Video Title
  - The title assocaited with the video. This was used to help determine if the video qualified to be a part of
    our data set.
- Channel Name
  - The name of the channel that uploaded the video onto YouTube. This is used to help determine how many videos
    a channel has for each game and the name of the node if it enters a game's network.
