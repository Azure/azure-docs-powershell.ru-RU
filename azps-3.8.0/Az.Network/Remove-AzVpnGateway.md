---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 1e13cad885d18d8c15a033ae85b340041107cdc0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073943"
---
# <span data-ttu-id="afca6-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="afca6-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="afca6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="afca6-102">SYNOPSIS</span></span>
<span data-ttu-id="afca6-103">Командлет Remove-AzVpnGateway удаляет шлюз Azure VPN.</span><span class="sxs-lookup"><span data-stu-id="afca6-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="afca6-104">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="afca6-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="afca6-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="afca6-105">SYNTAX</span></span>

### <span data-ttu-id="afca6-106">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="afca6-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afca6-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="afca6-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afca6-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="afca6-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afca6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afca6-109">DESCRIPTION</span></span>
<span data-ttu-id="afca6-110">Командлет Remove-AzVpnGateway удаляет шлюз Azure VPN.</span><span class="sxs-lookup"><span data-stu-id="afca6-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="afca6-111">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="afca6-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="afca6-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="afca6-112">EXAMPLES</span></span>

### <span data-ttu-id="afca6-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="afca6-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="afca6-114">В этом примере создается группа ресурсов, Виртуальная глобальная сеть, виртуальный концентратор виртуальных частных сетей, масштабируемый шлюз VPN в центре US и сразу же удаляются.</span><span class="sxs-lookup"><span data-stu-id="afca6-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="afca6-115">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="afca6-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="afca6-116">Это приведет к удалению VpnGateway и всех VpnConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="afca6-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="afca6-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="afca6-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="afca6-118">В этом примере создается группа ресурсов, Виртуальная глобальная сеть, виртуальный концентратор виртуальных частных сетей, масштабируемый шлюз VPN в центре US и сразу же удаляются.</span><span class="sxs-lookup"><span data-stu-id="afca6-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="afca6-119">Это удаление выполняется с помощью оболочки PowerShell, в которой используется объект VpnGateway, возвращенный командой "Get-AzVpnGateway".</span><span class="sxs-lookup"><span data-stu-id="afca6-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="afca6-120">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="afca6-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="afca6-121">Это приведет к удалению VpnGateway и всех VpnConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="afca6-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="afca6-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="afca6-122">PARAMETERS</span></span>

### <span data-ttu-id="afca6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afca6-123">-DefaultProfile</span></span>
<span data-ttu-id="afca6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afca6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afca6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="afca6-125">-Force</span></span>
<span data-ttu-id="afca6-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="afca6-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="afca6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afca6-127">-InputObject</span></span>
<span data-ttu-id="afca6-128">Объект vpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="afca6-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="afca6-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="afca6-129">-Name</span></span>
<span data-ttu-id="afca6-130">Имя vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="afca6-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="afca6-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afca6-131">-PassThru</span></span>
<span data-ttu-id="afca6-132">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="afca6-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="afca6-133">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="afca6-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="afca6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afca6-134">-ResourceGroupName</span></span>
<span data-ttu-id="afca6-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="afca6-135">The resource group name.</span></span>

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

### <span data-ttu-id="afca6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afca6-136">-ResourceId</span></span>
<span data-ttu-id="afca6-137">Идентификатор ресурса Azure для vpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="afca6-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="afca6-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afca6-138">-Confirm</span></span>
<span data-ttu-id="afca6-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="afca6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afca6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afca6-140">-WhatIf</span></span>
<span data-ttu-id="afca6-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="afca6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afca6-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="afca6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afca6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afca6-143">CommonParameters</span></span>
<span data-ttu-id="afca6-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="afca6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afca6-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afca6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afca6-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="afca6-146">INPUTS</span></span>

### <span data-ttu-id="afca6-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="afca6-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="afca6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="afca6-148">System.String</span></span>

## <span data-ttu-id="afca6-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="afca6-149">OUTPUTS</span></span>

### <span data-ttu-id="afca6-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="afca6-150">System.Boolean</span></span>

## <span data-ttu-id="afca6-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="afca6-151">NOTES</span></span>

## <span data-ttu-id="afca6-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afca6-152">RELATED LINKS</span></span>

[<span data-ttu-id="afca6-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="afca6-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="afca6-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="afca6-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="afca6-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="afca6-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
