<img width="925" height="483" alt="image" src="https://github.com/user-attachments/assets/b04b62e3-a527-49f5-9a79-dffb5b136edf" />

In this lab I configured an **OSPF route** via ISPR1, and a **floating static route** via ISPR2.
Both of the routes can be tested in such a way: 
1. First, use `tracert 8.8.8.8` command in the PC1's command prompt, to show the route of the packet from PC1 to R2-Remote, also you can check the R1's routing table using the `show ip route` command. There will be an OSPF route to `8.8.8.8` via ISPR1, marked with the **O** letter.
2. Then open the R1 CLI, and shutdown the g0/1 interface using the `shutdown` command.
3. Try to `tracert 8.8.8.8` from PC1 now.
As you can see, the route from PC1 to R2-Remote now passes the ISPR2 Router. Use the `show ip route` command on R1's CLI to confirm that the route to `8.8.8.8` is now static, marked with the **S** letter, and has an Administrative Distance of 120.
