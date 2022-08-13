# docker_tool
docker_tool
wget https://nmap.org/dist/nmap-7.92.tar.bz2
bzip2 -cd nmap-7.92.tar.bz2  | tar xvf -
nmap-7.92.tar.bz2 
cd nmap-7.92
./configure
make
sudo su
make install



mkdir "logs"
docker run --restart=always --ulimit nofile=65536:65536 -p 9200:9200 -p 9300:9300 -d --name es1 -v $PWD/logs:/usr/share/elasticsearch/logs -v $PWD/config/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml -v $PWD/config/jvm.options:/usr/share/elasticsearch/config/jvm.options  -v $PWD/data:/usr/share/elasticsearch/data  hktalent/elasticsearch:7.16.2
echo "Wait for es to start before running the following script"
docker logs -f es1
echo "Wait for es to start before running the following script"


apt install docker.io
docker pull yankovg/python3.8.2-ubuntu18.04
docker run -itd yankovg/python3.8.2-ubuntu18.04 bash
docker exec -it docker的ID /bin/bash
apt-get update
apt install git --fix-missing
apt install vim
rm /usr/bin/python3
ln -s /usr/local/bin/python3.8 /usr/bin/python3
python3 -m pip install --upgrade pip
git clone https://github.com/0x727/ShuiZe_0x727.git
chmod 777 docker_build.sh
./docker_build.sh


docker cp a0c5177c07b7:/ShuiZe_0x727/ShuiZe.py /root

docker cp a0c5177c07b7:/ShuiZe_0x727/result/4e998a3086bb/bibvip.com.xlsx /root

1.docker打包
https://blog.csdn.net/m0_67402125/article/details/123869967

2.装载之前打包的tar文件，首先需要安装好你的docker，并运行。
执行命令装载到你的docker中
docker load< 你的路径/rabbitmq.tar

运行你的tar文件

docker run -d -p 5672:5672 -p 15672:15672 --name rabbitmq newmq:v1
