FROM duunky/dunkyandfilscorporation:server-web-GIS
WORKDIR /
RUN mkdir /API
COPY index.html /usr/share/nginx/html/
COPY installationDotNet.sh /
COPY start.sh /
COPY API /API
ADD installationDotNet.sh /docker-entrypoint.d
ADD start.sh /docker-entrypoint.d
RUN chmod +x /installationDotNet.sh
RUN chmod +x /start.sh
RUN ./installationDotNet.sh
COPY default.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
CMD ["/start.sh"]
