logstash install

安装jdk
yum -y install java-1.8.0
安装jdk
wget https://artifacts.elastic.co/downloads/logstash/logstash-6.4.0.tar.gz
tar zxf logstash-6.4.0.tar.gz -C /Data/apps/
配置logstash的环境变量
echo "export PATH=\$PATH:/Data/apps/logstash-6.4.0/bin" > /etc/profile.d/logstash.sh
. /etc/profile

启动logstash
logstash -e "input {stdin{}} output {stdout{}}" --quiet

logstash -e 'input{stdin{}}output{stdout{codec=>rubydebug}}'

logstash -f logstash.conf --quiet

ref: https://blog.csdn.net/CleverCode/article/details/78632887

==========

logstash-input-jdbc安装
. bin/logstash-plugin install logstash-input-jdbc
mysql-connector-java下載
wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-8.0.12.tar.gz
tar zxf mysql-connector-java-8.0.12.tar.gz -C .

wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.47.tar.gz
tar zxf mysql-connector-java-5.1.47.tar.gz -C .
