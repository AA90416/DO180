ubi7/ubi:7.7

sandeep ved <sandeepv@sg.ibm.com>

PORT 8080

yum install -y httpd && yum clean all

sed -ri -e "/^Listen 80/c\Listen ${PORT}" /etc/httpd/conf/httpd.conf &&
    chown -R apache:apache /etc/httpd/logs/ && 
    chown -R apache:apache /run/httpd/

apache

# Expose the custom port that you provided in the ENV var
${PORT}

# Copy all files under src/ folder to Apache DocumentRoot (/var/www/html) 


# Start Apache in the foreground
"httpd","-D","FOREGROUND"
