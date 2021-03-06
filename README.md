
# COSC490GUI
## Overview
This research project focuses on how to automate usability testing and the challenges that surround this. It's a cross-platform, web scraping tool that will test if any given website is usable and provide feedback for improvements. This tool is to help agile development teams better integrate usability testing. It was created by 6 Towson University students for their software practicum class. The students are Kristen Thesing, Jose De La Rosa, Heiu Dinh, Daniel Thompson, James Lohr and Kyara Pugh. They worked with MITRE usabilty testers and engineers to create a deliverable software product for the InSure Spring 2020 project. 

## Getting Started
### Requirements  
- Node.js, to install packages required by our front-end GUI, powered by Electron
- Python3, used for packages, to write our tests and control Selenium WebDriver
- Chrome, as the browser of choice to test Web-Apps
- ChromeDriver, a tool provided by [google.com](https://sites.google.com/a/chromium.org/chromedriver/home "ChromeDriver Documentation"), used by Selenium WebDriver to control Chrome. 

### Installing ChromeDriver 

Your required version of ChromeDriver is dependent on your version of Chrome.  
**(Currently supporting up to Chrome version 81)**  

To determine your version of Chrome:
1. Click the Menu Icon in the upper-right corner.  
2. Click Help> About Google Chrome.  

To download the ChromeDriver binary for your platform and operating system, visit:  
https://sites.google.com/a/chromium.org/chromedriver/downloads  

As indicated in the [setup](https://sites.google.com/a/chromium.org/chromedriver/getting-started) instructions, you can:
1. Include the ChromeDriver location in your PATH environment variable.
  * (Linux) In terminal: 
    ```
    sudo mv chromedriver /usr/bin/chromedriver
    sudo chown root:root /usr/bin/chromedriver
    sudo chmod +x /usr/bin/chromedriver
    ```
2. Provide the path to ChromeDriver when instantiating webdriver.Chrome().
   * *in py/api.py*
3. *To Be Implemented: provide path to GUI*

### Installing The Project

1. To install the required front-end dependencies:  
   * Open a terminal.
   * CD into the electron/ directory.
   * Enter the command `npm install`
2. To install the required back-end packages:   
   * Open a terminal.
   * CD into the py/ directory.
   * (Recommended) Start or Create and Start a python virtual environment.
   * Install packages for your Operating system
      * (Win) `pip3 install -r win_requirements.txt`
      * (Mac) `pip3 install -r osx_requirements.txt`
      * (Linux) `pip3 install -r lin_requirements.txt`
3. To run: 
    Flask server:
    * In py/ directory: 
      Enter command `py api.py` or `python3 api.py`
    Electron GUI:
    * In eletron/ directory: 
      Enter command `npm start`
   
### Troubleshooting
* If errors occur with nltk when running Check page text, you may need to install nltk data  
  * In py/ directory:
    ```
    python3
    import nltk
    nltk.download('punkt')
    ```
    
## References

For help with Selenium WebDriver refer to:  
https://www.selenium.dev/documentation/en/getting_started/  
or for more detailed docs:  
https://selenium-python.readthedocs.io/index.html
