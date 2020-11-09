---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: 7cc9dbe5c4727c283ead66e88b6c52c9c2fcd00e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244065"
---
# <span data-ttu-id="72535-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="72535-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="72535-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72535-102">SYNOPSIS</span></span>
<span data-ttu-id="72535-103">Обновляет масштабируемый шлюз ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="72535-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="72535-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72535-104">SYNTAX</span></span>

### <span data-ttu-id="72535-105">ByExpressRouteGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72535-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72535-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="72535-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72535-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="72535-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72535-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72535-108">DESCRIPTION</span></span>

<span data-ttu-id="72535-109">Set-AzExpressRouteGateway обновляет единицы масштабирования для ExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="72535-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="72535-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72535-110">EXAMPLES</span></span>

### <span data-ttu-id="72535-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72535-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="72535-112">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="72535-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="72535-113">Шлюз ExpressRoute будет создан на виртуальном концентраторе с двумя единицами масштабирования, которые затем будут изменены на 3 единицы измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="72535-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="72535-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72535-114">PARAMETERS</span></span>

### <span data-ttu-id="72535-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72535-115">-AsJob</span></span>
<span data-ttu-id="72535-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="72535-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72535-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72535-117">-DefaultProfile</span></span>
<span data-ttu-id="72535-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72535-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72535-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72535-119">-InputObject</span></span>
<span data-ttu-id="72535-120">ExpressRouteGateway, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="72535-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72535-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="72535-121">-MaxScaleUnits</span></span>
<span data-ttu-id="72535-122">Максимальное количество единиц масштабирования для этого ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="72535-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="72535-123">Допустимый диапазон > 2</span><span class="sxs-lookup"><span data-stu-id="72535-123">Valid range > 2</span></span>

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

### <span data-ttu-id="72535-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="72535-124">-MinScaleUnits</span></span>
<span data-ttu-id="72535-125">Минимальное количество единиц масштаба для этого ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="72535-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="72535-126">Допустимый диапазон > 2</span><span class="sxs-lookup"><span data-stu-id="72535-126">Valid range > 2</span></span>

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

### <span data-ttu-id="72535-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72535-127">-Name</span></span>
<span data-ttu-id="72535-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="72535-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72535-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72535-129">-ResourceGroupName</span></span>
<span data-ttu-id="72535-130">Имя группы ресурсов для ExpressRouteGateway, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="72535-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72535-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72535-131">-ResourceId</span></span>
<span data-ttu-id="72535-132">Идентификатор ExpressRouteGateway, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="72535-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72535-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="72535-133">-Tag</span></span>
<span data-ttu-id="72535-134">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72535-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="72535-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72535-135">-Confirm</span></span>
<span data-ttu-id="72535-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="72535-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72535-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72535-137">-WhatIf</span></span>
<span data-ttu-id="72535-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="72535-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72535-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="72535-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72535-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72535-140">CommonParameters</span></span>
<span data-ttu-id="72535-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72535-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72535-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72535-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72535-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72535-143">INPUTS</span></span>

### <span data-ttu-id="72535-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="72535-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="72535-145">System. String</span><span class="sxs-lookup"><span data-stu-id="72535-145">System.String</span></span>

## <span data-ttu-id="72535-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72535-146">OUTPUTS</span></span>

### <span data-ttu-id="72535-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="72535-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="72535-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="72535-148">NOTES</span></span>

## <span data-ttu-id="72535-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72535-149">RELATED LINKS</span></span>