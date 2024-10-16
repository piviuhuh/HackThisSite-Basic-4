# HackThisSite - Basic 4
## Description
An email script has been set up, which sends the password to the administrator. Requirements: HTML knowledge, an email address

We will be doing Basic 4 from HackThisSite
https://www.hackthissite.org/missions/basic/4/

## Solution
Upon accessing the challenge page, we observe:

`This time Sam hardcoded the password into the script. However, the password is long and complex, and Sam is often forgetful. So he wrote a script that would email his password to him automatically in case he forgot. Here is the script:`

With that information, let’s check the source code for anything useful.

Upon examining the webpage's source code, we were able to identify Sam's email address. When we clicked the 'Send password to Sam' button, a message appeared indicating that a password reminder had been successfully dispatched.
By utilizing Burp Suite, we can intercept the network traffic, modify the email address field to replace Sam's with ours, and then forward the modified request to obtain the password.

### Steps

1. Launch Burp Suite and turn intercept on.
2. If you press the 'Send password to Sam' button, you'll notice that Burp successfully intercepts the request, demonstrating its ability to capture network traffic.
3. Alter the email address field to replace Sam's with your own, and then deactivate the interception feature.

Upon revisiting our browser, we observe that the password reminder has been successfully delivered to our email inbox.
For the password reminder to be effective, you must use the email address associated with your HackThisSite account.

I appreciate you taking the time to review my write-up. If you have any inquiries or comments, please feel free to reach out. See you on the next challenge.








