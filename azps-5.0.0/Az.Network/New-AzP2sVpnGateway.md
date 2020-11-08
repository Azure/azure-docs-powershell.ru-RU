---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 516cd38257a8742f1bc23b3207b7e3c982d9eb36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248839"
---
# <span data-ttu-id="1d959-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1d959-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="1d959-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d959-102">SYNOPSIS</span></span>
<span data-ttu-id="1d959-103">Создайте новый P2SVpnGateway в разделе VirtualHub для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="1d959-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="1d959-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d959-104">SYNTAX</span></span>

### <span data-ttu-id="1d959-105">ByVirtualHubNameByVpnServerConfigurationObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d959-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d959-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="1d959-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d959-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="1d959-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d959-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="1d959-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d959-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="1d959-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d959-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="1d959-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d959-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d959-111">DESCRIPTION</span></span>
<span data-ttu-id="1d959-112">С помощью командлета **New-AzP2sVpnGateway** вы можете создать новый P2SVpnGateway в разделе VirtualHub, чтобы указать, что вы указываете на подключение к сайту с клиентов в Azure VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="1d959-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="1d959-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d959-113">EXAMPLES</span></span>

### <span data-ttu-id="1d959-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1d959-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "EnableInternetSecurity": True,
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="1d959-115">Командлет **New-AzP2sVpnGateway** позволяет создать новый P2SVpnGateway в разделе VirtualHub для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="1d959-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="1d959-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d959-116">PARAMETERS</span></span>

### <span data-ttu-id="1d959-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d959-117">-AsJob</span></span>
<span data-ttu-id="1d959-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1d959-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="1d959-119">-CustomDnsServer</span></span>
<span data-ttu-id="1d959-120">Список настраиваемых DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="1d959-120">The list of Custom Dns Servers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d959-121">-DefaultProfile</span></span>
<span data-ttu-id="1d959-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d959-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d959-123">-Name</span></span>
<span data-ttu-id="1d959-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1d959-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d959-125">-ResourceGroupName</span></span>
<span data-ttu-id="1d959-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1d959-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="1d959-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="1d959-128">Включить флаг безопасности Интернета для этого подключения P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1d959-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d959-129">-RoutingConfiguration</span></span>
<span data-ttu-id="1d959-130">Настройка маршрутизации для этого подключения</span><span class="sxs-lookup"><span data-stu-id="1d959-130">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="1d959-131">-Tag</span></span>
<span data-ttu-id="1d959-132">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d959-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="1d959-133">-VirtualHub</span></span>
<span data-ttu-id="1d959-134">VirtualHub, с которым должен быть связан этот P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1d959-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-135">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="1d959-135">-VirtualHubId</span></span>
<span data-ttu-id="1d959-136">Идентификатор VirtualHub, с которым должен быть связан этот P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1d959-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-137">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="1d959-137">-VirtualHubName</span></span>
<span data-ttu-id="1d959-138">Идентификатор VirtualHub, с которым должен быть связан этот P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1d959-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="1d959-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="1d959-140">P2S VpnClient AddressPool для этого P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1d959-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="1d959-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="1d959-142">Единица масштабирования для этого P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1d959-142">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-143">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d959-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="1d959-144">VpnServerConfiguration, который нужно прикрепить к этому P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1d959-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1d959-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="1d959-146">Идентификатор объекта конфигурации VPN-сервера, к которому будет присоединен этот P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1d959-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d959-147">-Confirm</span></span>
<span data-ttu-id="1d959-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1d959-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d959-149">-WhatIf</span></span>
<span data-ttu-id="1d959-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1d959-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d959-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1d959-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d959-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d959-152">CommonParameters</span></span>
<span data-ttu-id="1d959-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d959-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d959-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d959-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d959-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d959-155">INPUTS</span></span>

### <span data-ttu-id="1d959-156">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1d959-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="1d959-157">System. String Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d959-157">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="1d959-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d959-158">OUTPUTS</span></span>

### <span data-ttu-id="1d959-159">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1d959-159">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="1d959-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d959-160">NOTES</span></span>

## <span data-ttu-id="1d959-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d959-161">RELATED LINKS</span></span>

[<span data-ttu-id="1d959-162">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d959-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
