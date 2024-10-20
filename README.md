# TACACS-_and_RADIUS
Configure authentication based on server with TACACS+ and RADIUS:

In this lab, you will see how to configure server-based AAA authentication using TACACS+ and RADIUS.
This lab is available in Cisco Network Academy.

For your best experience, paste the link below into your browser to download the packet tracer archieve:

**https://drive.google.com/file/d/10IWMiN9pNdex_0u2VV82sH_hHoYQT_o-/view?usp=drive_link

Step by Step:

- Configure server-based AAA authentication using TACACS+.
- Verify server-based AAA authentication of client PC-B.
- Configure server-based AAA authentication using RADIUS.
- Verify server-based AAA authentication of client PC-B.


Topology of the project -> 

![image](https://github.com/user-attachments/assets/61f58fc9-19ee-4d0c-b037-b5dd8a4cc9b0)

Route table -> 

![image](https://github.com/user-attachments/assets/4a552b8f-fe3f-4374-b7c5-a73a9abcb59b)

Cennario:
The network topology shows routers R1, R2, and R3. Currently, all administrative security is based on knowledge of the secret enable password. In this lab, I configured and tested both local and server-based AAA solutions.

Configure router R2 to support server-based authentication using the TACACS+ protocol.
Configure router R3 to support server-based authentication using the RADIUS protocol.

Part 01: Configure the AAA authentication based on server using the TACACS+ protocol on R2:

First step we gonna check if hte PCs have interconnection using the PING at command prompt.
To complete this task consult the route table.

Ping PC-A to PC-B and PC-C ->

![image](https://github.com/user-attachments/assets/25ec4989-40c7-4a18-bf76-71e1ee989aa7)

Ping PC-B to PC-C ->

![image](https://github.com/user-attachments/assets/67bc4ce6-3a48-401f-b2e3-036ed670f822)

2. Configure a local backup database entry named Admin:
For backup purposes, configure a local username of Admin2 and a secret password of admin2pa55.

![image](https://github.com/user-attachments/assets/aef45e4c-9127-433e-aaf1-4f4fc33dfd23)

3. Check the TACACS+ server configuration:
Click the TACACS+ server.
**On the Services tab, click AAA. Note that after the configuration on R2 there is a network configuration entry for R2 and a user setup entry for Admin2.

![image](https://github.com/user-attachments/assets/41f4ad2b-7784-4d4c-a2ea-feace9081195)

4. Configuration of the TACACS+ server details:

The first step is configure the IP address and the server AAA TACACS secret key on R2.

![image](https://github.com/user-attachments/assets/305890bc-74f9-45d7-9969-4ad98c4adc9f)

5. Configuration of AAA login authentication for console access on R2:

Enable AAA on R2 and configure all logins to authenticate using the TACACS+ AAA server. If it is not available, use the local database.

5.1 . Configure the vty lines to use the defined AAA authentication method.

Configure AAA authentication so that console login uses the default AAA authentication method.

![image](https://github.com/user-attachments/assets/1d17cb4b-6fd3-407a-96f1-56863f47f874)

6. Now verify if you can access R2 with the new credentials that you’ve create.

![image](https://github.com/user-attachments/assets/c8570710-4410-43c9-8a98-f51947886aae)

**NOTE: If you do not be able to access the router, please back some steps and verify.

Part 02: Configure the AAA authentication based on server using the RADIUS protocol on R3:

Set up a local backup database called Admin:
For backup purposes, set up a local username of Admin3 and a secret password of admin3pa55.

![image](https://github.com/user-attachments/assets/72348e62-5985-4260-9ffc-84ff4f66c467)

2. Check the RADIUS server configuration:
Click the Radius server.
**On the Services tab, click AAA. Notice that there is a network configuration entry for R3 and a user installation entry for Admin3.

![image](https://github.com/user-attachments/assets/5d8af097-2dad-4abf-9520-94a1869f27c0)

3. Configure details of RADIUS server on R2:
Configure the IP address and secret key of the AAA Radius server on R3.

![image](https://github.com/user-attachments/assets/9d569955-58b4-49f7-ac21-acacb2b0395b)

4. Configure AAA login authentication for console access on R3:
Enable AAA on R3 and configure all logins to authenticate using the AAA Radius server. If it is not available, use the local database.

![image](https://github.com/user-attachments/assets/e00c890a-61e6-4c4b-b678-169a6a7b656e)

5. Verify your AAA authentication methods.

Now after those steps you have completed this LAB!!!


