This project sends emails for outreach
Email Generation Script

Overview

This Python script automates the process of generating and formatting outreach emails for different schools based on a given CSV file and an email template. The emails are personalized using placeholders replaced with actual data from the CSV file. The final emails are saved in a Word document (.docx) for easy review and sending.

Features

Reads a CSV file containing school names and contact email addresses.
Uses an email template with placeholders to generate personalized emails.
Groups email addresses by school and formats them accordingly.
Saves the generated emails to a Word document.

Input File Preparation 
    This code needs the email template and the list of school with emails, see STEM Teacher Research (MIDDLE).csv

Environment Setup
1. Install Visual Studio Code 
2. Create Github account
3. Sign into Github on Visual Studio Code
4. Download stempathize code from https://github.com/tr1sha-t/stempathize 
5. Move into /user/<username> e.g. /user/trisha-t
6. Ensure you have the following key files 
        stempathize_send_emails.py
        input/STEM Teacher Research (MIDDLE).csv
        README.md (this file)

7. Install brew 
8. Add brew to your PATH
9. Install Python
10. Add python to your PATH
11. Install/Update pip 
12. Run code

Dependencies (for this specific code)

The script requires the following Python libraries:

pandas for handling CSV files
python-docx for generating the Word document

Install the required libraries using:

pip install pandas python-docx

How It Works

CSV Input: The script reads a CSV file that contains at least two columns:

"School Name": The name of the school

"Contact Email Address": The email addresses of school contacts.

Processing:

Filters out any missing data.

Groups email addresses by school.

Personalizes email content using placeholders such as:

{school name} -> Full school name.
[insert FULL name] -> Sender's name.
[insert beginning of school name] -> Shortened school name.
[insert program name] -> Name of the program being promoted.

Output:

The script generates a list of formatted emails.

Saves the emails into a .docx file.

Usage

Parameters

file_path: Path to the input CSV file.
email_template: Dictionary containing the email subject and body with placeholders.
sender_name: The name of the sender to replace in the template.
program_name: The name of the program to include in the email.
output_file: Name of the output .docx file where the emails are stored.

Running the Script

Update the parameters in the script and run:

python script.py

Example Email Template

Subject:

Please Share For {school_name} Students: Build a Mind-Blowing Project! | STEMpathize

Body:

Hello {school name} Team,

I’d like to follow up on the previous email regarding STEMpathize’s [insert program name] for [insert beginning of school name] students. I would love to further discuss our programs or how students can get involved with STEMpathize.

Thank you for your time, and I look forward to hearing back.

Best regards,
[insert FULL name]
Outreach Team | STEMpathize

Output

The script generates a Word document containing emails formatted as:

To: email1@example.com, email2@example.com
Subject: Please Share For ABC High School Students: Build a Mind-Blowing Project! | STEMpathize

Hello ABC High School Team,

I’d like to follow up on the previous email regarding STEMpathize’s Saturday Workshop Series for ABC students. I would love to further discuss our programs or how students can get involved with STEMpathize.

Thank you for your time, and I look forward to hearing back.

Best regards,
Trisha Thyagarajan
Outreach Team | STEMpathize

Notes

Ensure the CSV file is correctly formatted with appropriate column headers.

If running into issues, verify that all required Python packages are installed.

Modify the email_template dictionary to customize the email content as needed.

License

This script is provided for educational and outreach purposes. Feel free to modify and use it according to your needs.