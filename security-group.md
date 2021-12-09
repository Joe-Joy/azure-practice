Azure network security group is used to filter network traffic to and from Azure resources in an Azure virtual network. A network security group contains security rules that allow or deny inbound network traffic to, or outbound network traffic from, several types of Azure resources. 

NSGs are assigned o a network or a subnet
When you assign a NSG to a subnet, the rules apply to all network interfaces in that subnet
Each subnet and network interface can have one NSG applied to it
NSG supports TCP,UDP and ICMP and operate at Layer 4 of the OSI model
With NSGs, the connection are stateful (Return traffic is automatically allowed for the same TCP/UDP session)
Several default security rules created by Azure within each NSG which cannot be removed but you can override them with the rules of higher priority
You can add more rules by specifying Name, Priority, (100 to 4096- Lower # rule has higher priority ), port, Protocol, Source, Destination and Action

**Security rules:**
A network security group contains zeroh, or as many rules as desired, within Azure subscription limits. Each rule specifies the following properties:
1. Name - A unique name within the network security group.
2. Priority - A number between 100 and 4096. Rules are processed in priority order, with lower numbers processed before higher numbers, because lower numbers have higher priority. Once traffic matches a rule, processinga stops. As a result, any rules that exist with lower priorities (higher numbers) that have the same attributes as rules with higher priorities are not processed.
3. Source or destination - Any, or an individual IP address, classless inter-domain routing (CIDR) block (10.0.0.0/24, for example), service tag, or application security group. If you specify an address for an Azure resource, specify the private IP address assigned to the resource. Network security groups are processed after Azure translates a public IP address to a private IP address for inbound traffic, and before Azure translates a private IP address to a public IP address for outbound traffic. . Specifying a range, a service tag, or application security group, enables you to create fewer security rules. The ability to specify multiple individual IP addresses and ranges (you cannot specify multiple service tags or application groups) in a rule is referred to as augmented security rules. Augmented security rules can only be created in network security groups created through the Resource Manager deployment model. You cannot specify multiple IP addresses and IP address ranges in network security groups created through the classic deployment model.
4. Protocol - TCP, UDP, ICMP, ESP, AH, or Any.
5. Direction - Whether the rule applies to inbound, or outbound traffic.
6. Port range - You can specify an individual or range of ports. For example, you could specify 80 or 10000-10005. Specifying ranges enables you to create fewer security rules. Augmented security rules can oenly be created in network security groups created through the Resource Manager deployment model. You cannot specify multiple ports or port ranges in the same security rule in network security groups created through the classic deployment model.
7. Action - Allow or deny


NSG Creation:

1.
![image](https://user-images.githubusercontent.com/95157073/145434846-0a65be3d-2283-41c9-9712-2b18a57a338c.png)

2.
![image](https://user-images.githubusercontent.com/95157073/145435437-dc4f6654-3fd5-43bc-875b-8515972009c1.png)


`                                                                                                       `                                                                                                                                     `                                                           
