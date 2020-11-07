---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 6aabba5154e14f3af0ccfff20569c0cdc51a2578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730349"
---
# <span data-ttu-id="33205-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="33205-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="33205-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33205-102">SYNOPSIS</span></span>
<span data-ttu-id="33205-103">Создает масштабируемый шлюз ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="33205-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="33205-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33205-104">SYNTAX</span></span>

### <span data-ttu-id="33205-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33205-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33205-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="33205-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33205-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="33205-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33205-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33205-108">DESCRIPTION</span></span>

<span data-ttu-id="33205-109">New-AzExpressRouteGateway создает масштабируемый шлюз ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="33205-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="33205-110">Это программное обеспечение связи для Azure внутри VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="33205-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="33205-111">Этот шлюз может масштабироваться с учетом единиц масштабирования, указанных в этом или Set-AzExpressRouteGatewayом командлете.</span><span class="sxs-lookup"><span data-stu-id="33205-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="33205-112">Соединение настраивается с помощью локального канала ExpressRoute на масштабируемый шлюз.</span><span class="sxs-lookup"><span data-stu-id="33205-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="33205-113">ExpressRouteGateway будет находиться в той же папке, что и VirtualHub, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="33205-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="33205-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33205-114">EXAMPLES</span></span>

### <span data-ttu-id="33205-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33205-115">Example 1</span></span>

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

<span data-ttu-id="33205-116">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="33205-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="33205-117">Шлюз ExpressRoute будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="33205-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="33205-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33205-118">PARAMETERS</span></span>

### <span data-ttu-id="33205-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33205-119">-AsJob</span></span>
<span data-ttu-id="33205-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="33205-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33205-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33205-121">-DefaultProfile</span></span>
<span data-ttu-id="33205-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33205-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33205-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="33205-123">-MaxScaleUnits</span></span>
<span data-ttu-id="33205-124">Максимальное количество единиц масштабирования для этого ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="33205-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="33205-125">Допустимый диапазон > 2</span><span class="sxs-lookup"><span data-stu-id="33205-125">Valid range > 2</span></span>

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

### <span data-ttu-id="33205-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="33205-126">-MinScaleUnits</span></span>
<span data-ttu-id="33205-127">Минимальное количество единиц масштаба для этого ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="33205-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="33205-128">Допустимый диапазон > 2</span><span class="sxs-lookup"><span data-stu-id="33205-128">Valid range > 2</span></span>

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

### <span data-ttu-id="33205-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="33205-129">-Name</span></span>
<span data-ttu-id="33205-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="33205-130">The resource name.</span></span>

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

### <span data-ttu-id="33205-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33205-131">-ResourceGroupName</span></span>
<span data-ttu-id="33205-132">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="33205-132">The resource name.</span></span>

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

### <span data-ttu-id="33205-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="33205-133">-Tag</span></span>
<span data-ttu-id="33205-134">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33205-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="33205-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="33205-135">-VirtualHub</span></span>
<span data-ttu-id="33205-136">VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="33205-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="33205-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="33205-137">-VirtualHubId</span></span>
<span data-ttu-id="33205-138">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="33205-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="33205-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="33205-139">-VirtualHubName</span></span>
<span data-ttu-id="33205-140">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="33205-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="33205-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33205-141">-Confirm</span></span>
<span data-ttu-id="33205-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="33205-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33205-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33205-143">-WhatIf</span></span>
<span data-ttu-id="33205-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="33205-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33205-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="33205-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33205-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33205-146">CommonParameters</span></span>
<span data-ttu-id="33205-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33205-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33205-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33205-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33205-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33205-149">INPUTS</span></span>

### <span data-ttu-id="33205-150">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33205-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="33205-151">System. String</span><span class="sxs-lookup"><span data-stu-id="33205-151">System.String</span></span>

## <span data-ttu-id="33205-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33205-152">OUTPUTS</span></span>

### <span data-ttu-id="33205-153">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="33205-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="33205-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="33205-154">NOTES</span></span>

## <span data-ttu-id="33205-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33205-155">RELATED LINKS</span></span>
