This project is developed via wamp server .
we have included mail verification for the user . For that you have to setup 'sendmail' .
If you are using xampp server sendmail will be preinstall with that.
If you are using wamp server download and extract sendmail from http://www.glob.com.au/sendmail/sendmail.zip
1)place the sendmail folder in you wamp folder and configure the sendmail.ini as the following


smtp_server=smtp.gmail.com

; smtp port (normally 25)

smtp_port=465

; SMTPS (SSL) support
;   auto = use SSL for port 465, otherwise try to use TLS
;   ssl  = alway use SSL
;   tls  = always use TLS
;   none = never try to use SSL

smtp_ssl=ssl

default_domain=localhost <!-- (if you have differnt, domain enter your domain)  -->
; if your smtp server requires authentication, modify the following two lines

auth_username=<!-- your email id -->
auth_password=<!-- your email password -->




; sendmail will use your hostname and your default_domain in the ehlo/helo
; smtp greeting.  you can manually set the ehlo/helo name if required
hostname=localhost<!--  (if you are using different domain change hostname according to that) -->

note : 

2) configure your php.ini file in wamp/xampp as following 
i) search for [mail function] in your php.ini 
ii) Bellow that configure the file as following

; For Win32 only.
; http://php.net/smtp
; SMTP = localhost
; http://php.net/smtp-port
; smtp_port = 25

; For Win32 only.
; http://php.net/sendmail-from
; sendmail_from ="admin@wampserver.invalid"

; For Unix only.  You may supply arguments as well (default: "sendmail -t -i").
; http://php.net/sendmail-path
sendmail_path =<!-- "D:\wamp64\sendmail\sendmail.exe -t -i" (the path should be your sendmail.exe file's path)-->

iii) Restart your server .




