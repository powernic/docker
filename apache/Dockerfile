FROM php:apache
RUN docker-php-ext-install mysqli

ENV APACHE_RUN_USER travis
ENV APACHE_RUN_GROUP travis
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_PID_FILE /var/run/apache2/apache2.pid
ENV APACHE_LOCK_DIR /var/lock/apache2