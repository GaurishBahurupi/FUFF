# Directory Enumeration/Bursting with FFUF

In penetration testing and web application security assessments, directory enumeration (also known as directory bursting) is a crucial phase for identifying hidden directories and files on a target web server. FFUF (Fuzz Faster U Fool) is a powerful and flexible tool commonly used for this purpose. This article provides an in-depth explanation of the FFUF command and its components, along with additional FFUF commands frequently used in directory enumeration.

## Understanding the FFUF Command

The basic FFUF command for directory enumeration is as follows:

```bash
ffuf -u https://hackycorp.com/FUZZ -w /home/gaurish/Downloads/common.txt
```
Let's break down each component of this command:

- `ffuf`: This is the command to execute FFUF.
- `-u`: This flag specifies the target URL to fuzz. In this case, we're targeting `https://hackycorp.com/`, and the part of the URL that we want to brute force is represented by the keyword `FUZZ`.
- `-w`: This flag specifies the wordlist or dictionary file containing a list of directory and file names to try during the enumeration process. Here, `/home/gaurish/Downloads/common.txt` is the path to the wordlist file.
<img width="1440" alt="Screenshot 2024-03-22 at 11 18 17 PM" src="https://github.com/gaurish303/FUFF/assets/139263378/a5c7d902-0857-435d-a951-1db7aaf745ce">

### Additional FFUF Commands

While the basic command above is sufficient for many directory enumeration tasks, FFUF offers additional commands that can enhance the enumeration process. Here are some commonly used commands:

- `-e`: This flag specifies the extensions to append to the wordlist entries. For example, `-e .php,.html,.txt` would try each entry with `.php`, `.html`, and `.txt` extensions.
- `-recursion`: This flag enables recursive directory scanning, allowing FFUF to search for directories within directories.
- `-recursion-depth`: This flag specifies the maximum recursion depth for directory scanning.
- `-t`: This flag specifies the number of concurrent threads to use during the enumeration process, increasing the speed of the scan.
- `-maxtime`: This flag specifies the maximum time (in seconds) to spend on each request.
- `-o`: This flag specifies the output file to save the results of the enumeration.

### Conclusion

Directory enumeration with FFUF is a fundamental aspect of web application security testing. By using the FFUF command with appropriate parameters and wordlists, testers can efficiently discover hidden directories and files, potentially uncovering security vulnerabilities and improving the overall security posture of the target web server.

