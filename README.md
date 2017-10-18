# learning-ansible



### 入门实例

#### 连接受控机器

+ 创建hello/hosts文件，添加如下内容

  ```shell
  tpd ansible_ssh_host=172.28.104.225 ansible_ssh_port=22 ansible_ssh_user=frank ansible_ssh_pass=1
  ```

+ 执行如下命令

  ```shell
   ansible tpd -i hosts   -m ping
  ```

  返回结果

  ```
  tpd | FAILED! => {
      "failed": true,
      "msg": "to use the 'ssh' connection type with passwords, you must install the sshpass program"
  }
  ```

+ 安装sshpass

  ```shell
  sudo apt-get install  sshpass 
  ```

+ 执行如下命令

  ```
  ansible tpd -i hosts   -m ping

  # 返回结果
  tpd | SUCCESS => {
      "changed": false,
      "failed": false,
      "ping": "pong"
  }
  ```

#### 执行Playbooks



### 资料索引

+ [python自动化运维篇(视频)](http://www.imooc.com/learn/853) 


+ [Ansible中文权威指南](http://www.ansible.com.cn/)
+ [ansible-examples](https://github.com/ansible/ansible-examples/)
+ [使用ansible搭建自动发布系统](http://blog.csdn.net/sunyurun/article/details/43463915)
+ [《奔跑吧Ansible》](https://book.douban.com/subject/26699570/)
+ [Code samples from the book "Ansible: Up and Running" ](https://github.com/ansiblebook/ansiblebook)

