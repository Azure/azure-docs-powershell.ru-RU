---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 15023fbbb0576f99f66519198c893080ebe1c92f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729961"
---
# <span data-ttu-id="a0d6c-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0d6c-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="a0d6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d6c-103">Настройка подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="a0d6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0d6c-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d6c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d6c-106">Командлет **Set-AzVirtualNetworkGatewayConnection** настраивает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="a0d6c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0d6c-107">EXAMPLES</span></span>

### <span data-ttu-id="a0d6c-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="a0d6c-108">Example 1:</span></span>
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

## <span data-ttu-id="a0d6c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0d6c-109">PARAMETERS</span></span>

### <span data-ttu-id="a0d6c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0d6c-110">-AsJob</span></span>
<span data-ttu-id="a0d6c-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a0d6c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0d6c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d6c-112">-DefaultProfile</span></span>
<span data-ttu-id="a0d6c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0d6c-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="a0d6c-114">-EnableBgp</span></span>
<span data-ttu-id="a0d6c-115">Необходимость использования сеанса BGP через туннель VPN S2S</span><span class="sxs-lookup"><span data-stu-id="a0d6c-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="a0d6c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a0d6c-116">-Force</span></span>
<span data-ttu-id="a0d6c-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0d6c-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="a0d6c-118">-IpsecPolicies</span></span>
<span data-ttu-id="a0d6c-119">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="a0d6c-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="a0d6c-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="a0d6c-121">Следует ли использовать селекторы трафика на основе политики для S2S-соединения</span><span class="sxs-lookup"><span data-stu-id="a0d6c-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="a0d6c-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0d6c-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="a0d6c-123">Указывает объект PSVirtualNetworkGatewayConnection, используемый этим командлетом для изменения подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="a0d6c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0d6c-124">-Confirm</span></span>
<span data-ttu-id="a0d6c-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d6c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d6c-126">-WhatIf</span></span>
<span data-ttu-id="a0d6c-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d6c-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d6c-129">CommonParameters</span></span>
<span data-ttu-id="a0d6c-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0d6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d6c-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d6c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d6c-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0d6c-132">INPUTS</span></span>

### <span data-ttu-id="a0d6c-133">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0d6c-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="a0d6c-134">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a0d6c-134">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a0d6c-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="a0d6c-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="a0d6c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0d6c-136">OUTPUTS</span></span>

### <span data-ttu-id="a0d6c-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0d6c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="a0d6c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0d6c-138">NOTES</span></span>

## <span data-ttu-id="a0d6c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0d6c-139">RELATED LINKS</span></span>

[<span data-ttu-id="a0d6c-140">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0d6c-140">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a0d6c-141">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0d6c-141">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a0d6c-142">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0d6c-142">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


