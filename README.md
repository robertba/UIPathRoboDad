# UIPathRoboDad
You can use this UIPath project in your household to monitor Netflix consumption in near real-time and learn if kids are "sneak watching" without you knowing.  The alerts are configurable and customizable.  This process requires a working Netflix account with a profile. It requires the Chrome browser and unless the email process is changed, a valid Gmail account that is set with mail forwarding functionality enabled. It requires a connection to Orchestrator which contains stored credentials.

## Approach
The process works by first downloading a baseline Netflix viewing history.  As soon as someone watches something in Netflix (even for one second), the viewing history is updated by Netflix.  The process takes advantage of this by continuing to download the viewing history in an infinite loop at a configurable interval.  This updated viewing history is then compared to the baseline viewing history.  If it differs, the process knows someone has watched Netflix.
When Netflix has been watched, the process will notify the executor in one of four configurable ways.  This includes email, text message (which uses email as a means to send the message), text to speech (voice on the computer on which the process is running), and/or a google home device that's setup to cast to from the Chrome browser. 
The process ends (exists it's infinite loop) once someone has been "caught" watching Netflix or the executor of the process decides to stop it.

## Requirements
A working Netflix Account, UIPath Studio, UIPath Robot, access to a UIPath Orchestrator Instance with valid Netflix Credentials, for email and text message support access to a Gmail account with credentials and email forwarding support turned on, Microsoft Excel

## Documentation
The documentation is found in the root directory of the project:  https://github.com/robertba/UIPathRoboDad/blob/master/UIPathRoboDad_docs.pdf
