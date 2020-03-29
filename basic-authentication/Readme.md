OS: Centos 7.+


1. Install password file creation utility: `yum install httpd-tools`

2. Generate user-password pair: `htpasswd -c /etc/nginx/.htpasswd user1`

3. Protect nginx location:

    location / {
        auth_basic           “Administrator’s Area”;
        auth_basic_user_file /etc/nginx/.htpasswd user1; 
    }
