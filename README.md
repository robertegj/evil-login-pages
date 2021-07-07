# decoy-pages-and-logins
a collection of look-alike logins and other "official" things that can easily be spoofed

# links
- [AWS Login]()
- [Google Login]()

# process

Right click the page, save page as .html  
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
add emails
