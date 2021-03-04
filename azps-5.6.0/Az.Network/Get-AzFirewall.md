---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 56227c5c3df8f428e8d25329f8dbb9965ff502cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956952"
---
# <span data-ttu-id="b565b-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b565b-101">Get-AzFirewall</span></span>

## <span data-ttu-id="b565b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b565b-102">SYNOPSIS</span></span>
<span data-ttu-id="b565b-103">Получает брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="b565b-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="b565b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b565b-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b565b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b565b-105">DESCRIPTION</span></span>
<span data-ttu-id="b565b-106">С **помощью cmdlet Get-AzFirewall** можно получить один или несколько брандмауэров в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b565b-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="b565b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b565b-107">EXAMPLES</span></span>

### <span data-ttu-id="b565b-108">1. Извлечение всех брандмауэров в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b565b-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="b565b-109">В этом примере извлекает все брандмауэры в группе ресурсов "rgName".</span><span class="sxs-lookup"><span data-stu-id="b565b-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="b565b-110">2. Извлечение брандмауэра по имени</span><span class="sxs-lookup"><span data-stu-id="b565b-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="b565b-111">В этом примере извлекает брандмауэр azFw в группе ресурсов "rgName".</span><span class="sxs-lookup"><span data-stu-id="b565b-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="b565b-112">3. Извлечение всех брандмауэров с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="b565b-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="b565b-113">В этом примере извлекается все брандмауэры, которые начинаются с azFw.</span><span class="sxs-lookup"><span data-stu-id="b565b-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="b565b-114">4. Получение брандмауэра и добавление коллекции правил приложений в брандмауэр</span><span class="sxs-lookup"><span data-stu-id="b565b-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="b565b-115">В этом примере мы извлекаем брандмауэр, а затем добавляем в брандмауэр коллекцию правил приложений, вызывая метод AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="b565b-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="b565b-116">5. Извлечение брандмауэра и добавление коллекции правил сети в брандмауэр</span><span class="sxs-lookup"><span data-stu-id="b565b-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="b565b-117">В этом примере мы извлекаем брандмауэр, а затем добавляем в брандмауэр коллекцию правил сети с помощью метода вызова AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="b565b-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="b565b-118">6. Получение брандмауэра и получение коллекции правил приложения по имени из брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b565b-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="b565b-119">В этом примере получается брандмауэр, а затем по имени получается набор правил метод GetApplicationRuleCollectionByName в объекте брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b565b-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="b565b-120">Имя коллекции правил для метода GetApplicationRuleCollectionByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b565b-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="b565b-121">7. Извлечение брандмауэра и извлечение коллекции правил сети по имени из брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b565b-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="b565b-122">В этом примере получается брандмауэр, а затем по имени получается набор правил методов GetNetworkRuleCollectionByName в объекте брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b565b-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="b565b-123">Имя коллекции правил для метода GetNetworkRuleCollectionByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b565b-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="b565b-124">8. Получение брандмауэра и удаление коллекции правил приложения по имени из брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b565b-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="b565b-125">В этом примере извлекает брандмауэр, а затем удаляет коллекцию правил по имени, методу RemoveApplicationRuleCollectionByName в объекте брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b565b-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="b565b-126">Имя коллекции правил для метода RemoveApplicationRuleCollectionByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b565b-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="b565b-127">9. Извлечение брандмауэра и удаление коллекции правил сети по имени из брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b565b-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="b565b-128">В этом примере извлекает брандмауэр, а затем удаляет коллекцию правил по имени — методу RemoveNetworkRuleCollectionByName в объекте брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b565b-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="b565b-129">Имя коллекции правил для метода RemoveNetworkRuleCollectionByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b565b-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="b565b-130">10. Извлечение брандмауэра и выделение брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b565b-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="b565b-131">В этом примере извлекает брандмауэр и вызывает "Выделить" в брандмауэре, чтобы запустить службу брандмауэра с использованием конфигурации (коллекций правил приложений и правил сети), связанной с брандмауэром.</span><span class="sxs-lookup"><span data-stu-id="b565b-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="b565b-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b565b-132">PARAMETERS</span></span>

### <span data-ttu-id="b565b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b565b-133">-DefaultProfile</span></span>
<span data-ttu-id="b565b-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b565b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b565b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="b565b-135">-Name</span></span>
<span data-ttu-id="b565b-136">Указывает имя брандмауэра, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b565b-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b565b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b565b-137">-ResourceGroupName</span></span>
<span data-ttu-id="b565b-138">Имя группы ресурсов, к которой принадлежит брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="b565b-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b565b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b565b-139">CommonParameters</span></span>
<span data-ttu-id="b565b-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b565b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b565b-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b565b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b565b-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b565b-142">INPUTS</span></span>

### <span data-ttu-id="b565b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b565b-143">System.String</span></span>

## <span data-ttu-id="b565b-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b565b-144">OUTPUTS</span></span>

### <span data-ttu-id="b565b-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b565b-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="b565b-146">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b565b-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b565b-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b565b-147">NOTES</span></span>

## <span data-ttu-id="b565b-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b565b-148">RELATED LINKS</span></span>

[<span data-ttu-id="b565b-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b565b-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b565b-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b565b-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="b565b-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b565b-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
