---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 71fff2d475c5cf3045be8aa4c628776b0dd42dc7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244149"
---
# <span data-ttu-id="b2850-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b2850-101">Get-AzFirewall</span></span>

## <span data-ttu-id="b2850-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2850-102">SYNOPSIS</span></span>
<span data-ttu-id="b2850-103">Получает брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="b2850-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="b2850-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2850-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2850-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2850-105">DESCRIPTION</span></span>
<span data-ttu-id="b2850-106">Командлет **Get-AzFirewall** получает один или несколько брандмауэров в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2850-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="b2850-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2850-107">EXAMPLES</span></span>

### <span data-ttu-id="b2850-108">1: получение всех брандмауэров в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b2850-108">1:  Retrieve all Firewalls in a resource group</span></span>
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

<span data-ttu-id="b2850-109">В этом примере извлекаются все брандмауэры в группе ресурсов "rgName".</span><span class="sxs-lookup"><span data-stu-id="b2850-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="b2850-110">2. Загрузка брандмауэра по имени</span><span class="sxs-lookup"><span data-stu-id="b2850-110">2:  Retrieve a Firewall by name</span></span>
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

<span data-ttu-id="b2850-111">В этом примере извлекается брандмауэр с именем "azFw" в группе ресурсов "rgName".</span><span class="sxs-lookup"><span data-stu-id="b2850-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="b2850-112">3. получение всех брандмауэров с фильтрацией</span><span class="sxs-lookup"><span data-stu-id="b2850-112">3:  Retrieve all Firewalls with filtering</span></span>
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

<span data-ttu-id="b2850-113">В этом примере извлекаются все брандмауэры, которые начинаются с "azFw".</span><span class="sxs-lookup"><span data-stu-id="b2850-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="b2850-114">4. получение доступа к брандмауэру и Добавление набора правил приложения в брандмауэр</span><span class="sxs-lookup"><span data-stu-id="b2850-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="b2850-115">В этом примере извлекается брандмауэр, после чего в брандмауэр добавляется коллекция правил приложений, вызывая метод AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="b2850-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="b2850-116">5. Извлеките брандмауэр и добавьте в брандмауэр коллекцию сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="b2850-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="b2850-117">В этом примере извлекается брандмауэр, после чего в брандмауэр добавляется коллекция сетевых правил, вызывая метод AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="b2850-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="b2850-118">6. получение доступа к брандмауэру и получение набора правил приложения по имени из брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b2850-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="b2850-119">В этом примере извлекается брандмауэр и затем получается коллекция правил по имени, вызывающему метод GetApplicationRuleCollectionByName для объекта Firewall.</span><span class="sxs-lookup"><span data-stu-id="b2850-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="b2850-120">Имя набора правил для метода GetApplicationRuleCollectionByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="b2850-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="b2850-121">7. получение брандмауэра и получение из него коллекции сетевых правил по имени.</span><span class="sxs-lookup"><span data-stu-id="b2850-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="b2850-122">В этом примере извлекается брандмауэр и затем получается коллекция правил по имени, вызывающему метод GetNetworkRuleCollectionByName для объекта Firewall.</span><span class="sxs-lookup"><span data-stu-id="b2850-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="b2850-123">Имя набора правил для метода GetNetworkRuleCollectionByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="b2850-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="b2850-124">8. получение брандмауэра и удаление набора правил приложения по имени из брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b2850-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="b2850-125">В этом примере извлекается брандмауэр, после чего коллекция правил удаляется по имени, вызывая метод RemoveApplicationRuleCollectionByName для объекта Firewall.</span><span class="sxs-lookup"><span data-stu-id="b2850-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="b2850-126">Имя набора правил для метода RemoveApplicationRuleCollectionByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="b2850-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="b2850-127">9. Извлеките брандмауэр и удалите из него коллекцию сетевых правил по имени.</span><span class="sxs-lookup"><span data-stu-id="b2850-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="b2850-128">В этом примере извлекается брандмауэр, после чего коллекция правил удаляется по имени, вызывая метод RemoveNetworkRuleCollectionByName для объекта Firewall.</span><span class="sxs-lookup"><span data-stu-id="b2850-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="b2850-129">Имя набора правил для метода RemoveNetworkRuleCollectionByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="b2850-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="b2850-130">10: получение брандмауэра и его выделение</span><span class="sxs-lookup"><span data-stu-id="b2850-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="b2850-131">В этом примере извлекается брандмауэр и вызываются функции выделения ресурсов в брандмауэре, чтобы запустить службу брандмауэра с помощью конфигурации (коллекций приложений и сетевых правил), связанных с брандмауэром.</span><span class="sxs-lookup"><span data-stu-id="b2850-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="b2850-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2850-132">PARAMETERS</span></span>

### <span data-ttu-id="b2850-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2850-133">-DefaultProfile</span></span>
<span data-ttu-id="b2850-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2850-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2850-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2850-135">-Name</span></span>
<span data-ttu-id="b2850-136">Указывает имя брандмауэра, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b2850-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b2850-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2850-137">-ResourceGroupName</span></span>
<span data-ttu-id="b2850-138">Указывает имя группы ресурсов, к которой относится брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="b2850-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

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

### <span data-ttu-id="b2850-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2850-139">CommonParameters</span></span>
<span data-ttu-id="b2850-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2850-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2850-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2850-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2850-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2850-142">INPUTS</span></span>

### <span data-ttu-id="b2850-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b2850-143">System.String</span></span>

## <span data-ttu-id="b2850-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2850-144">OUTPUTS</span></span>

### <span data-ttu-id="b2850-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b2850-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="b2850-146">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network.. PSAzureFirewall, Microsoft. Azure. PowerShell. командлеты. Network, Version = 1.0.0.0, культура = независимая, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="b2850-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b2850-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2850-147">NOTES</span></span>

## <span data-ttu-id="b2850-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2850-148">RELATED LINKS</span></span>

[<span data-ttu-id="b2850-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b2850-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b2850-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b2850-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="b2850-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b2850-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
