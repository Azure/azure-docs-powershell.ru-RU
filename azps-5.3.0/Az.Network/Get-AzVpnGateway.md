---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: b6537b9b8501aa2ec0aa76c9ede080893bf136ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421999"
---
# <span data-ttu-id="5bd3e-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5bd3e-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="5bd3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd3e-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd3e-103">Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName OR, где перечислены все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="5bd3e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5bd3e-104">SYNTAX</span></span>

### <span data-ttu-id="5bd3e-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5bd3e-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bd3e-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd3e-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bd3e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bd3e-107">DESCRIPTION</span></span>
<span data-ttu-id="5bd3e-108">Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName OR, где перечислены все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="5bd3e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5bd3e-109">EXAMPLES</span></span>

### <span data-ttu-id="5bd3e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5bd3e-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="5bd3e-111">Выше будет создаваться группа ресурсов Virtual WAN, Виртуальная сеть, Виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5bd3e-112">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5bd3e-113">Затем она получает VpnGateway, используя имя группы ресурсов и имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="5bd3e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5bd3e-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="5bd3e-115">Этот cmdlet возвращает все шлюзы, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="5bd3e-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="5bd3e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bd3e-116">PARAMETERS</span></span>

### <span data-ttu-id="5bd3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd3e-117">-DefaultProfile</span></span>
<span data-ttu-id="5bd3e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bd3e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5bd3e-119">-Name</span></span>
<span data-ttu-id="5bd3e-120">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5bd3e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd3e-121">-ResourceGroupName</span></span>
<span data-ttu-id="5bd3e-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5bd3e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd3e-123">CommonParameters</span></span>
<span data-ttu-id="5bd3e-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd3e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd3e-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bd3e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd3e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bd3e-126">INPUTS</span></span>

### <span data-ttu-id="5bd3e-127">Нет</span><span class="sxs-lookup"><span data-stu-id="5bd3e-127">None</span></span>

## <span data-ttu-id="5bd3e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5bd3e-128">OUTPUTS</span></span>

### <span data-ttu-id="5bd3e-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5bd3e-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="5bd3e-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5bd3e-130">NOTES</span></span>

## <span data-ttu-id="5bd3e-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bd3e-131">RELATED LINKS</span></span>

[<span data-ttu-id="5bd3e-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5bd3e-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="5bd3e-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5bd3e-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="5bd3e-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5bd3e-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
