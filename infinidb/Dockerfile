FROM vvoronin/ubuntu-tools
MAINTAINER Viktor Voronin <voronin@x12.su>

RUN /tools/apt build-essential wget libncurses5-dev expect libz-dev libxml2-dev libreadline-dev flex

WOKDIR /tmp
 
RUN wget -Omysql-4.6.2-1.tar.gz https://github.com/infinidb/mysql/archive/4.6.2-1.tar.gz &&\
	tar -zxf mysql-4.6.2-1.tar.gz &&\
	ln -s mysql-4.6.2-1 mysql &&\
	cd mysql &&\
	./configure --prefix=/usr/local/Calpont/mysql &&\
    make &&  make install &&\
    cd .. &&\
	wget -Oinfinidb-4.6.2-1.tar.gz https://github.com/infinidb/infinidb/archive/4.6.2-1.tar.gz &&\
	tar -zxf infinidb-4.6.2-1.tar.gz &&\
	ln -s infinidb-4.6.2-1 infinidb &&\
	cd infinidb &&\
	./configure --prefix=/usr/local/Calpont/ &&\
	make && make install
    