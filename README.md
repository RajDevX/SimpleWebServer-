# SimpleWebServer-
# Developing a Simple Webserver
## AIM:
To develop a simple webserver to display top 5 programming languages.

## DESIGN STEPS:
### Step 1: 
HTML content creation
### Step 2:
Design of webserver workflow
### Step 3:
Implementation using Python code
### Step 4:
Serving the HTML pages.
### Step 5:
Testing the webserver

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>TOP 5 PROGRAMMING LANGUAGES</title>
</head>
<body>
<h2>1. C++
C++ is a programming language that extends the C programming language. It's a programming language that combines features from both low-level and high-level languages. The bulk of CAD applications use C++ interfaces. Since mechanical engineering is more closely related to robotics and automation, mechanical engineers can use a programming language like C++.</h2>
<h2>2. Javascript
JavaScript is a well-known programming language on the internet. It's also known as the HTML programming language, and it's commonly used on the internet. JavaScript is an easy-to-learn programming language. In fact, it is less complicated than the majority of programming languages. Since HTML and CSS are the foundations of a beautiful website, web developers should learn this programming language as well.
</h2>
<h2>3. PHP
PHP is widely used for server-side web creation when a website requests information from a server on a regular basis. Since PHP is an older programming language, it has a large user community that has developed frameworks, libraries, and automation tools to make it easier to use. Debugging PHP code is also easy.
</h2>
<h2>4. Python
Python is a versatile software programming language that is ideal for writing scripts and is particularly useful in engineering projects for automating procedures. Python's key benefit is that it is easy to learn and understand compared to many other software programming languages. In a Python programme, you'd need about 5 times less code for any given function than you would in a Java or C++ programme. Although the precision of other languages is often needed, Python can help any project, from films to enterprise programmes, run more smoothly.
</h2>
<h2>5. Go
Go was developed by Google as an efficient, readable, and convenient system-level programming language. It's suitable for distributed systems, which are spread over many networks and must communicate by sending messages to each other. Despite being a new language, Go has a large standards library and extensive documentation. It is primarily used in applications that require the processing of large amounts of data. Netflix, Twitch, and Uber are only a few of the companies that use Go for unique purposes.
</h2>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8080)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:
![client side output](https://user-images.githubusercontent.com/93427303/143028749-65fc38bd-becc-46c9-9535-8e7eedefdcc8.png)
![server side output](https://user-images.githubusercontent.com/93427303/143028656-f63c850c-4564-429d-b4ca-f22981a25230.png)


## RESULT:
The above webser has been run succesfully
