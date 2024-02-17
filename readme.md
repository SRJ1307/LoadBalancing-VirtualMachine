# Load Balancing using the Virtual Machine based on IP
Here we will learn how do manag the traffice coming on our webiste by using VMs.
IN this case VMs are already created we will just attach the load balancer.
Note: Here we are using Virtual Machine, so we need to decide on how much instance/VM we will distribute our load. Unlike VMSS Vm instances will not automitically scale.

    1. Search for Load Balancer in Azure.
    2. Click on +  to start creating one.
    3. Follow teh steps as mentioned in attached images of this file.
<img width="966" alt="image" src="https://github.com/SRJ1307/LoadBalancing-VirtualMachine/assets/157812379/e477a0fa-3415-47d1-94eb-53f90df2aea1">


Make sure load balancer type is public here, since we will be accessing it outside internet, so it should be accessible from anywhere.
     
<img width="1250" alt="image" src="https://github.com/SRJ1307/LoadBalancing-VirtualMachine/assets/157812379/f57f6ed7-8461-4994-91db-0b48e950567b">
    Add fron-end IP configuration by creating new public IP, or if you have any other you can use that also.
    
<img width="970" alt="image" src="https://github.com/SRJ1307/LoadBalancing-VirtualMachine/assets/157812379/c0292128-8a2d-41d4-9bff-b2da498434dc">
    In the backned pool add one, make sure to choose the same vnet, which is associate with the VMs.
    In IP address section from dropdown choose the ip address of all VMs on which you want to balance the load.
    
<img width="1249" alt="image" src="https://github.com/SRJ1307/LoadBalancing-VirtualMachine/assets/157812379/4d5dd67b-53e2-4aeb-b04a-0ea336b90ab5">
    In the Inbound Rule create a load balancing rule.
    As of now no need to create any outbound rule for this example.
    Skip to last now, and review + create.
<img width="1243" alt="image" src="https://github.com/SRJ1307/LoadBalancing-VirtualMachine/assets/157812379/3ab750a6-5cd8-4757-bffd-9e8143c06547">
Go to the load Balancer you created, navigate to front-end ip configuration in left pane.
Copy the public IP and paste it in a new tab in browser. You should be able to see you application running.
<img width="1274" alt="image" src="https://github.com/SRJ1307/LoadBalancing-VirtualMachine/assets/157812379/29c24dc8-2564-4e53-a2fd-181864e3a16f">

Happy Learning!


    




   
