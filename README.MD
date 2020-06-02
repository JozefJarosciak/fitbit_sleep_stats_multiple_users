# Retrieval of Sleep-Related Data from Fitbit Accounts of Multiple Users

##########################################################################

Date: May 2020

Author: Jozef Jarosciak - jozef@jarosciak.com - https://joe0.com

Licensing: MIT license

##########################################################################

# Requirements:
- Installed **Google Chrome vs 83**+
- **chromedriver.exe** in the program's folder (one packaged with the code is for Chrome 83+)
- Writable subfolder 'export-patients' in the program's root
- **list-of-patients.json** - this file contains the list of patients in JSON format:
    - Specify the first name, last name of each of the users (patients)
    - Specify the web login name and password of each patient (this is the user name and password user uses to login to Fitbit)
    - The data range for which to extract the sleep patterns (start and end date)
- Python Libraries: **json5==0.8.5, requests==2.22.0 and selenium==3.141.0** web driver. If it doesn't work just run 'pip3 install -r requirements.txt' in your shell

# How to Run:
- Tested on Windows 10 only (but the code should be OS agnostic)
- Run the code: `python3 process-patients.py`

# Results:
- Once the code has processed all patients entered into the list-of-patients.json file, it'll place results in JSON format to 'export-patients' subfolder  
- Resulting files will be named in this format:

	**FirstName-LastName__StartDate-to-EndDate.json** 
	
	e.g. Camila-Koike__2020-05-06-to-2020-05-12.json

# Issues:
- The code is currently as is, I did not have the time to code in the proper handling of exceptions and debug it.
- The risk of errors is high, especially if the credentials for users are not correctly typed into list-of-patients.json

# Licensing: MIT license

Copyright (c) <2020> <Jozef Jarosciak - jozef@jarosciak.com - https://joe0.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.