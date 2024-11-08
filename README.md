# The Optimal Suitcase Organizer

**Pack-It** is an intelligent suitcase organization application that helps users efficiently pack their suitcases by suggesting optimal item placements, folding methods, and estimated weights and volumes. Using advanced AI technology and online search capabilities, **Pack-It** minimizes the need for user input by automatically fetching dimensions and weight estimates for items.

## Features
- **Automatic Item Dimension & Weight Fetching**: Searches the web to gather item dimensions and weights based on minimal user input.
- **User Confirmation**: Prompts users to confirm fetched data, allowing them to refine the search if necessary.
- **Optimal Packing Suggestions**: Recommends where to place each item in the suitcase and how to fold it for maximum space utilization.
- **Total Space & Weight Calculation**: Calculates the total weight and remaining space in the suitcase after packing all items.
- **Professional User Interface**: Clean and user-friendly interface built with Tkinter.

## How It Works
1. **Web Search Integration**: Uses Google’s Custom Search API to fetch snippets about the item’s dimensions and weight based on the name provided by the user.
2. **AI-Powered Analysis**: Uses a Generative Language Model to analyze the search results and estimate the item's dimensions and weight.
3. **Packing Strategy**: Once all items are confirmed, the AI organizes them within the suitcase, calculates total space and weight, and suggests how to fold each item and where to place it.

## Requirements
- Python 3.6+
- API keys for Google Custom Search API and Google Generative Language Model API (Gemini)

## Installation
##### IMPORTANT!
In order to download this project, you must fill out a request form linked in the license of this repository. This is required by law!
1. #### Clone or download this repository.
2. #### Install the required Python packages:
```bash
pip install requests google-generativeai
```
3. ####  API Key Setup
The application utilizes two API keys and a search engine ID. The first key is for Gemini - Google's generative AI that is used to make decisions about the items and their placements. The second key is for a custom search engine that is used to search the web for the dimensions of the items. Lastly, the search engine ID is to identify the exact search engine being used in this project (the ```cx``` component). To add these keys, create a file called ```key.txt``` and paste the three keys in the file with this syntax:
```
<Gemini API Key>
<Google Custom Search API Key>
<Search Engine ID>
```

## Testing
Feel free to test your API keys by running the ```api_test.py``` application with the following command:
```bash
python test_api.py
```
This command should execute the testing script which searches the web for a topic and then feeds that information into Gemini. The language model then parses the information and provides the user with a summary. If this all goes well, then the ```key.txt``` file is perfectly initialized.

## Usage
Once all environmental factors have been properly established and set up, the command to run the main program is
```bash
python main.py
```
This command will start the program which is features a graphical user interface. Users are first prompted to enter the dimensions of their suitcase, and then they can add seperate items. The app will scour the web to find the dimensions of these items, so it's best if the user is as specific as possible (Ex. Lenovo IdeaPad Flex 5 instead of Laptop). The application will confirm the dimensions with the user before adding them to the list of items. Once all the items are added, the user is to press the button located towards the right to organize the suitcase. The list of items along with their dimensions are all thoughtfully processed to find the optimum way to place them, as well as an enumeration of detailed instructions on how to do so.
