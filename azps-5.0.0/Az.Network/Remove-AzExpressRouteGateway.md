---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245960"
---
# <span data-ttu-id="1774e-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="1774e-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="1774e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1774e-102">SYNOPSIS</span></span>
<span data-ttu-id="1774e-103">Командлет Remove-AzExpressRouteGateway удаляет шлюз Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1774e-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="1774e-104">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="1774e-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="1774e-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1774e-105">SYNTAX</span></span>

### <span data-ttu-id="1774e-106">ByExpressRouteGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1774e-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1774e-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="1774e-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1774e-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="1774e-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1774e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1774e-109">DESCRIPTION</span></span>
<span data-ttu-id="1774e-110">Командлет Remove-AzExpressRouteGateway удаляет шлюз Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1774e-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="1774e-111">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="1774e-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="1774e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1774e-112">EXAMPLES</span></span>

### <span data-ttu-id="1774e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1774e-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="1774e-114">Этот пример создает группу ресурсов, виртуальную глобальную сеть, виртуальный концентратор, масштабируемый шлюз ExpressRoute в центральной стране США и сразу же удаляет его.</span><span class="sxs-lookup"><span data-stu-id="1774e-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="1774e-115">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="1774e-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="1774e-116">Это приведет к удалению ExpressRouteGateway и всех ExpressRouteConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="1774e-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="1774e-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1774e-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="1774e-118">В этом примере создается группа ресурсов, виртуальная сеть глобальной сети, виртуальный концентратор, масштабируемый шлюз ExpressRoute и сразу же удаляются.</span><span class="sxs-lookup"><span data-stu-id="1774e-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="1774e-119">Это удаление выполняется с помощью оболочки PowerShell, в которой используется объект ExpressRouteGateway, возвращенный командой "Get-AzExpressRouteGateway".</span><span class="sxs-lookup"><span data-stu-id="1774e-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="1774e-120">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="1774e-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="1774e-121">Это приведет к удалению ExpressRouteGateway и всех ExpressRouteConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="1774e-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="1774e-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1774e-122">PARAMETERS</span></span>

### <span data-ttu-id="1774e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1774e-123">-DefaultProfile</span></span>
<span data-ttu-id="1774e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1774e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1774e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1774e-125">-Force</span></span>
<span data-ttu-id="1774e-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1774e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1774e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1774e-127">-InputObject</span></span>
<span data-ttu-id="1774e-128">Объект ExpressRouteGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1774e-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="1774e-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1774e-129">-Name</span></span>
<span data-ttu-id="1774e-130">Имя ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="1774e-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="1774e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1774e-131">-PassThru</span></span>
<span data-ttu-id="1774e-132">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1774e-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1774e-133">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1774e-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1774e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1774e-134">-ResourceGroupName</span></span>
<span data-ttu-id="1774e-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1774e-135">The resource group name.</span></span>

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

### <span data-ttu-id="1774e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1774e-136">-ResourceId</span></span>
<span data-ttu-id="1774e-137">Идентификатор ресурса Azure для ExpressRouteGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1774e-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="1774e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1774e-138">-Confirm</span></span>
<span data-ttu-id="1774e-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1774e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1774e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1774e-140">-WhatIf</span></span>
<span data-ttu-id="1774e-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1774e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1774e-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1774e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1774e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1774e-143">CommonParameters</span></span>
<span data-ttu-id="1774e-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1774e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1774e-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1774e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1774e-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1774e-146">INPUTS</span></span>

### <span data-ttu-id="1774e-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="1774e-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="1774e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1774e-148">System.String</span></span>

## <span data-ttu-id="1774e-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1774e-149">OUTPUTS</span></span>

### <span data-ttu-id="1774e-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1774e-150">System.Boolean</span></span>

## <span data-ttu-id="1774e-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="1774e-151">NOTES</span></span>

## <span data-ttu-id="1774e-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1774e-152">RELATED LINKS</span></span>
