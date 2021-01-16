---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506903"
---
# <span data-ttu-id="a098d-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="a098d-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="a098d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a098d-102">SYNOPSIS</span></span>
<span data-ttu-id="a098d-103">Этот Remove-AzExpressRouteGateway удаляет шлюз Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a098d-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="a098d-104">Это шлюз, специфичность подключения к программному обеспечению, определяемом программным обеспечением виртуальной WAN Azure.</span><span class="sxs-lookup"><span data-stu-id="a098d-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="a098d-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a098d-105">SYNTAX</span></span>

### <span data-ttu-id="a098d-106">ByExpressRouteGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a098d-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a098d-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a098d-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a098d-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a098d-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a098d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a098d-109">DESCRIPTION</span></span>
<span data-ttu-id="a098d-110">Этот Remove-AzExpressRouteGateway удаляет шлюз Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a098d-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="a098d-111">Это шлюз, специфичность подключения к программному обеспечению, определяемом программным обеспечением виртуальной WAN Azure.</span><span class="sxs-lookup"><span data-stu-id="a098d-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="a098d-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a098d-112">EXAMPLES</span></span>

### <span data-ttu-id="a098d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a098d-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="a098d-114">В этом примере создается группа ресурсов, виртуальнаяwan, виртуальный концентратор, масштабируемый шлюз ExpressRoute в центральной части США, а затем сразу удаляется.</span><span class="sxs-lookup"><span data-stu-id="a098d-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="a098d-115">Чтобы скрыть запрос при удалении виртуального шлюза, используйте флаг -Force.</span><span class="sxs-lookup"><span data-stu-id="a098d-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="a098d-116">При этом будут удалены ExpressRouteGateway и все подключенные к нему подключения ExpressRouteConnections.</span><span class="sxs-lookup"><span data-stu-id="a098d-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="a098d-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a098d-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="a098d-118">В этом примере создается группа ресурсов, виртуальная WAN, виртуальный концентратор, масштабируемый шлюз ExpressRoute в Западной центральной части США, а затем сразу удаляется.</span><span class="sxs-lookup"><span data-stu-id="a098d-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="a098d-119">Это удаление происходит с помощью piping Powershell, который использует объект ExpressRouteGateway, Get-AzExpressRouteGateway команды.</span><span class="sxs-lookup"><span data-stu-id="a098d-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="a098d-120">Чтобы скрыть запрос при удалении виртуального шлюза, используйте флаг -Force.</span><span class="sxs-lookup"><span data-stu-id="a098d-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="a098d-121">При этом будут удалены ExpressRouteGateway и все подключенные к нему подключения ExpressRouteConnections.</span><span class="sxs-lookup"><span data-stu-id="a098d-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="a098d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a098d-122">PARAMETERS</span></span>

### <span data-ttu-id="a098d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a098d-123">-DefaultProfile</span></span>
<span data-ttu-id="a098d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a098d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a098d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a098d-125">-Force</span></span>
<span data-ttu-id="a098d-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a098d-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a098d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a098d-127">-InputObject</span></span>
<span data-ttu-id="a098d-128">Объект ExpressRouteGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a098d-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="a098d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a098d-129">-Name</span></span>
<span data-ttu-id="a098d-130">Имя ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="a098d-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a098d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a098d-131">-PassThru</span></span>
<span data-ttu-id="a098d-132">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a098d-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a098d-133">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a098d-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a098d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a098d-134">-ResourceGroupName</span></span>
<span data-ttu-id="a098d-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a098d-135">The resource group name.</span></span>

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

### <span data-ttu-id="a098d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a098d-136">-ResourceId</span></span>
<span data-ttu-id="a098d-137">Удаляемая служба ExpressRouteGateway с использованием ИД ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a098d-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="a098d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a098d-138">-Confirm</span></span>
<span data-ttu-id="a098d-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a098d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a098d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a098d-140">-WhatIf</span></span>
<span data-ttu-id="a098d-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a098d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a098d-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a098d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a098d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a098d-143">CommonParameters</span></span>
<span data-ttu-id="a098d-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a098d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a098d-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a098d-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a098d-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a098d-146">INPUTS</span></span>

### <span data-ttu-id="a098d-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="a098d-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="a098d-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a098d-148">System.String</span></span>

## <span data-ttu-id="a098d-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a098d-149">OUTPUTS</span></span>

### <span data-ttu-id="a098d-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a098d-150">System.Boolean</span></span>

## <span data-ttu-id="a098d-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a098d-151">NOTES</span></span>

## <span data-ttu-id="a098d-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a098d-152">RELATED LINKS</span></span>
