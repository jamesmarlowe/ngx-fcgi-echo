# ngx-fcgi-echo
Example fcgi application that echos post data back through nginx

Requisites
----------
This requires the FastCGI Developer's Kit (http://www.fastcgi.com/) and spawn-fcgi
```
sudo apt-get install libfcgi-dev spawn-fcgi
```

Building
--------
```
cd ngx-fcgi-echo
mkdir build
cd build
cmake ..
make
```

Running
-------
```
bash fastcgi-echo.sh
bash restart.sh
```

Trying
------
simply POST to localhost/ with a post body to see it echoed
```
curl -X POST -d 'test' localhost/uri
```
Which should give you
```
test from localhost/uri
```

Notes
-----
* fcgi docs available at http://www.fastcgi.com/
* To return an HTTP status other than 200, add a 'Status:' header in your fcgi file

