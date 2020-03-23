Setup several nodejs services for nginx load balancing.


``` 
#nginx.conf
http {
    upstream backend {
        server 127.0.0.1:3001;
        server 127.0.0.1:3002;
    }
}

#...
location / {
        proxy_pass http://backend;
    }
}
```
