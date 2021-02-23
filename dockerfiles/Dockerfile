FROM mariadb:latest

ENV MYSQL_ROOT_PASSWORD test123
ENV MYSQL_DATABASE testDB
ENV MYSQL_USER testuser
ENV MYSQL_PASSWORD test123

# Configure root password
#RUN echo "root:root123" | chpasswd

EXPOSE 3306

CMD ["mysqld"]
