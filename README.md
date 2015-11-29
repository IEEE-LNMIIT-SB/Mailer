# Mailer  
Mailer using multiple gmail accounts.  
Installation : pip install -r requirements.txt  
Step 1: Turn on the Gmail API  (POC members can skip this step, just drop me a mail, I will send you the required file)

  1. Use this wizard(https://console.developers.google.com/flows/enableapi?apiid=gmail) to create or select a project in the Google Developers Console and automatically turn on the API. Click the Go to credentials button to continue.  
  2. At the top of the page, select the OAuth consent screen tab. Select an Email address, enter a Product name if not already set, and click the Save button.  
  3. Back on the Credentials tab, click the Add credentials button and select OAuth 2.0 client ID.  
  4. Select the application type Other and click the Create button.  
  5. Click OK to dismiss the resulting dialog.  
  6. Click the  (Download JSON) button to the right of the client ID.  
  7. Move this file to your working directory and rename it client_secret.json.  

Step 2: Login all your accounts in you default browser.  

Step 3: Make sure that you contacts sheet is in suppored format. (xlsx).   
  1. If you have names and emails, make sure that names are in 1st column, and email in 2nd column  
  2. If you don't have names in contacts list, then remove any other column from the sheet. max_column of sheet must be 1.  
  3. Make sure that your desired sheet is the active sheet.  

Step 4: Change the parameters in msg.py according to your needs :  
  1. count : Number of gmail accounts to be used for mailing.  
  2. limit : Limit on number of emails to be sent from one gmail account.  
  3. excel : path to excel sheet of contacts  
  4. subject : subject of mails  
  5. salutation :   
    1. Case 1: Names are present in contact list  
            'Dear <name>' : <name> will be replaced with values of name in excel sheet.  
    2. Case 2: Names are not present in contact list  
            'Respected Sir' or 'Dear Student' etc.  
  5. msg : message to be sent  
    1.  '\n' for next line  
    2.   \ for line wrapping in code for easy understanding  
    3.   you can use link as it is, it will appear as hyperlink in gmail.  

Step 5: Run program by typing 'python mailer.py' in terminal.  
