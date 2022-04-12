$vnet = @{
    Name = 'myVNet'
    ResourceGroupName = 'LattineGroup'
    Location = 'brazilsouth'
    AddressPrefix = '10.0.0.0/16'
    }
    $virtualNetwork = New-AzVirtualNetwork @vnet
$subnet = @{
    Name = 'MySub'
    VirtualNetwork = $virtualNetwork
    AddressPrefix = '10.0.0.0/24'
    }
$subnetConfig = Add-AzVirtualNetworkSubnetConfig @subnet
$vm1 = @{     
    Location ='brazilsouth' 
    ResourceGroupName = 'LattineGroup'
    Name = 'VMName' 
    Size = 'Standard_D2s_v3' 
    VirtualNetworkName = 'MyVnet' 
    ImageName =  'MicrosoftWindowsServer:WindowsServer:2016-Datacenter-with-Containers:latest'
    SubnetName = 'MySub' 
    PublicIpAddressName = 'MyPublic' 
    Credential = $cred
} 
New-AzVM @vm1


