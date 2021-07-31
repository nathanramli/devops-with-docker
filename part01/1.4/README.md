I execute the install command for curl first.

```
~ $ docker run -it --name dowd-1.4 ubuntu sh -c 'apt-get update; apt-get install curl; echo "Input website:"; read website
; echo "Searching.."; sleep 1; curl http://$website;'
....
done.
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>
```