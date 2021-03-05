---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: faa634facf6baa8d0d55490ec32a9395feaea5db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963987"
---
# <span data-ttu-id="ef4df-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="ef4df-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="ef4df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef4df-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4df-103">Обновляет шлюз ExpressRoute в масштабируемом масштабе.</span><span class="sxs-lookup"><span data-stu-id="ef4df-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="ef4df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef4df-104">SYNTAX</span></span>

### <span data-ttu-id="ef4df-105">ByExpressRouteGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef4df-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef4df-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ef4df-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef4df-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ef4df-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef4df-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef4df-108">DESCRIPTION</span></span>

<span data-ttu-id="ef4df-109">Командлет **Set-AzExpressRouteGateway** позволяет обновить единицы масштаба для существующей версии ExpressRouteGateway или обновить теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef4df-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="ef4df-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef4df-110">EXAMPLES</span></span>

### <span data-ttu-id="ef4df-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef4df-111">Example 1</span></span>

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

<span data-ttu-id="ef4df-112">Выше будет создаваться группа ресурсов Virtual WAN, Виртуальная сеть, Виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4df-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ef4df-113">В этом примере в виртуальном центре будет создан шлюз ExpressRoute с 2-масштабными единицами, которые затем будут изменены на трехмерные единицы.</span><span class="sxs-lookup"><span data-stu-id="ef4df-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="ef4df-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef4df-114">PARAMETERS</span></span>

### <span data-ttu-id="ef4df-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef4df-115">-AsJob</span></span>
<span data-ttu-id="ef4df-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ef4df-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef4df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4df-117">-DefaultProfile</span></span>
<span data-ttu-id="ef4df-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4df-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4df-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef4df-119">-InputObject</span></span>
<span data-ttu-id="ef4df-120">ExpressRouteGateway, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="ef4df-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="ef4df-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="ef4df-121">-MaxScaleUnits</span></span>
<span data-ttu-id="ef4df-122">Максимальное количество единиц масштаба для этой темы ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ef4df-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="ef4df-123">Допустимый диапазон > 2</span><span class="sxs-lookup"><span data-stu-id="ef4df-123">Valid range > 2</span></span>

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

### <span data-ttu-id="ef4df-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="ef4df-124">-MinScaleUnits</span></span>
<span data-ttu-id="ef4df-125">Минимальное количество единиц масштаба для этого проекта ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ef4df-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="ef4df-126">Допустимый диапазон > 2</span><span class="sxs-lookup"><span data-stu-id="ef4df-126">Valid range > 2</span></span>

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

### <span data-ttu-id="ef4df-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ef4df-127">-Name</span></span>
<span data-ttu-id="ef4df-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef4df-128">The resource name.</span></span>

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

### <span data-ttu-id="ef4df-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4df-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef4df-130">Имя группы ресурсов ExpressRouteGateway, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="ef4df-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="ef4df-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef4df-131">-ResourceId</span></span>
<span data-ttu-id="ef4df-132">ИД ExpressRouteGateway, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="ef4df-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="ef4df-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef4df-133">-Tag</span></span>
<span data-ttu-id="ef4df-134">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="ef4df-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ef4df-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef4df-135">-Confirm</span></span>
<span data-ttu-id="ef4df-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ef4df-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef4df-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef4df-137">-WhatIf</span></span>
<span data-ttu-id="ef4df-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef4df-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef4df-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ef4df-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef4df-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4df-140">CommonParameters</span></span>
<span data-ttu-id="ef4df-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4df-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4df-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4df-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4df-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef4df-143">INPUTS</span></span>

### <span data-ttu-id="ef4df-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ef4df-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ef4df-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ef4df-145">System.String</span></span>

## <span data-ttu-id="ef4df-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef4df-146">OUTPUTS</span></span>

### <span data-ttu-id="ef4df-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="ef4df-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="ef4df-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef4df-148">NOTES</span></span>

## <span data-ttu-id="ef4df-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef4df-149">RELATED LINKS</span></span>
