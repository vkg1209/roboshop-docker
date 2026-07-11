FROM mysql:8.0
ENV MYSQL_ROOT_PASSWORD="RoboShop@1"
ENV CART_ENDPOINT=cart:8080
ENV DB_HOST=mysql
COPY db/ /docker-entrypoint-initdb.d
CMD ["java", "-jar", "/app/shipping.jar"]

Environment=CART_ENDPOINT=<CART-SERVER-IPADDRESS>:8080
Environment=DB_HOST=<MYSQL-SERVER-IPADDRESS>
# Created as part of K8 init containers
# FROM mysql:8.0
# COPY db/ /docker-entrypoint-initdb.d
# COPY custom-script.sh /usr/local/bin/custom-script.sh
# RUN chmod +x /usr/local/bin/custom-script.sh
# ENTRYPOINT ["/usr/local/bin/custom-script.sh"]

# FROM mysql:8.0
# ENV MYSQL_ROOT_PASSWORD="RoboShop@1"
# COPY db/ /docker-entrypoint-initdb.d