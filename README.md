Download Link: https://assignmentchef.com/product/solved-cse598-project-3
<br>
The aim of this project is to make sure that you have read the slides and the text and have understood the concepts covered in the lectures and in the text, including messaging, caching, and VIPLE. By the end of the assignment, you should have a good understanding of the concepts and have applied these concepts in developing operational programs.

<h1>Practice Exercises and Preparation</h1>

<ol>

 <li>Reading: Textbook Chapters 4 and 5.4.2 on XML file operations, Chapter 9 and Appendix B on IoT and VIPLE.</li>

 <li>Practice exercises: Questions at the end of Chapters 8. Complete the multiple choice questions. The solution is available in the course web page.</li>

 <li>Practice exercises: Questions at the end of Chapters 9. Complete the multiple choice questions. The solution is available in the course web page.</li>

 <li>Follow Lecture 2-8 to implement a Website with caching.</li>

 <li>Read Text Chapter 9 and download VIPLE (http://neptune.fulton.ad.asu.edu/VIPLE/) to develop workflow programs for robotics applications.</li>

 <li>Follow Text Chapter 9 and Appendix B. Implement different applications using finite state machines.</li>

 <li>Follow the tutorial to run the drive-by-wire program using the Unity simulator. Note, in order to start you program, you need to:

  <ul>

   <li>After you started the Unity Simulator, you need to go back to VIPLE, to click the</li>

  </ul></li>

</ol>

“Start” button”, the green arrow. Then, the Control window will appear, showing that the robot is running.

<ul>

 <li>When you are controlling the robot using the keyboard, you must keep the Control window on the top in active, not in background.</li>

</ul>




<h1>Assignment 5: Messaging</h1>




Create a simplified messaging service to buffer messages in an XML file and a Web client to allow users to send and receive messages. You will develop your service and application on IIS Express localhost.

<ul>

 <li>Messaging service: Develop a service (WSDL service, RESTful service, or Workflow service) that can buffer messages before the receivers fetch the messages. The messages must be saved in an XML file (or JSON file) that the service can access. The service must offer the following operations. You may</li>

</ul>

add more parameters for additional functions.                                                                                    [25]

<ul>

 <li>Operation 1: sendMsg: It allows the client to send a string message to the messaging service, and the message will be stored in the database (XML file) with senderID, receiverID, and a time stamp.</li>

</ul>

Inputs: string senderID, string receiverID, string msg.

Output: void

Note: a timestamp will be added by the program.

<ul>

 <li>Operation 2: receiveMsg: It allows the client to receive all the messages send to the receiverID.</li>

</ul>

Inputs: string receiverID, boolean purge

Output: string[] an array of messages, with each element containing the related information: senderID, sending time, and message.

Note: The receiver should receive the new messages that have not been received in the previous receive call. If purge == true, the service will delete all messages of the receiver.

To read and write an XML file on disk, you may want to read text Chapter 4 on XML processing and

Section 5.4.2 on reading and writing XML files. You may also read Text Chapter 10 and using LINQ to XML methods.

<ul>

 <li>MsgApp: Develop a Web application (client) in ASP .Net or MVC that contains at least two Web pages: Sender page and Receiver page. The sender sends messages to the Messaging service and the receiver receives messages from the service. A sample GUI is shown below. The GUI must link to all components that need to be implemented. You can add additional items in your GUI. [25]</li>

</ul>




To test your clients (sender and receiver) on localhost/IIS Express: Right click the service project and choose View in Browser to run the service. Then, start the client, which will open another bowser window to run the client. Copy and paste the URL into a new browser window. Now, you have three sessions of your application: one service session and two client sessions. You can test your application by sending a message in one browser and receiving the message in another browser. Submit a screenshot of your testing.







Submission: You can put the service and the client in one solution or in two separate solutions. You must place all the files into one folder and zip the folder for submission. Make sure that your solution and project can run on TA’s computer.

<h1>Assignment 6: IoT Application Composition and Integration</h1>

Due: March 28, 2020 by 11:59pm (Arizona Time)

Before you start this part of the assignment, you need to follow the lecture slides and the tutorial in Text Appendix B and Chapter 9 to get started with programming in VIPLE workflow.

<ul>

 <li>An ASCII code consists of 7 bits of 0s or 1s. The 8<sup>th</sup> bit is often generated for parity checking. Write a</li>

</ul>

VIPLE application to generate the even-parity bit for an ASCII code.

<ul>

 <li>Use the keypress event to enter a string of seven 0s and 1s. The VIPLE diagram counts the number of 1s entered. After seven digits are entered, it outputs the string of eight digits, with the eighth digit to be 1 if the number of 1s entered is an odd number. Otherwise, the eighth digit will be 0. Use Print Line</li>

</ul>

to print the entire eight digits.                                                                                                                [5]

<ul>

 <li>Use a WSDL service or a RESTful service (for example, in ASU Repository) to encrypt the eight-digit value generated in the previous question, save the encrypted value into a variable, and use Print Line</li>

</ul>

to print the encrypted string.                                                                                                                  [5]

<ul>

 <li>Write a code activity to read the encrypted value and decrypt the value by calling the corresponding decryption service. You can use either a WSDL service or a RESTful service in this question. [5]</li>

 <li>Generate a random binary number of 7 bits, instead of entering via keyboard. Use the activities in the previous questions (1.2 and 1.3) to process the number. Put these steps in a loop and iterate the steps</li>

</ul>

for N time, where you can set N = 10.                                                                                                   [5]

Submission: The VIPLE code for questions 1.1, 1.2, 1.3, and 1.4.

<ul>

 <li>Robot maze navigation using VIPLE and an HTML5 simulator: Web 2D simulator. Configure your devices following these diagrams.</li>

</ul>

Read the instructions on the web page to configure the simulator. Note, you need to change the right wall to left wall!

On the VIPLE side, you need to configure your devices to match with what you have configured on the Web simulator side.

Your tasks are to implement the <strong>left</strong>-wall-following program. You can follow the textbook Section

9.5.4. Note, the book shows the sample code for the <strong>right</strong>-wall-following program.

Submission: The code for question 2.

Put all the codes in all questions in one folder, zip the folder, and submit the zip file.