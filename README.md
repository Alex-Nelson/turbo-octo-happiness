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

Please check back later.

## Network Visualization
![Image of Dark Souls Network](https://github.com/Alex-Nelson/turbo-octo-happiness/blob/master/Images/DarkSoulsNetwork.PNG)
*Fig 1. Dark Souls Network*

![Image of Resident Evil VII Network](https://github.com/Alex-Nelson/turbo-octo-happiness/blob/master/Images/RE7Network.PNG)
*Fig 2. Resident Evil VII Network*

These two networks were generated with a sample of 20 nodes from the dictionary created from the CSV files.
The nodes were randomly selected from the list of keys (channels) from the dictionary and are only added if
they have videos for the game. We chose to do 20 sample nodes becuase there are a lot of channels in the dcitonary
and the resulting graph would be unreadable.

## Jupyter Notebook for Project

[Jupyter Notebook](https://github.com/Alex-Nelson/turbo-octo-happiness/blob/master/Notebook/CS499_Semester_Project.ipynb)
Click the link to view the Jupyter Notebook for this project on the Github repository.

## Data Used

### Description

We collected the data using the YouTube Data API to do search queries using fifty video games
that have at least 10,000 videos containing footage of the game. Videos that contain the words
_trailer_, _song_, _theme_, and _tutorial_ were excluded from our data becaue these videos do not
pertain to what videos we are trying to collect for our project. Due to the nature of the YouTube Data API,
we could only receive a max of 50 results per page and had to save the JSON data into different CSV files.

Once the query was fully completed, we formatted the CSV files to remove unnecssary columns for our data and
combined each CSV file into one CSV file that our Jupter Notebook code filters through to create the dictionary,
like the one used to create 

### Link to Data

[Data](https://github.com/Alex-Nelson/turbo-octo-happiness/tree/master/Data)
Click the link to view the data files we used for this project.
