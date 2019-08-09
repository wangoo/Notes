CentOS 7:

         yum install python-setuptools && easy_install pip
         yum install openssh git
         pip install git+https://github.com/shadowsocks/shadowsocks.git@master
         
  Usage with Config File 
  
        ssserver -c /etc/shadowsocks.json -d start 
        ssserver -c /etc/shadowsocks.json -d stop
   
  Create a config file /etc/shadowsocks.json. Example:
    
          {
              "server":"my_server_ip",
              "server_port":8388,
              "local_address": "127.0.0.1",
              "local_port":1080,
              "password":"mypassword",
              "timeout":300,
              "method":"aes-256-cfb",
              "fast_open": false
            }
    Open firewall port :
    
        firewall-cmd --zone=public --add-port=xxxx/tcp --permanent
        firewall-cmd --reload
