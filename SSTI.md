# What is server-side template injection?

A server-side template injection occurs when an attacker is able to use native template syntax to inject a malicious payload into a template, which is then executed server-side.

Template engines are designed to generate web pages by combining fixed templates with volatile data. Server-side template injection attacks can occur when user input is concatenated directly into a template, rather than passed in as data. This allows attackers to inject arbitrary template directives in order to manipulate the template engine, often enabling them to take complete control of the server.

An example of vulnerable code see the following one:
```javascript
$output = $twig->render("Dear " . $_GET['name']);
```
In the previous example part of the template itself is being dynamically generated using the GET parameter name. As template syntax is evaluated server-side, this potentially allows an attacker to place a server-side template injection payload inside the name parameter as follows:
```javascript
http://vulnerable-website.com/?name={{bad-stuff-here}}
```

## Constructing a server-side template injection attack
