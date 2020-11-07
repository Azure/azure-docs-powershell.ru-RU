---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: b4b0253814c6488c5f7269c6a79d51790a2f39fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901970"
---
# <span data-ttu-id="f0860-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f0860-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="f0860-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0860-102">SYNOPSIS</span></span>
<span data-ttu-id="f0860-103">Командлет Remove-AzExpressRouteGateway удаляет шлюз Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f0860-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="f0860-104">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="f0860-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="f0860-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0860-105">SYNTAX</span></span>

### <span data-ttu-id="f0860-106">ByExpressRouteGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0860-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0860-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f0860-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0860-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f0860-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0860-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0860-109">DESCRIPTION</span></span>
<span data-ttu-id="f0860-110">Командлет Remove-AzExpressRouteGateway удаляет шлюз Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f0860-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="f0860-111">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="f0860-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="f0860-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0860-112">EXAMPLES</span></span>

### <span data-ttu-id="f0860-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0860-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="f0860-114">Этот пример создает группу ресурсов, виртуальную глобальную сеть, виртуальный концентратор, масштабируемый шлюз ExpressRoute в центральной стране США и сразу же удаляет его.</span><span class="sxs-lookup"><span data-stu-id="f0860-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="f0860-115">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="f0860-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="f0860-116">Это приведет к удалению ExpressRouteGateway и всех ExpressRouteConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="f0860-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="f0860-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f0860-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="f0860-118">В этом примере создается группа ресурсов, виртуальная сеть глобальной сети, виртуальный концентратор, масштабируемый шлюз ExpressRoute и сразу же удаляются.</span><span class="sxs-lookup"><span data-stu-id="f0860-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="f0860-119">Это удаление выполняется с помощью оболочки PowerShell, в которой используется объект ExpressRouteGateway, возвращенный командой "Get-AzExpressRouteGateway".</span><span class="sxs-lookup"><span data-stu-id="f0860-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="f0860-120">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="f0860-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="f0860-121">Это приведет к удалению ExpressRouteGateway и всех ExpressRouteConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="f0860-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="f0860-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0860-122">PARAMETERS</span></span>

### <span data-ttu-id="f0860-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0860-123">-DefaultProfile</span></span>
<span data-ttu-id="f0860-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0860-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0860-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f0860-125">-Force</span></span>
<span data-ttu-id="f0860-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f0860-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f0860-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0860-127">-InputObject</span></span>
<span data-ttu-id="f0860-128">Объект ExpressRouteGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f0860-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="f0860-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0860-129">-Name</span></span>
<span data-ttu-id="f0860-130">Имя ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="f0860-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="f0860-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0860-131">-PassThru</span></span>
<span data-ttu-id="f0860-132">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f0860-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f0860-133">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f0860-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0860-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0860-134">-ResourceGroupName</span></span>
<span data-ttu-id="f0860-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0860-135">The resource group name.</span></span>

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

### <span data-ttu-id="f0860-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0860-136">-ResourceId</span></span>
<span data-ttu-id="f0860-137">Идентификатор ресурса Azure для ExpressRouteGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f0860-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="f0860-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0860-138">-Confirm</span></span>
<span data-ttu-id="f0860-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0860-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0860-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0860-140">-WhatIf</span></span>
<span data-ttu-id="f0860-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0860-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0860-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0860-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0860-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0860-143">CommonParameters</span></span>
<span data-ttu-id="f0860-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0860-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0860-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0860-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0860-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0860-146">INPUTS</span></span>

### <span data-ttu-id="f0860-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f0860-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="f0860-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f0860-148">System.String</span></span>

## <span data-ttu-id="f0860-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0860-149">OUTPUTS</span></span>

### <span data-ttu-id="f0860-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0860-150">System.Boolean</span></span>

## <span data-ttu-id="f0860-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0860-151">NOTES</span></span>

## <span data-ttu-id="f0860-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0860-152">RELATED LINKS</span></span>
