# httpserver

##### _A Multithreaded HTTP server, with logging and healthcheck functionality_
 
1) To build program, enter "make" in the command line. This will build the "httpserver" executable.
2) Program will still take a port number as a parameter, but this time it will also have two optional parameters defining the number of threads and the name of the log file to hold the contents of logging. Optional parameters can appear in any order
   - ./httpserver 8080 -N 4 -l log_file
   - ./httpserver -N 6 1234 
   - ./httpserver 8010 -l other_log
   - ./httpserver 3030

3) In another terminal, enter a GET or PUT request using curl. 
    - For example, for GET, enter: `curl http://localhost:8080/filename`
    - For PUT, enter: `curl -T localfile.txt http://localhost:8080/filename` 
    - For HEAD, enter: `curl -I http://localhost:8080/filename`
    - The request target must be a 27 ASCII characters. 

IMPORTANT: This binary was compiled using gcc in the course required environment. So this may not work if you are running this in an operating system other than Ubuntu 18.04

