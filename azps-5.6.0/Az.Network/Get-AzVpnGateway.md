---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: e03e14a3327f0e3eaf91131208653bbaaa2fc0c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965715"
---
# <span data-ttu-id="add83-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="add83-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="add83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="add83-102">SYNOPSIS</span></span>
<span data-ttu-id="add83-103">Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName OR, где перечислены все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="add83-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="add83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="add83-104">SYNTAX</span></span>

### <span data-ttu-id="add83-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="add83-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add83-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add83-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="add83-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="add83-107">DESCRIPTION</span></span>
<span data-ttu-id="add83-108">Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName OR, в который перечислены все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="add83-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="add83-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="add83-109">EXAMPLES</span></span>

### <span data-ttu-id="add83-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="add83-110">Example 1</span></span>

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

<span data-ttu-id="add83-111">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="add83-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="add83-112">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="add83-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="add83-113">Затем она получает VpnGateway, используя имя группы ресурсов и имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="add83-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="add83-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="add83-114">Example 2</span></span>

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

<span data-ttu-id="add83-115">Этот cmdlet возвращает все шлюзы, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="add83-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="add83-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="add83-116">PARAMETERS</span></span>

### <span data-ttu-id="add83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add83-117">-DefaultProfile</span></span>
<span data-ttu-id="add83-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="add83-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="add83-119">-Name</span><span class="sxs-lookup"><span data-stu-id="add83-119">-Name</span></span>
<span data-ttu-id="add83-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="add83-120">The resource name.</span></span>

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

### <span data-ttu-id="add83-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add83-121">-ResourceGroupName</span></span>
<span data-ttu-id="add83-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="add83-122">The resource group name.</span></span>

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

### <span data-ttu-id="add83-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add83-123">CommonParameters</span></span>
<span data-ttu-id="add83-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add83-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add83-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="add83-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add83-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="add83-126">INPUTS</span></span>

### <span data-ttu-id="add83-127">Нет</span><span class="sxs-lookup"><span data-stu-id="add83-127">None</span></span>

## <span data-ttu-id="add83-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="add83-128">OUTPUTS</span></span>

### <span data-ttu-id="add83-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="add83-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="add83-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="add83-130">NOTES</span></span>

## <span data-ttu-id="add83-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="add83-131">RELATED LINKS</span></span>

[<span data-ttu-id="add83-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="add83-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="add83-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="add83-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="add83-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="add83-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
