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
8. If you enter several of the following commands in succession in the console, you can visually check the operation of the fault tolerance provided by the    `keepalived` daemon:
*      vagrant ssh haproxy2
*      sudo poweroff
9. After entering these commands, we again go to the already existing ip address in the browser **(ip is given in paragraph 6)** and reload the page several      times again. Even after turning off one of the servers, the address continues to be operational and the http pages change in accordance with the          algorithm of our `haproxy`-type balancing.

*Screenshots:*

<a href="https://ibb.co/02cW1JR"><img src="https://i.ibb.co/H4VMRgf/IMG-20220408-093152-948.jpg" alt="IMG-20220408-093152-948" border="0"></a>

<a href="https://ibb.co/44NnNR8"><img src="https://i.ibb.co/5scgchr/2022-04-08-12-56-56.png" alt="2022-04-08-12-56-56" border="0"></a>

<a href="https://ibb.co/8B1p4TL"><img src="https://i.ibb.co/rtDSfTR/2022-04-08-13-03-29.png" alt="2022-04-08-13-03-29" border="0"></a>

<a href="https://ibb.co/X4nQywv"><img src="https://i.ibb.co/YW5CDrq/2022-04-08-12-57-18.png" alt="2022-04-08-12-57-18" border="0"></a>

<a href="https://ibb.co/3Tshhyy"><img src="https://i.ibb.co/vcBzzxx/2022-04-08-13-07-36.png" alt="2022-04-08-13-07-36" border="0"></a>

<a href="https://ibb.co/8B1p4TL"><img src="https://i.ibb.co/rtDSfTR/2022-04-08-13-03-29.png" alt="2022-04-08-13-03-29" border="0"></a>
