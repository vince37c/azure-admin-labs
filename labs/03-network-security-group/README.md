# Lab 03: Configure Network Security Group and Subnet Association

## Objective
Configure a Network Security Group (NSG) with inbound rules and associate it with a subnet to control network traffic to virtual machines.

## Resources Created
- Network Security Group
- Inbound security rules
- NSG to Subnet association

## Prerequisites
- Existing Azure tenant + subscription
- Contributor permissions
- Virtual Network and Subnet from previous labs
- Virtual Machine deployed in the VNet

## Naming Used (Examples)
- Network Security Group: app-subnet-nsg
- Subnet: app-subnet

## Build Steps (Azure Portal)

1. Navigate to **Network security groups**.
2. Click **Create**.
3. Select your subscription and an existing resource group.
4. Enter a name for the NSG.
5. Choose the same region as your virtual network.
6. Click **Review + create**, then **Create**.

### Configure Inbound Rules

7. Open the newly created NSG.
8. Select **Inbound security rules**.
9. Click **Add**.
10. Configure rule values (example):

- Source: Any  
- Destination: Any  
- Service: RDP or HTTP  
- Action: Allow  
- Priority: 1000  
- Name: allow-access  

11. Click **Add**.

### Associate NSG with Subnet

12. From the NSG blade, select **Subnets**.
13. Click **Associate**.
14. Select your Virtual Network.
15. Select the target subnet.
16. Click **OK**.

## Validation

- Confirm inbound rules appear in the NSG.
- Verify the NSG is associated with the subnet.
- Check VM networking to confirm traffic is governed by the subnet NSG.

## Screenshots to Capture

- NSG overview → 01-nsg-overview.png  
- Inbound rule configuration → 02-nsg-rule.png  
- Subnet association blade → 03-nsg-subnet.png  

## Cleanup

1. Navigate to the Network Security Group.
2. Delete the NSG.
3. Confirm the subnet association is removed.

## Notes / What I Learned

- NSGs can be applied at both subnet and NIC levels.
- Subnet-level NSGs affect all resources inside that subnet.
- Lower priority numbers take precedence.
- Custom allow rules override default deny behavior.
