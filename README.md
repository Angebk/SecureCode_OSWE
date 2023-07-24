# SecureCode_OSWE
As my first practice for the OSWE, I created this script as a test to automate various vulnerabilities and improve my skills in code analysis and white-box web hacking. If the script is helpful to you, you can support me with a star. It's not entirely perfect since it's the first script I've created.

Automation script to obtain a reverse shell on the Secure Code machine from Vulnhub
https://www.vulnhub.com/entry/securecode-1,651/

## Usage
Once the virtual machine is started, you should obtain its IP address. Replace the IP address in the script with the IP address of the virtual machine. Sometimes, the script may not behave optimally; if this is the case, replace the script's cookies with the cookies provided by the virtual machine. And there you have it, you will get your reverse shell.

At the end, it will ask for your IP and the port where you should listen using netcat `nc -lvnp <port>` . Don't forget to be in listening mode before sending the IP and Port. If you encounter any errors before running the script again, go to the machine's website and log out, as the script logs in automatically.

## Vulnerabilities
* (Authentication Bypass) Blind SQL injection that extract admin token, then abuse reset passord feature to login into admin account.
* (Remote code execution) Bypassing file uplaod with Content-Type "Header Validation" and bypass extension blacklists with .phar (PHP Archive extension).
