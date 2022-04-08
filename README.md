# lab_05

   **The second example of a server balancer.**

   Balancing type - `haproxy`.
   
   The fault tolerance of the balancing servers is provided with the help of `keepalived`.
   
  To test the work of this balancer, you need:
1. Download all files from this repository and move them to one folder.
2. On the command line, write the command:
*      vagrant up
3. Wait until the virtual machines are created and started.
4. After that, enter the command in the command line:
*      ansible-playbook nginx.conf
5. Wait until the playbook is played and the results of its work are displayed.
6. After that, we launch any of our browsers and enter in the search bar:
*      http://192.168.11.100/
7. We are waiting for the html page to load, then we press the page reload button and observe how the page will change.

*Screenshots:*

<a href="https://ibb.co/02cW1JR"><img src="https://i.ibb.co/H4VMRgf/IMG-20220408-093152-948.jpg" alt="IMG-20220408-093152-948" border="0"></a>

<a href="https://ibb.co/TP0JVyN"><img src="https://i.ibb.co/44SC6k0/IMG-20220408-093157-946.jpg" alt="IMG-20220408-093157-946" border="0"></a>

<a href="https://ibb.co/6Rkvjqt"><img src="https://i.ibb.co/wNfJ52Q/IMG-20220408-093155-197.jpg" alt="IMG-20220408-093155-197" border="0"></a>
