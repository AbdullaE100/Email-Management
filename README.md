# Email-Management
This project demonstrates the power of C++ as a programming language, showcasing how foundational programming constructs can be applied to build a meaningful and engaging application. The Email Management System serves as both an exercise in OOP and data structure utilization and as a step toward developing more complex applications. 


Table of Contents
Project Report: Email Management System	1
Project Structure The project is organized into multiple files and folders, as shown below:	1
Class Descriptions	2
Functionality Overview	3
Project Execution	3
Summary	4


Project Report: Email Management System
The Email Management System is a C++ application to simulate email storage and retrieval for several users. It provides inboxes, outboxes, and trash for each user so they can view their emails and organize them. This system takes advantage of object-oriented principles with classes and data structures, including stacks, queues, and maps, for the core structure of this system.
Project Structure The project is organized into multiple files and folders, as shown below:
Header Files (.h):
•	Email.h: Defines the Email class, which represents a single email entity comprising fields like sender, receiver, subject, and content.
•	EmailManager.h: Declares the EmailManager class, whose role is to manage emails.
•	User.h: Declares the User class, representing individual users by their email addresses and folders (inbox, outbox, trash).
•	Queue.h and Stack.h: Provide generic Queue and Stack templates for handling email collections.
•	Utility.h: Defines the checkCondition function, used for validating user input.
Source Files (.cpp):
•	main.cpp: Acts as the main entry point for the application, handling user interactions and facilitating access to various system functionalities.
•	Email.cpp, EmailManager.cpp, and User.cpp: Implement functionality for the respective classes.
•	Queue.cpp and Stack.cpp: Define queue and stack operations for managing email collections.
•	Utility.cpp: Implements the checkCondition function, which validates user input, ensuring it falls within defined bounds.
Supporting Files:
•	global.txt: A file that loads predefined email data, allowing the system to be initialized with sample emails.
Class Descriptions
Email:
•	Attributes: subject, content, sender, receiver.
•	Methods: Getters and setters for each attribute to allow access and modification of email details.
User:
•	Attributes: User’s email address (email), and three Stack objects representing the inbox, outbox, and trashcan.
•	Methods: Functions to set and retrieve the user's email, along with functions to get or set each folder.
EmailManager:
•	Attributes: stack (where we manage stack operations) and utility functions to check for spam.
•	Methods:
o	isSpam: Checks if an email contains keywords typically associated with spam.
o	saveEmail: Saves an email to a specified folder (Inbox, Outbox, or Trash).
o	viewEmails: Allows the user to view emails in a specific folder.
o	parseEmail: Extracts the username portion from an email address.
Data Structures:
•	Stack: Used for inbox, outbox, and trashcan folders, enabling LIFO (Last In, First Out) access.
•	Queue: Not currently utilized in the project but available for future enhancements, such as queued email sending.
•	Map: Used to manage users and their respective email data.
Utility Functions
•	checkCondition: Ensures user input is within specified limits. This function is called frequently (e.g., in menu selections) to provide robust input handling.
Functionality Overview
User Management:
•	Users are initialized based on email data from global.txt. If a user is not already in the system, they are added and initialized with empty inboxes, outboxes, and trash folders.
Email Management:
•	Save Email: Supports saving emails into a user’s folder (Inbox, Outbox, or Trash) based on specific conditions.
•	View Email: Users can view summaries of emails in their folders and read full content upon request. The program prompts users to select the email index they wish to view, providing an intuitive interface.
Spam Detection:
•	Emails containing certain keywords (e.g., "win", "free", "urgent") are automatically directed to the trashcan.
Input Validation:
•	The checkCondition function is used to ensure that all menu selections and email viewing actions are within valid bounds, improving the user experience by gracefully handling invalid inputs.
Project Execution
To execute this project:
1.	Ensure all .cpp and .h source files are in the same directory.
2.	Compile the project using the provided CMakeLists.txt file, or use a command like:

g++ -std=c++17 -g main.cpp Email.cpp EmailManager.cpp User.cpp Queue.cpp Map.cpp -o EmailSystem

if mac osX: 
./EmailSystem
On Windows
 EmailSystem.exe
DEMO:
 

Summary
The Email Management System is a robust and user-friendly C++ application that emulates a basic email management interface. It provides accessible email folders (Inbox, Outbox, Trash) for users, enabling basic operations such as reading email information, organizing emails into folders, and handling spam. Built upon well-organized classes and diverse data structures, this system efficiently stores, organizes, and retrieves email data.
This project demonstrates key C++ concepts, including:
•	Object-Oriented Design: The system leverages classes to encapsulate email and user data, using stacks and queues to manage these efficiently. Core functionalities such as Email, User, and EmailManager are encapsulated in specialized classes, making the code modular, maintainable, and scalable.
•	Data Structures: Carefully chosen data structures enhance the program's functionality and performance. The LIFO (Last In, First Out) stack structure is ideal for managing the inbox and outbox, as it mirrors the behavior of real-world email clients where the most recent emails are accessed first. Additionally, the Map structure enables efficient lookup and retrieval of user information, facilitating a seamless user experience.
•	Spam Filtering: The built-in spam filtering feature detects and categorizes emails containing specific keywords (e.g., "win," "free," "urgent") as spam, automatically moving them to the trash. This real-world feature reduces clutter, keeping the inbox focused on important messages.
•	File Handling: Initial user email data is loaded from a text file (global.txt), which mimics persistent storage and initializes users and their email history. The program also writes email data to user-specific files, allowing data to be retained between sessions. This demonstrates practical file handling and data persistence in C++.
•	User Interface and Input Validation: Users can interact with the application via an interactive console-based interface to view emails, navigate folders, and see specific email content. The checkCondition function validates all user inputs within defined boundaries, enhancing the robustness and reliability of the application by preventing errors from invalid inputs.
The Email Management System showcases a solid understanding of C++ and core programming principles, providing a foundation for future enhancements. Potential improvements include:
•	Email Deletion and Restoration: Adding the ability for users to permanently delete emails from the trash or restore them to the inbox would enhance user control over email content.
•	Search Functionality: Implementing a search feature would allow users to locate specific emails quickly by entering keywords from the subject, sender, or content.
•	Sorting and Filtering Options: Additional sorting options (by date, sender, subject) and filtering capabilities (e.g., unread, flagged) could streamline email retrieval and improve usability.
•	Sending and Receiving Emails: Expanding the application to simulate sending and receiving emails would turn it into a fully functional email client. This could involve network programming or integration with external email APIs.
•	Enhanced Security Features: Adding user authentication, data encryption, and machine learning-based spam filtering would increase the project's practicality and relevance in a real-world context.
This project demonstrates the power of C++ as a programming language, showcasing how foundational programming constructs can be applied to build a meaningful and engaging application. The Email Management System serves as both an exercise in OOP and data structure utilization and as a step toward developing more complex applications. The project underscores the importance of designing flexible, modular, and scalable code, which is valuable in both academic and professional programming environments.
