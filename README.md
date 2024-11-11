<div align="center">
  <h1 align="center">Stock Data Communication Simulation Project</h1>

  <p align="center">
    Whatsapp communication template structure
    <br />
  </p>
</div>

<!-- ABOUT THE PROJECT -->
## About The Project

This project aims to create a template script for the whats app communication.

With changes in _config.json_ file and _chat.csv_ which will further introducted later, this project is able to generate number of group communication between different members of people.


<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- GETTING STARTED -->
## Getting Started

<!-- Prerequisites -->
### Prerequisites

These are the two core requiremenst in order to use this python script to compile.

* Anaconda (Python 3)
* Jupython Notebook

<!-- config.json -->
### config.json

This is the sample database structure I used for the input, 

**This contains:**


| Columns       | Description   |
| ------------- | ------------- |
| Date          | Indicates the date and time  |
| FileName      | Need to be generated maunally as it is all have to be unique. it is in the format of two digit number-four digit number. e.g. 13-3945  |
| FromPhone, ToPhone, FromName, ToName | These columns need to be generated maunally as this need to link with name and personal details. More importantly, there shouldnt be any repetition between FromPhone and ToPhone & FromName and ToName |
| Message       | This is the columns that merged with the _chat.csv_ file  |
| GroupName, GroupID  | It is there for the group chat, note that this template script is limited to generate one group for each run. In order to run a multiple numbers of group, make sure to change the 'multiple' in the setting and run the script again. |
| FromEmail, ToEmail | (not in used)  |

<!-- chat.csv -->
### chat.csv

This _.csv_ file contains all the stock trading conversation extracted from https://stocktwits.com/symbol/TSLA.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- Functionality -->
## Functionality

### Setting

In Setting, you can set multiple instances:
  * Starting and ending period
  * Interval for each onversation in minute (Note that this need to consider the number of file names in your _config.json_ file to avoid error)
  * Conversation for each day (Note that this need to consider the number of file names in your _config.json_ file to avoid error)
  * Number of people in the group chat


```sh
start = datetime.strptime('1/1/2020 09:00 AM', '%d/%m/%Y %I:%M %p')
end = datetime.strptime('14/1/2020 05:00 PM', '%d/%m/%Y %I:%M %p')
interval = 8
perday = 3
multiple = 5
  ```

### Date Modification

This functionality allows you to modify the date by number of days, months and years. 


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- Output -->
## Output

This will be the expected output when runing the script, you would get each _.eml_ file for each conversation taken, and it will be all collected under the _.zip_ file you name it **'HERE'**. Make sure to uncomment all the code in order to obtain output.
  ```sh
  zipObj = ZipFile('HERE', 'w')
  ```

<img width="592" alt="image" src="https://user-images.githubusercontent.com/61008377/193235593-b9a68a10-44f0-4b38-a15d-3361dbf7ba27.png">


<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CREDITS -->
<h2 id="credits"> :scroll: Credits</h2>

Hana Chae!

[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/hchae0817)
[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hana-chae-06a9001b8/)


<p align="right">(<a href="#readme-top">back to top</a>)</p>



