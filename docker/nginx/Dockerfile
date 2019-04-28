FROM nginx:latest

# static web files (css, img, etc)
# COPY /public /var/www/public

COPY /config/nginx.conf /etc/nginx/nginx.conf

# RUN chmod 755 -R /var/www/public

EXPOSE 80 443

ENTRYPOINT ["nginx"]

CMD ["-g", "daemon off;"]