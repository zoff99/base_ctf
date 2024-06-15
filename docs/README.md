
## Challenges

#### 01 linux i
* cd ~
* find a file that is the flag hidden in some directory
* use `ls -l` and `cd <dirname>` to find the filename flag
* practice: try `ls -l /home`

#### 02 linux ii
* cd ~
* use `ls --help` to find the hidden .dir directory(s)
* `cat file` reveals the flag

#### 03 linux iii
* run `cat` or `strings` on /tmp/.flag3
* pipe the output (`|`) to grep, ex. `cat file | grep FLAG`

#### 04 base64 encoded string
* Base64 decode the file /tmp/.flag4
* use `base64 --help`
* practice: try `echo YOURNAME | base64 | base64 -d`

#### 05 nothing

#### 06 linux v find a user id
* use `ps --help` to find the user of the `webserver` process
* using `id`, find the uid of user
* flag is the other user who belongs to that same group
* hint: look at /etc/group

#### 07 linux vi
* look in the ~www user's homedir to find the flag

#### 08 nothing

#### 09 visit a web service
* `curl localhost:8080`
* find an HTML comment tag which contains the flag
* https://www.w3schools.com/tags/

#### 10 web site 1
* `curl localhost:8080`
* look at the "cookies" being set by the server
* `curl --help` to find out which option turns on "Include protocol headers"
* Hint: The option you need is a single letter and rhymes with: Eye
* b64 decoder reveals flag

#### 11 web site 2
* `curl localhost:31337`
* look at the output

#### 12 unknown filetype
* cd ~
* find out what kind of filetype `oddfile` is
* `head -1 oddfile`
* http://www.garykessler.net/library/file_sigs.html
* or `file <file>`
* `unzip` and `cat` it to reveal the flag

#### 13 nmap to find a [local] hidden port
* `nmap localhost`
* flag is the service name for the listener port beginning with 3

#### 14 analyze a tcpdump
* cd ~
* examine the TCP Dump (Packet Capture) and find the flag
* `tcpdump -r flag.dmp`
* use the `-n` flag to not resolve hostnames
* use `-A` to display the data transferred
* look for the flag data being sent > 216.58.218.142.80
* if you can't scroll back add `| more` to the very end of your tcpdump command
* press `[SPACEBAR]` to advance, or `q` to exit from `more`.

#### 15 decode an encrypted message
* cd ~
* examine the file ce.txt
* flag is the number of the key used to decrypt the message

#### 16 just an ordinary image
* cd ~
* examine the image file pic.png

#### 17 discover a hidden code
* cd ~
* examine the file randomx.dat

#### 18 discover a hidden secret in an image
* cd ~
* examine the image file fl.png
* use `i2a/ascii-image-converter` to find the secret hidden in the image


#### check your result
* if you paste all your flags to take the SHA256 hash like this
* `echo 'FLAG1_12SECRECT2FLAG10_12.....' | sha256sum`
* you will get this secret code: `dcaba7f7976e180140e78b2d42e9b1a8521a7be9394dbf6c082161099cd0848a`

