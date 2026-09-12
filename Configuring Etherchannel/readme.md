<img width="992" height="526" alt="image" src="https://github.com/user-attachments/assets/fe0f8ca9-c2f7-4fca-986a-5927fea00932" />

In this lab, I configured **EtherChannel** using three different methods:
1) **LACP** using the ```channel-group 1 mode active``` command — deployed on the ASW1 to DSW1 link.
2) **PAgP** using the ```channel-group 1 mode desirable``` command — deployed on the ASW2 to DSW2 link.
3) **Static EtherChannel** using the ```channel-group 1 mode on``` command — deployed on the DSW1 to DSW2 link.
   
Additionally, I configured SVIs on DSW1 and DSW2 to serve as the default gateways for the PCs and the Server.
A dedicated /30 subnet was also configured on the routed EtherChannel link between DSW1 and DSW2 to enable inter-switch routing.
