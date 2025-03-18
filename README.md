
# Creating Azure Virtual Networks Tutorial     Date : 2025-03-18

I'll walk you through the process of creating Azure Virtual Networks with screenshots for each step.

## Step 1: Create a Virtual Network
1. In the Azure portal, search for "Virtual networks" and select "Create virtual network"
2. Name your virtual network (e.g., "vnet1")
3. Assign an address space (e.g., 10.0.0.0/16)
4. Rename the default subnet to "subnet-a" and assign it an address range (e.g., 10.0.0.0/24)

![Creating virtual network with subnet-a](https://github.com/user-attachments/assets/bbac8546-65e1-4916-848c-58863390a3ad)

## Step 2: Create a Second Subnet
1. After the virtual network is created, navigate to "Subnets" under the virtual network
2. Click "+ Subnet" to add a new subnet
3. Name it "subnet-b" and assign an address range (e.g., 10.0.1.0/24)

![Creating subnet-b](https://github.com/user-attachments/assets/303de79f-1101-4834-af49-4acd14acff5b)

![Subnet-b configuration](https://github.com/user-attachments/assets/4285ca09-a060-4be0-b694-6641388f2827)

## Step 3: Verify Both Subnets
After creating both subnets, verify they appear correctly in your virtual network:

![Both subnets configured](https://github.com/user-attachments/assets/263a8317-f294-45c3-af01-0ac84ad71b8c)

## Step 4: Create and Associate Network Security Group
1. Create a new Network Security Group (NSG) called "NSG-1" in the same region as your virtual network
2. Associate the NSG with both subnet-a and subnet-b to act as a stateful firewall

![NSG association complete](https://github.com/user-attachments/assets/10efd2c0-05e4-45bc-92e8-f6048d26bda2)

Now your Azure virtual network is properly configured with two subnets, both protected by the same Network Security Group,

**SIDE BENEFIT**
When creating a Network Security Group (NSG), it must be deployed in the same region as the virtual network it will protect.
If you create an NSG in a different region from your virtual network, you won't be able to associate it with your subnets, 
as Azure requires NSGs to be in the same region as the virtual network resources they protect


