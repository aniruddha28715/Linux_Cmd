

<!-- =============================. CURL CALL EXTENTIONS .===================================>
<!-- 
1. Data & Method Extensions
These define how you talk to the server and what you send.
-->
-X	        --request	    Specifies the HTTP method (GET, POST, PUT, DELETE, etc.).
-d	        --data	        Sends data in a POST request (URL-encoded).
--data-raw		            Sends data exactly as written (prevents @ character processing).
-F	        --form	        Sends data as "multipart/form-data" (used for file uploads).
-G	        --get	        Forces the -d data to be appended to the URL as a query string.
-H	        --header	    Adds a custom header (e.g., -H "Content-Type: application/json").
-T	        --upload-file	Transfers a local file to the destination URL (common for FTP/PUT).


<!--
2. Output & File Management
These define where the server's response goes.
-->
-o	    --output	            Saves the output to a specific filename (e.g., -o result.txt).
-O	    --remote-name	        Saves the file using its original name from the URL.
-J	    --remote-header-name	Uses the server's Content-Disposition header for the filename.
-C	    --continue-at	        Resumes a transfer at a specific offset. Use -C - to auto-resume.
-r	    --range	                Fetches only a specific byte range (e.g., -r 0-499 for first 500 bytes).
-D	    --dump-header	        Saves the response headers to a specified file.


<!--
3. Visibility & Debugging
These control the "meta-information" shown in your terminal.
--> 
-v	    --verbose	            Shows the full "conversation" (request/response headers).
-i	    --include	            Shows the response headers followed by the body content.
-I	    --head	                Performs a HEAD request; shows only the headers, no body.
-s	    --silent	            Hides the progress meter and error messages.
-S	    --show-error	        When used with -s, it allows errors to still be printed.
-#	    --progress-bar	        Displays a simple # progress bar instead of the detailed table.
-w	    --write-out	            Formats and prints specific info (like % {http_code}) after completion.


<!-- 
4. Authentication & Security 
-->
-u	--user	Provides credentials in user:password format.
-k	--insecure	Allows connecting to SSL sites without valid/trusted certificates.
-E	--cert	Specifies a client certificate file for SSL/TLS.
-L	--location	Follows "301/302 Redirect" links automatically.
-x	--proxy	Routes the request through a proxy server (e.g., -x 127.0.0.1:8080).
--anyauth		Tells curl to figure out the most secure auth method automatically.


<!--
5. Advanced Session Control
-->
-b	--cookie	Sends a cookie string or reads cookies from a file.
-c	--cookie-jar	Saves all cookies from the session into a file.
-A	--user-agent	Sets a custom User-Agent string (to mimic a specific browser).
-e	--referer	Sets the "Referer Page" URL.
-m	--max-time	Sets a hard timeout for the entire operation (in seconds).
--connect-timeout		Sets a timeout only for the initial connection phase.
--limit-rate		Limits transfer speed (e.g., --limit-rate 100K).







