---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c7f7f8603c03300f4f1df1d47a62ed35ca3b93d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392295"
---
# <span data-ttu-id="b0014-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b0014-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b0014-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0014-102">SYNOPSIS</span></span>
<span data-ttu-id="b0014-103">Настраивает подключение виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="b0014-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="b0014-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0014-104">SYNTAX</span></span>

### <span data-ttu-id="b0014-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0014-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0014-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="b0014-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0014-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0014-107">DESCRIPTION</span></span>
<span data-ttu-id="b0014-108">Командлет **Set-AzVirtualNetworkGatewayConnection** настраивает подключение виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="b0014-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="b0014-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0014-109">EXAMPLES</span></span>

### <span data-ttu-id="b0014-110">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="b0014-110">Example 1:</span></span>
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

### <span data-ttu-id="b0014-111">Пример 2. Добавление и обновление тегов в существующую надстройку VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b0014-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
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

## <span data-ttu-id="b0014-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0014-112">PARAMETERS</span></span>

### <span data-ttu-id="b0014-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0014-113">-AsJob</span></span>
<span data-ttu-id="b0014-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b0014-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0014-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0014-115">-DefaultProfile</span></span>
<span data-ttu-id="b0014-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0014-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0014-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="b0014-117">-EnableBgp</span></span>
<span data-ttu-id="b0014-118">Использование сеанса BGP через VPN-туннель S2S</span><span class="sxs-lookup"><span data-stu-id="b0014-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="b0014-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="b0014-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="b0014-120">Время обнаружения за считанные секунды при обнаружении неавтных подключений</span><span class="sxs-lookup"><span data-stu-id="b0014-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="b0014-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b0014-121">-Force</span></span>
<span data-ttu-id="b0014-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b0014-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b0014-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="b0014-123">-IpsecPolicies</span></span>
<span data-ttu-id="b0014-124">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="b0014-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="b0014-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b0014-125">-Tag</span></span>
<span data-ttu-id="b0014-126">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="b0014-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b0014-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b0014-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="b0014-128">Список политик выбора трафика.</span><span class="sxs-lookup"><span data-stu-id="b0014-128">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="b0014-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0014-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="b0014-130">Использование PrivateIP для подключения к S2S</span><span class="sxs-lookup"><span data-stu-id="b0014-130">Whether to use PrivateIP for a S2S connection</span></span>

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

### <span data-ttu-id="b0014-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="b0014-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="b0014-132">Следует ли использовать селекторы трафика на основе политики для подключения К2S</span><span class="sxs-lookup"><span data-stu-id="b0014-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="b0014-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b0014-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="b0014-134">Указывает объект PSVirtualNetworkGatewayConnection, который используется этим командлетом для изменения подключения виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="b0014-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="b0014-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0014-135">-Confirm</span></span>
<span data-ttu-id="b0014-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0014-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0014-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0014-137">-WhatIf</span></span>
<span data-ttu-id="b0014-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0014-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0014-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b0014-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0014-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0014-140">CommonParameters</span></span>
<span data-ttu-id="b0014-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0014-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0014-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0014-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0014-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0014-143">INPUTS</span></span>

### <span data-ttu-id="b0014-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b0014-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="b0014-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b0014-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b0014-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="b0014-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="b0014-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="b0014-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="b0014-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0014-148">OUTPUTS</span></span>

### <span data-ttu-id="b0014-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b0014-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b0014-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0014-150">NOTES</span></span>

## <span data-ttu-id="b0014-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0014-151">RELATED LINKS</span></span>

[<span data-ttu-id="b0014-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b0014-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b0014-153">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b0014-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b0014-154">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b0014-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


