# Mailer  
Mailer using multiple gmail accounts.  

Step 1: Turn on the Gmail API  

&nbsp a. Use this wizard(https://console.developers.google.com/flows/enableapi?apiid=gmail) to create or select a project in the Google Developers Console and automatically turn on the API. Click the Go to credentials button to continue.  
&nbsp b. At the top of the page, select the OAuth consent screen tab. Select an Email address, enter a Product name if not already set, and click the Save button.  
&nbsp c. Back on the Credentials tab, click the Add credentials button and select OAuth 2.0 client ID.  
&nbsp d. Select the application type Other and click the Create button.  
&nbsp e. Click OK to dismiss the resulting dialog.  
&nbsp f. Click the  (Download JSON) button to the right of the client ID.  
&nbsp g. Move this file to your working directory and rename it client_secret.json.  

Step 2: Login all your accounts in you default browser.  

Step 3: Make sure that you contacts sheet is in suppored format. (xlsx).   
&nbsp a. If you have names and emails, make sure that names are in 1st column, and email in 2nd column  
&nbsp b. If you don't have names in contacts list, then remove any other column from the sheet. max_column of sheet must be 1.  
&nbsp c. Make sure that your desired sheet is the active sheet.  

Step 4: Change the parameters in msg.py according to your needs :  
&nbsp a) count : Number of gmail accounts to be used for mailing.  
&nbsp b) limit : Limit on number of emails to be sent from one gmail account.  
&nbsp c) excel : path to excel sheet of contacts  
&nbsp d) subject : subject of mails  
&nbsp e) salutation :   
     &nbsp&nbsp Case 1: Names are present in contact list  
            'Dear <name>' : <name> will be replaced with values of name in excel sheet.  
     &nbsp&nbsp Case 2: Names are not present in contact list  
            'Respected Sir' or 'Dear Student' etc.  
&nbsp f) msg : message to be sent  
     &nbsp&nbsp i.  '\n' for next line  
     &nbsp&nbsp ii.  \ for line wrapping in code for easy understanding  
     &nbsp&nbsp iii. you can use link as it is, it will appear as hyperlink in gmail.  

Step 5: Run program by typing 'python mailer.py' in terminal.  
