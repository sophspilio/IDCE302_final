# IDCE 302: Final Project 
Sophie Spiliotopoulos and Rob Kearney
## Script 1: Web Scraping Weather Forecast with Python
This code web scrapes from the National Weather Service five day forecast. It combines techniques from Labs 3 and 4, with a focus on web scraping using `beautiful soup` and data munging using string manipulation. The code begins by prompting the user for a latitude and longitude that are converted to strings and inserted into the `url` that requests the weather at the given location. The script then retrieves the information from the page, parses it using `beautiful soup`, and finally assigns it to a string `weather_forecast`, which we add to a list called `forecast`. To clean up this data, we used a for loop and the `.replace()` function to clean up the data, removing excessive spaces and newlines. This [Stack Overflow article](https://stackoverflow.com/questions/37505224/add-a-space-between-each-word-in-the-string) was useful to add spaces in between some of the words. We used `replace` and `re.sub` to add a whitespace before each uppercase letter. This specific line of code was useful for this scenario because the words we wanted to add space between were all capitalized. 

Writing this script went relatively smoothly, with only minimal errors along the way that we were able to quickly debug. We found Lab 3, Lab 4, the textbook, and the Stack Overflow article mentioned above the most helpful for debugging. 
This script is definitely something that we could use in the future for a number of different types of projects. It applies web scraping and data munging, which are both important fundamental skills to have in the coding world. 

See the code for script 1 in the attached  `.ipynb` file entitled `302Final_script1`. 

## Script 2: Analyzing a Survey

In this script we are GIS Analysts tasked with interpreting the results of a survey for a humanitarian organization in Kenya. In this hypothetical situation, we are given the results of a survey in the form of a .txt file, however, the file is improperly formated and contains a number of transcription errors. For the next two challenges, we write code that reads the results of the survey line by line using a for loop and uses multivariable assignment to assign the variables for `name` and `vote`. Additionally, to deal with the transcription errors we created a function to "munge" our data so that we remove all transcription errors and prepare the data for analysis.  

#### Challenge 1 
Our first challenge is to write a script that takes the county name as an input from the user and displays the number of votes that we cast for that county. To acheive this we use two functions. One is a function that "munges" our data the other counts the votes that match the user's input . `.upper` is used to standardize the user's input and make it consistent with the format of our "munged" data. An if statement is used to count all the votes that match the county name from the user's input. The end result is printed after the for loop iterates through the entirety of the survey. 

#### Challenge 2
Our second challenge is to write a script that includes 3 functions for "munging" our data, checking for duplicate votes, and counting the votes for each county. As a bonus, we incude code that prints a statement identifying the county with the most votes. This is acheived by calling each of the three functions described above within a for loop that iterates through the entirety of the survey. 

At first, we were quickly able to write a code that created the desired output. However, the code we wrote was only one function and we found it difficult to seperate the code into the 3 funtions. The main issue was that our "munging" function was not reassigning the variables for `name` and `vote` as we had intended. After reading about "Global Variables" in [Chapter 11 of the Think Python textbook](http://greenteapress.com/thinkpython2/html/thinkpython2012.html) we realized that the reason our "munging" function was not working was because we were reassigning our `name` and `vote` variables locally inside the function and they would disapear after the function finished running. Once we made the `name` and `vote` variables global variables, our script worked perfectly with our 3 functions.

See the code for script 2 in the attached  `.ipynb` file entitled `302Final_script2`. 
