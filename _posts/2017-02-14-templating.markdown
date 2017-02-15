my newish default xhtml template look something like.
 

```html
<?xml version='1.0' encoding='UTF-8'?>
<html xmlns="http://www.w3.org/1999/xhtml"><head>
 <meta name="viewport" content="width=device-width, initial-scale=1"/>
 <title></title>
 <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
</head><body>
	
</body></html>
```


while a fairly nice wsgi footer looks like

```python


def blunk(status, response_headers):
    print 'status:\t%s' % status
    for I in response_headers:
        print '%s:\t%s' % (I[0], I[1])
    print '\n\n',

if __name__ == '__main__':
    foo = application({}, blunk)
    print foo
```

this allows for the execution of the script from the command line simplifying troubleshooting.