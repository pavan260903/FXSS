# FXSS
FXSS: Uncovered web app vulnerabilities enabling malicious code injection, posing security threats, data breaches, and compromising user safety.
#installation
python3 main.py -f <filename> -o <output>

-f: Filename that contains bunch of links
-o: Output filename in which all the vulnerable endpoints is stored
-t: No of threads[Increase the threads if you want more speed] (Max: 10)
-u: Single URL to scan.
-H: Custom Headers.(PLease use , within "" to add multiple headers)

Using  multiple  headers:
python3 main.py -f urls.txt -H "Cookies:test=123;id=asdasd, User-Agent: Mozilla/Firefox" -t 7 -o result.txt

Using  single  header:
python3 main.py -f urls.txt -H "Cookies:test=123;id=asdasd" -t 7 -o result.txt

Scanning single URL:
python3 main.py -u http://example.com/hpp/?pp=12 -o out.txt

Detect waf & scan:
python3 main.py -u http://example.com/hpp/?pp=12 -o out.txt --waf

Specify waf manually:

python3 main.py -u http://example.com/hpp/?pp=12 -o out.txt -w cloudflare

Using PIPE

cat katana.txt | python3 main.py --pipe -t 7
