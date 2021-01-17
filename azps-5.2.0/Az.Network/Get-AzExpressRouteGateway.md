---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413708"
---
# <span data-ttu-id="75849-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="75849-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="75849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75849-102">SYNOPSIS</span></span>
<span data-ttu-id="75849-103">Возвращает ресурс ExpressRouteGateway с помощью resourceGroupName и GatewayName OR, в который перечислены все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="75849-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="75849-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75849-104">SYNTAX</span></span>

### <span data-ttu-id="75849-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75849-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75849-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75849-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75849-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="75849-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75849-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75849-108">DESCRIPTION</span></span>
<span data-ttu-id="75849-109">Возвращает ресурс ExpressRouteGateway с помощью resourceGroupName и GatewayName OR, в который перечислены все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="75849-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="75849-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75849-110">EXAMPLES</span></span>

### <span data-ttu-id="75849-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75849-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="75849-112">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор в Западной центральной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="75849-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="75849-113">После этого в виртуальном центре будет создан шлюз ExpressRoute с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="75849-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="75849-114">Затем expressRouteGateway получает его имя resourceGroupName и имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="75849-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="75849-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75849-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="75849-116">Эта команда будет получать все expressRouteGateway, которые начинаются с "test"</span><span class="sxs-lookup"><span data-stu-id="75849-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="75849-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75849-117">PARAMETERS</span></span>

### <span data-ttu-id="75849-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75849-118">-DefaultProfile</span></span>
<span data-ttu-id="75849-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75849-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75849-120">-Name</span><span class="sxs-lookup"><span data-stu-id="75849-120">-Name</span></span>
<span data-ttu-id="75849-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="75849-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="75849-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75849-122">-ResourceGroupName</span></span>
<span data-ttu-id="75849-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75849-123">The resource group name.</span></span>

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

### <span data-ttu-id="75849-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75849-124">-ResourceId</span></span>
<span data-ttu-id="75849-125">ИД ресурса Azure для expressRouteGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="75849-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75849-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75849-126">CommonParameters</span></span>
<span data-ttu-id="75849-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75849-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75849-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75849-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75849-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75849-129">INPUTS</span></span>

### <span data-ttu-id="75849-130">System.String</span><span class="sxs-lookup"><span data-stu-id="75849-130">System.String</span></span>

## <span data-ttu-id="75849-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75849-131">OUTPUTS</span></span>

### <span data-ttu-id="75849-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="75849-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="75849-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75849-133">NOTES</span></span>

## <span data-ttu-id="75849-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75849-134">RELATED LINKS</span></span>
