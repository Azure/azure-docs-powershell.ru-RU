---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247277"
---
# <span data-ttu-id="32d36-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="32d36-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="32d36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32d36-102">SYNOPSIS</span></span>
<span data-ttu-id="32d36-103">Получает ресурс ExpressRouteGateway с помощью ResourceGroupName и GatewayName или перечисляет все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="32d36-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="32d36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32d36-104">SYNTAX</span></span>

### <span data-ttu-id="32d36-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32d36-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32d36-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d36-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32d36-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="32d36-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32d36-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32d36-108">DESCRIPTION</span></span>
<span data-ttu-id="32d36-109">Получает ресурс ExpressRouteGateway с помощью ResourceGroupName и GatewayName или перечисляет все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="32d36-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="32d36-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32d36-110">EXAMPLES</span></span>

### <span data-ttu-id="32d36-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32d36-111">Example 1</span></span>

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

<span data-ttu-id="32d36-112">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую (Virtual HUB) в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="32d36-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="32d36-113">Шлюз ExpressRoute будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="32d36-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="32d36-114">Затем он получает ExpressRouteGateway, используя его resourceGroupName и имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="32d36-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="32d36-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32d36-115">Example 2</span></span>

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

<span data-ttu-id="32d36-116">Эта команда получит все ExpressRouteGateways, которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="32d36-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="32d36-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32d36-117">PARAMETERS</span></span>

### <span data-ttu-id="32d36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d36-118">-DefaultProfile</span></span>
<span data-ttu-id="32d36-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32d36-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32d36-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32d36-120">-Name</span></span>
<span data-ttu-id="32d36-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="32d36-121">The resource name.</span></span>

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

### <span data-ttu-id="32d36-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d36-122">-ResourceGroupName</span></span>
<span data-ttu-id="32d36-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32d36-123">The resource group name.</span></span>

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

### <span data-ttu-id="32d36-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32d36-124">-ResourceId</span></span>
<span data-ttu-id="32d36-125">Идентификатор ресурса Azure для expressRouteGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="32d36-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="32d36-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d36-126">CommonParameters</span></span>
<span data-ttu-id="32d36-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32d36-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d36-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32d36-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d36-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32d36-129">INPUTS</span></span>

### <span data-ttu-id="32d36-130">System. String</span><span class="sxs-lookup"><span data-stu-id="32d36-130">System.String</span></span>

## <span data-ttu-id="32d36-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32d36-131">OUTPUTS</span></span>

### <span data-ttu-id="32d36-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="32d36-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="32d36-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="32d36-133">NOTES</span></span>

## <span data-ttu-id="32d36-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32d36-134">RELATED LINKS</span></span>
