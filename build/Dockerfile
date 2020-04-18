FROM phpmyadmin/phpmyadmin:5.0.2

RUN mkdir /volume
RUN chmod -R 777 /volume

RUN mkdir /script
RUN chmod -R 777 /script

ADD script/run_server_php /script/run_server_php
CMD ["/bin/bash", "-x", "/script/run_server_php" ] 