Azure network security group is used to filter network traffic to and from Azure resources in an Azure virtual network. A network security group contains security rules that allow or deny inbound network traffic to, or outbound network traffic from, several types of Azure resources. 

> NSGs are assigned o a network or a subnet

> When you assign a NSG to a subnet, the rules apply to all network interfaces in that subnet

> Each subnet and network interface can have one NSG applied to it

> NSG supports TCP,UDP and ICMP and operate at Layer 4 of the OSI model

> With NSGs, the connection are stateful (Return traffic is automatically allowed for the same TCP/UDP session)

> Several default security rules created by Azure within each NSG which cannot be removed but you can override them with the rules of higher priority

> You can add more rules by specifying Name, Priority, (100 to 4096- Lower # rule has higher priority ), port, Protocol, Source, Destination and Action

**Security rules:**
A network security group contains zeroh, or as many rules as desired, within Azure subscription limits. Each rule specifies the following properties:
1. Name - A unique name within the network security group.
2. Priority - A number between 100 and 4096. Rules are processed in priority order, with lower numbers processed before higher numbers, because lower numbers have higher priority. Once traffic matches a rule, processinga stops. As a result, any rules that exist with lower priorities (higher numbers) that have the same attributes as rules with higher priorities are not processed.
3. Source or destination - Any, or an individual IP address, classless inter-domain routing (CIDR) block (10.0.0.0/24, for example), service tag, or application security group. If you specify an address for an Azure resource, specify the private IP address assigned to the resource. Network security groups are processed after Azure translates a public IP address to a private IP address for inbound traffic, and before Azure translates a private IP address to a public IP address for outbound traffic. . Specifying a range, a service tag, or application security group, enables you to create fewer security rules. The ability to specify multiple individual IP addresses and ranges (you cannot specify multiple service tags or application groups) in a rule is referred to as augmented security rules. Augmented security rules can only be created in network security groups created through the Resource Manager deployment model. You cannot specify multiple IP addresses and IP address ranges in network security groups created through the classic deployment model.
4. Protocol - TCP, UDP, ICMP, ESP, AH, or Any.
5. Direction - Whether the rule applies to inbound, or outbound traffic.
6. Port range - You can specify an individual or range of ports. For example, you could specify 80 or 10000-10005. Specifying ranges enables you to create fewer security rules. Augmented security rules can oenly be created in network security groups created through the Resource Manager deployment model. You cannot specify multiple ports or port ranges in the same security rule in network security groups created through the classic deployment model.
7. Action - Allow or deny




**NSG Creation:**

1.
![image](https://user-images.githubusercontent.com/95157073/145434846-0a65be3d-2283-41c9-9712-2b18a57a338c.png)

2.
![image](https://user-images.githubusercontent.com/95157073/145435437-dc4f6654-3fd5-43bc-875b-8515972009c1.png)

Type in Search bar

3.
![image](https://user-images.githubusercontent.com/95157073/145435894-c2ac7b16-16d5-4381-8f92-9197c3900e2f.png)

4.
![image](https://user-images.githubusercontent.com/95157073/145436106-f5dc317a-d316-4144-bdd1-c824cfbcc763.png)
Select Subscription and Resource group

5.
![image](https://user-images.githubusercontent.com/95157073/145436463-51ba2555-2225-44bc-b4a7-2a4d7dd62c24.png)

Give a name to your NSG

6.
![image](https://user-images.githubusercontent.com/95157073/145436690-d5c06135-838a-4ba5-a894-4f6b5ec856e3.png)

Add tags if needed

7.
![image](https://user-images.githubusercontent.com/95157073/145437383-c4685e2a-47e9-4d00-af7c-0379b0bcf845.png)

8.
![image](https://user-images.githubusercontent.com/95157073/145437487-b02f93a6-c753-4383-bbea-c80e2ccb60c8.png)

9.
![image](https://user-images.githubusercontent.com/95157073/145437570-8a178595-9a46-4773-b95d-d134b28ab9b4.png)

Notice this status on right corner

10.
![image](https://user-images.githubusercontent.com/95157073/145437723-eaf7ba4d-e49c-464c-a564-c01e5663ce7e.png)

11.
![image](https://user-images.githubusercontent.com/95157073/145452883-fdb28c79-0b48-4344-ac20-fae50e858732.png)

12.
![image](https://user-images.githubusercontent.com/95157073/145453565-53ac3222-dfd1-46be-9b99-46c91a38bddc.png)

13.
![image](https://user-images.githubusercontent.com/95157073/145453652-6cd24b56-615c-482d-9f86-9987a81f0131.png)

Select "ADD" to add new inbound security rules

14.
![image](https://user-images.githubusercontent.com/95157073/145454212-78f9f44d-b6f5-4a29-9b43-f3a261031bd0.png)

Select "ADD" to add new outbound security rules

15.
![image](https://user-images.githubusercontent.com/95157073/145454433-6b530a73-4a66-4477-923e-91569df453d5.png)

16.







`                                                                                                       `                                                                                                                                     `                                                           
