---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: bb937dab16e30eba28b247d5010e3fa8fcc37954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979464"
---
# <span data-ttu-id="cae31-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cae31-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="cae31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cae31-102">SYNOPSIS</span></span>
<span data-ttu-id="cae31-103">Настраивает подключение виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="cae31-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="cae31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cae31-104">SYNTAX</span></span>

### <span data-ttu-id="cae31-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cae31-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae31-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="cae31-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae31-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cae31-107">DESCRIPTION</span></span>
<span data-ttu-id="cae31-108">Командлет **Set-AzVirtualNetworkGatewayConnection** настраивает подключение виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="cae31-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="cae31-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cae31-109">EXAMPLES</span></span>

### <span data-ttu-id="cae31-110">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="cae31-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="cae31-111">Пример 2. Добавление и обновление тегов в существующую надстройку VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cae31-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="cae31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cae31-112">PARAMETERS</span></span>

### <span data-ttu-id="cae31-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cae31-113">-AsJob</span></span>
<span data-ttu-id="cae31-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cae31-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cae31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae31-115">-DefaultProfile</span></span>
<span data-ttu-id="cae31-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cae31-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cae31-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="cae31-117">-EnableBgp</span></span>
<span data-ttu-id="cae31-118">Использование сеанса BGP через VPN-туннель S2S</span><span class="sxs-lookup"><span data-stu-id="cae31-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="cae31-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="cae31-120">Время обнаружения неавтных подключений за считанные секунды</span><span class="sxs-lookup"><span data-stu-id="cae31-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-121">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="cae31-121">-ConnectionMode</span></span>
<span data-ttu-id="cae31-122">Режим подключения виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="cae31-122">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cae31-123">-Force</span></span>
<span data-ttu-id="cae31-124">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cae31-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cae31-125">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="cae31-125">-IpsecPolicies</span></span>
<span data-ttu-id="cae31-126">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="cae31-126">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="cae31-127">-Tag</span></span>
<span data-ttu-id="cae31-128">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="cae31-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-129">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="cae31-129">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="cae31-130">Список политик выбора трафика.</span><span class="sxs-lookup"><span data-stu-id="cae31-130">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="cae31-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="cae31-132">Использование PrivateIP для подключения к S2S</span><span class="sxs-lookup"><span data-stu-id="cae31-132">Whether to use PrivateIP for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="cae31-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="cae31-134">Следует ли использовать селекторы трафика на основе политики для подключения К2S</span><span class="sxs-lookup"><span data-stu-id="cae31-134">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-135">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cae31-135">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="cae31-136">Указывает объект PSVirtualNetworkGatewayConnection, который используется этим командлетом для изменения подключения виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="cae31-136">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cae31-137">-Confirm</span></span>
<span data-ttu-id="cae31-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae31-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae31-139">-WhatIf</span></span>
<span data-ttu-id="cae31-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae31-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae31-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cae31-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae31-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae31-142">CommonParameters</span></span>
<span data-ttu-id="cae31-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae31-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae31-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae31-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae31-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cae31-145">INPUTS</span></span>

### <span data-ttu-id="cae31-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cae31-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="cae31-147">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cae31-147">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cae31-148">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="cae31-148">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="cae31-149">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="cae31-149">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="cae31-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cae31-150">OUTPUTS</span></span>

### <span data-ttu-id="cae31-151">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cae31-151">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="cae31-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cae31-152">NOTES</span></span>

## <span data-ttu-id="cae31-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cae31-153">RELATED LINKS</span></span>

[<span data-ttu-id="cae31-154">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cae31-154">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cae31-155">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cae31-155">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cae31-156">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cae31-156">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


