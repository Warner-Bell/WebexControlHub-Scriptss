# webexControlHubScripts
Scripts utilizing the Cisco Webex Control Hub APIs

Filename | Language | Description
--- | --- | ---
BulkDeleteUsers.py | Python | Script to bulk delete users from a Control Hub org
DownloadRecordings.py | Python | Script to bulk download Recordings from a Control Hub org


1 	Sign in to Control Hub.
2 	Export your users into a CSV file.

You may need more than one CSV file if you have a large organization. See Ways to Add and Manage Users in Cisco Webex Control Hub.
3 	Save the CSV files to the computer where you're running the script.
4 	Open the CSV files for editing, and remove the rows that contain the users you want to keep.

You will be asked by the script to confirm the deletion of the users, so you can cancel if you make a mistake here. You could go back to Control Hub at that point and export (remaining) users into fresh CSV files.
5 	Run the script. For example, at your shell enter python BulkDeleteUsers.py.
6 	Enter the full path and name of your CSV file, when prompted. For example, ~/Downloads/exported_users.csv.

The script prompts you to enter your access token, so it can check whether the token is still valid to authenticate you.
7 	Enter your access token.

The script does a dry run, returns a count of users it will delete, and asks you to confirm that you want to delete N users.

If there are any errors, it could be that the user IDs are corrupted in the CSV files.
8 	Confirm that you want to delete the users.

The API calls required to delete each user take about two to three seconds, so you can expect the script to run for about five minutes when your CSV file has 100 users.

The script writes any errors to a CSV file in the same directory as the input files.
9 	Repeat this process if you have more than one CSV file.
