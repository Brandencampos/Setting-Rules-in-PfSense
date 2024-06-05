# Setting-Rules-in-PfSense
## Objective


The Objective of this lab will be to gain some hands on experience with setting rules in order to be able to access PfSense remotely in order to manage it through a kali linux machine over WAN.

### Skills Learned

- Proficiency in setting rules for firewalls to allow traffic in order to manage PfSense remotely
- Practical experience within the PfSense console
- Proficiency in setting ports only needed for access

### Tools Used
- PfSense

  
## Steps 
- Log in to the PfSense admin console
  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/c0d07aa7-7c83-48f0-9c89-a6854a5fc1cb)

- We'll navigate over to the Rules Page

![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/8aa76909-ea50-4b9b-9415-54f62f806a2c)

- Created a seperator for rules that are being created for remote management. This rule will be created so that when connected to the firewalls IP it will allow traffic.

![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/956b233c-6e36-4aa3-a054-e65c5e32482c)


- Once we start adding the rule the following settings will be used. Pass for the action, WAN interface, IPv4 address family, and TCP protocol.

  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/23ce542e-9027-47ed-afc5-2b4496c25467)


- For the source we'll use the address or alias option and will set the address to a kali linux box that we'll use in order to connect.

  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/567ae174-a7bc-49c7-b234-895b6b9f654c)


- For the destination we'll set it to "This Firewall"

  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/db768f75-6d95-437f-828e-51bd7b729d8d)


- We have the option to choose the port range as well but for this example we'll leave it at any

  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/82c0a22f-7625-4ea8-9e8f-fb870e3a51a9)


- After clicking save the rule should now be active and in the rules page

  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/304375c6-f809-4cae-bd65-1fa8a08b6611)


- Now we'll test from our Kali Linux box to see if the connection is allowed

![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/673a53e7-80d9-4e35-97f6-38f395bc7dc3)


- Was able to connect after creating rule and accessing through the IP address for PfSense WAN interface 192.168.0.25 and also able to ping

  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/38e7a968-2e60-4748-b9ec-bd9e33f55df6)


- Now we'll add ports that we'll be able to use to access

  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/057f6836-bb63-4686-9e61-56080b3cb7be)


- The alias is now created

![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/d739cafb-a2a8-4b4d-8bae-48a24fd2c358)


- We'll go ahead and edit the rule we made and reference the alias for the ports
- Instead of having the destination set to any we'll change it to other
  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/cfd402af-23eb-489c-ab34-f94358047d60)


- Now we can reference the alias Remote_mgmt


  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/3d75ed33-0629-4fde-82c5-7a0447131858)


- After setting that alias in the rule we should still be able to connect to the page on the browser

  ![image](https://github.com/Brandencampos/Setting-Rules-in-PfSense/assets/62733055/1f54c434-9d68-42cb-9218-67b9e12da7ca)



  




  
