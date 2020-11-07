---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 17731d3f864f429fdad58bf767fb5cb25950387d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730085"
---
# <span data-ttu-id="7cf86-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7cf86-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="7cf86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cf86-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf86-103">Командлет Remove-AzVpnGateway удаляет шлюз Azure VPN.</span><span class="sxs-lookup"><span data-stu-id="7cf86-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="7cf86-104">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf86-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="7cf86-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cf86-105">SYNTAX</span></span>

### <span data-ttu-id="7cf86-106">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7cf86-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf86-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7cf86-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf86-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf86-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf86-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf86-109">DESCRIPTION</span></span>
<span data-ttu-id="7cf86-110">Командлет Remove-AzVpnGateway удаляет шлюз Azure VPN.</span><span class="sxs-lookup"><span data-stu-id="7cf86-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="7cf86-111">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf86-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="7cf86-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cf86-112">EXAMPLES</span></span>

### <span data-ttu-id="7cf86-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7cf86-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="7cf86-114">В этом примере создается группа ресурсов, Виртуальная глобальная сеть, виртуальный концентратор виртуальных частных сетей, масштабируемый шлюз VPN в центре US и сразу же удаляются.</span><span class="sxs-lookup"><span data-stu-id="7cf86-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="7cf86-115">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="7cf86-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="7cf86-116">Это приведет к удалению VpnGateway и всех VpnConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="7cf86-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="7cf86-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7cf86-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="7cf86-118">В этом примере создается группа ресурсов, Виртуальная глобальная сеть, виртуальный концентратор виртуальных частных сетей, масштабируемый шлюз VPN в центре US и сразу же удаляются.</span><span class="sxs-lookup"><span data-stu-id="7cf86-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="7cf86-119">Это удаление выполняется с помощью оболочки PowerShell, в которой используется объект VpnGateway, возвращенный командой "Get-AzVpnGateway".</span><span class="sxs-lookup"><span data-stu-id="7cf86-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="7cf86-120">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="7cf86-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="7cf86-121">Это приведет к удалению VpnGateway и всех VpnConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="7cf86-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="7cf86-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cf86-122">PARAMETERS</span></span>

### <span data-ttu-id="7cf86-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf86-123">-DefaultProfile</span></span>
<span data-ttu-id="7cf86-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf86-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf86-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7cf86-125">-Force</span></span>
<span data-ttu-id="7cf86-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7cf86-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7cf86-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cf86-127">-InputObject</span></span>
<span data-ttu-id="7cf86-128">Объект vpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7cf86-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf86-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7cf86-129">-Name</span></span>
<span data-ttu-id="7cf86-130">Имя vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7cf86-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf86-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cf86-131">-PassThru</span></span>
<span data-ttu-id="7cf86-132">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7cf86-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7cf86-133">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7cf86-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7cf86-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf86-134">-ResourceGroupName</span></span>
<span data-ttu-id="7cf86-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7cf86-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf86-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf86-136">-ResourceId</span></span>
<span data-ttu-id="7cf86-137">Идентификатор ресурса Azure для vpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7cf86-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf86-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cf86-138">-Confirm</span></span>
<span data-ttu-id="7cf86-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7cf86-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf86-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf86-140">-WhatIf</span></span>
<span data-ttu-id="7cf86-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7cf86-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf86-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7cf86-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf86-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf86-143">CommonParameters</span></span>
<span data-ttu-id="7cf86-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7cf86-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf86-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf86-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf86-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cf86-146">INPUTS</span></span>

### <span data-ttu-id="7cf86-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7cf86-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="7cf86-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf86-148">System.String</span></span>

## <span data-ttu-id="7cf86-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf86-149">OUTPUTS</span></span>

### <span data-ttu-id="7cf86-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7cf86-150">System.Boolean</span></span>

## <span data-ttu-id="7cf86-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cf86-151">NOTES</span></span>

## <span data-ttu-id="7cf86-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cf86-152">RELATED LINKS</span></span>

[<span data-ttu-id="7cf86-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7cf86-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="7cf86-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7cf86-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="7cf86-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7cf86-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
