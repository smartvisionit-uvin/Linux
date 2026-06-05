**Log in to Cloudlare**


**Expand networks and select Tunnels**


**Create a new tunnel**


<img width="1577" height="770" alt="image" src="https://github.com/user-attachments/assets/5392342d-57dc-45d6-85c0-737bca2c66eb" />

**We will be setting up the Server on a Red hat Linux VM instance**


<img width="1148" height="618" alt="image" src="https://github.com/user-attachments/assets/88c16cb9-bf36-44db-9bc4-111a71485356" />

<img width="1817" height="982" alt="image" src="https://github.com/user-attachments/assets/4a11babf-2048-434a-8052-400c2bcab677" />


**Once installed the Tunnel will pop up**


<img width="1255" height="503" alt="image" src="https://github.com/user-attachments/assets/a70978f6-d529-4c82-9249-888158fc34b4" />

Click add published application and add a route. In this example, I will be adding a route to my ESXi host.

<img width="615" height="701" alt="image" src="https://github.com/user-attachments/assets/193b977b-545b-435f-95a4-12dbf77c4ec8" />


**Click save changes**

**Head back into Networking > Tunnels, click on the 3 dots and select Manage in Zero Trust**


<img width="1102" height="589" alt="image" src="https://github.com/user-attachments/assets/4ea9a7d8-7ff1-4d58-babd-2494aa94ea7d" />

**Select the route and make sure no TLS verify is turned off**


<img width="1594" height="782" alt="image" src="https://github.com/user-attachments/assets/541f2e86-3166-4715-8315-d5800c8f0e5a" />


**The subdomain I set up now takes me to my Esxi logon page**


<img width="924" height="746" alt="image" src="https://github.com/user-attachments/assets/85321841-d6ac-452b-ad34-d2e8b7461363" />

Set up LDP for additional security.

Click on Zero trust on the left pane and select protect an application with access. Add one time pin.

<img width="822" height="676" alt="image" src="https://github.com/user-attachments/assets/051204ce-6a62-4dcc-8454-815330585e00" />


<img width="1885" height="859" alt="image" src="https://github.com/user-attachments/assets/9c1f1ad1-3456-47d1-a1aa-5b13585f1ca3" />


<img width="1143" height="336" alt="image" src="https://github.com/user-attachments/assets/b891e8ba-ad54-4b26-b2c5-63a02f8402b5" />







