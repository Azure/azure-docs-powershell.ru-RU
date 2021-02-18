---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218580"
---
# <span data-ttu-id="69558-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="69558-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="69558-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69558-102">SYNOPSIS</span></span>
<span data-ttu-id="69558-103">Создает шлюз ExpressRoute в масштабируемом масштабе.</span><span class="sxs-lookup"><span data-stu-id="69558-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="69558-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69558-104">SYNTAX</span></span>

### <span data-ttu-id="69558-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69558-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69558-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="69558-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69558-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="69558-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69558-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69558-108">DESCRIPTION</span></span>

<span data-ttu-id="69558-109">New-AzExpressRouteGateway создает масштабируемый шлюз ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="69558-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="69558-110">Это программное обеспечение, определяемое подключением локально к Azure в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="69558-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="69558-111">Масштаб этого шлюза можно масштабировать с учетом единицы, заданной в этом или Set-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="69558-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="69558-112">Подключение устанавливается из локального контура ExpressRoute к масштабируемого шлюзу.</span><span class="sxs-lookup"><span data-stu-id="69558-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="69558-113">ExpressRouteGateway будет расположен в том же расположении, что и ссылка на VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="69558-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="69558-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69558-114">EXAMPLES</span></span>

### <span data-ttu-id="69558-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69558-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="69558-116">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="69558-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="69558-117">В этом примере в виртуальном центре будет создан шлюз ExpressRoute с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="69558-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="69558-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69558-118">PARAMETERS</span></span>

### <span data-ttu-id="69558-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69558-119">-AsJob</span></span>
<span data-ttu-id="69558-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="69558-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69558-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69558-121">-DefaultProfile</span></span>
<span data-ttu-id="69558-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69558-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69558-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="69558-123">-MaxScaleUnits</span></span>
<span data-ttu-id="69558-124">Максимальное количество единиц масштаба для этой темы ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="69558-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="69558-125">Допустимый > 2</span><span class="sxs-lookup"><span data-stu-id="69558-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69558-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="69558-126">-MinScaleUnits</span></span>
<span data-ttu-id="69558-127">Минимальное количество единиц масштаба для этого проекта ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="69558-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="69558-128">Допустимый диапазон > 2</span><span class="sxs-lookup"><span data-stu-id="69558-128">Valid range > 2</span></span>

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

### <span data-ttu-id="69558-129">-Name</span><span class="sxs-lookup"><span data-stu-id="69558-129">-Name</span></span>
<span data-ttu-id="69558-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="69558-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69558-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69558-131">-ResourceGroupName</span></span>
<span data-ttu-id="69558-132">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="69558-132">The resource name.</span></span>

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

### <span data-ttu-id="69558-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="69558-133">-Tag</span></span>
<span data-ttu-id="69558-134">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="69558-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="69558-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="69558-135">-VirtualHub</span></span>
<span data-ttu-id="69558-136">С виртуальным ИТ-частью VpnGateway необходимо связано.</span><span class="sxs-lookup"><span data-stu-id="69558-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69558-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="69558-137">-VirtualHubId</span></span>
<span data-ttu-id="69558-138">С ИД VirtualHub этого VpnGateway необходимо связан.</span><span class="sxs-lookup"><span data-stu-id="69558-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69558-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="69558-139">-VirtualHubName</span></span>
<span data-ttu-id="69558-140">С ИД VirtualHub этого VpnGateway необходимо связан.</span><span class="sxs-lookup"><span data-stu-id="69558-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69558-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69558-141">-Confirm</span></span>
<span data-ttu-id="69558-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="69558-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69558-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69558-143">-WhatIf</span></span>
<span data-ttu-id="69558-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69558-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69558-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="69558-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69558-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69558-146">CommonParameters</span></span>
<span data-ttu-id="69558-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69558-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69558-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69558-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69558-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69558-149">INPUTS</span></span>

### <span data-ttu-id="69558-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="69558-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="69558-151">System.String</span><span class="sxs-lookup"><span data-stu-id="69558-151">System.String</span></span>

## <span data-ttu-id="69558-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69558-152">OUTPUTS</span></span>

### <span data-ttu-id="69558-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="69558-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="69558-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69558-154">NOTES</span></span>

## <span data-ttu-id="69558-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69558-155">RELATED LINKS</span></span>
