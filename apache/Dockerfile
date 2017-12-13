FROM php:apache
RUN docker-php-ext-install mysqli
RUN apt-get update && apt-get install -q -y ssmtp mailutils && rm -rf /var/lib/apt/lists
RUN echo "hostname=rusnasti.ru" > /etc/ssmtp/ssmtp.conf
RUN echo "root=powernic@list.ru" >> /etc/ssmtp/ssmtp.conf
RUN echo "mailhub=mail" >> /etc/ssmtp/ssmtp.conf
RUN echo "FromLineOverride=YES" >> /etc/ssmtp/ssmtp.conf

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_PID_FILE /var/run/apache2/apache2.pid
ENV APACHE_LOCK_DIR /var/lock/apache2