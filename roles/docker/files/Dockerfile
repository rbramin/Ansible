FROM rockylinux:9

RUN dnf install -y httpd php php-mysqlnd mysql wget tar && \
    dnf clean all

WORKDIR /var/www/html

RUN wget https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/CUR-TF-200-ACACAD/studentdownload/lab-app.tgz && \
    tar xvf lab-app.tgz && rm -f lab-app.tgz

RUN chown -R apache:root /var/www/html

CMD ["/usr/sbin/httpd","-DFOREGROUND"]

EXPOSE 80

