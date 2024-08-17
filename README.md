# File Integrity Monitoring System

This Python script monitors file changes in a specified directory using the watchdog library. It logs modifications, creations, deletions, and movements of files for tracking changes to file contents.

# Features
1. Real-time Monitoring: Watches for file system events such as modifications, creations, deletions, and movements.<br>
2. Flexible Path Specification: Allows the user to specify the directory to monitor via command-line arguments, with a default to the current directory.<br>

# Installation
Ensure you have Python 3 installed. You need to install the watchdog library if it’s not already available.<br> 

You can install it using pip:<br>
pip install watchdog<br>
python3 app.py /path/to/directory<br>

If you do not provide a path, use:<br>
python3 app.py<br>
This command will monitor the current directory.<br>

# How It Works
-> Import Libraries: Imports necessary modules including sys, time, hashlib, logging, and watchdog.<br>
-> Configuration: Sets up logging with a specific format to display timestamps, process IDs, log levels, and messages.<br>
-> Event Handling: Custom event handler logs file changes.<br>
-> Observer Setup: Initializes and starts a watchdog observer to watch for file system events in the specified directory.<br>

# Log Output

The script logs the following events:<br>

File Created: Logs when a new file is created, including the file’s hash.<br>
File Modified: Logs when a file is modified, including the updated file’s hash.<br>
File Deleted: Logs when a file is deleted.<br>
File Moved: Logs when a file is moved from one location to another.<br>
Logs are output to the terminal, providing real-time updates on file system changes.<br>

Example-

Here’s an example of how the script logs events:<br>
Copy code
2024-08-17 14:32:01 - 12345 - INFO - File created: /path/to/directory/example.txt<br>
2024-08-17 14:32:15 - 12345 - INFO - File modified: /path/to/directory/example.txt <br>
2024-08-17 14:33:20 - 12345 - INFO - File deleted: /path/to/directory/example.txt<br>

