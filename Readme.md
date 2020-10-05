Ansible 教程

- 首先创建ansible.cfg，指定inventory的位置

- 然后在对应位置创建hosts来代表要对应的主机

- ```shell
  ansible -m ping all
  ```

  看一下对应主机通了没有

- ad-hoc 命令 

  ```shell
  ansible -m shell -a 'ls' all
  ```

  -m 指定模块，就像一个个linux 命令

  all 用来指定主机

  -b 以sudo 执行

  -K 询问密码

- playbook 命令

  ```shell
  ansible-playbook -K playbook.yml
  ```

  

