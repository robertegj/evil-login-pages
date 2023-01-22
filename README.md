there are no tracking scripts inlcuded - this is:  
### a purely static recreation of common logins

# try it out
- [Amazon Login](https://robertegj.github.io/evil-login-pages/Amazon/login.html)
- [Google Login](https://robertegj.github.io/evil-login-pages/Amazon/login.html)
- [GitLab Login](https://robertegj.github.io/evil-login-pages/Amazon/login.html)

# evil login pages
a collection of look-alike logins and other "official" things that can easily be spoofed

# why do this?
awareness.  
the first reaction i had when I showed these logins to someone:  
> That's scary  
> --Someone

this repo was put together in less than an hour - it's really easy to "spoof" a login page.  
i created this to demonstrate that.  

this is **absolutely not** an original idea.  
in fact, some phishing tools (that come preinstalled in Kali!) actually have **built in** email templates for common providers.  

this is not that.  
this is strictly for educational purposes.  

# how i did it

Right click the login page, save page as .html  
wget -E -H -k -K -p that_page.html  


sometimes use this:
```
with (window.open("")) {
    document.open("text/html");
    document.write("<!--\n"); //for live version delete this line
    document.write(opener.document.documentElement.outerHTML.replace(/</g,"<").replace(/>/g, ">"));
    document.write("\n//-->"); //for live version delete this line
    document.close();
    document.title = "DOM Snapshot:" + opener.document.title;
    focus();
}
```
# todo
- add more emails
- add more links to readme
