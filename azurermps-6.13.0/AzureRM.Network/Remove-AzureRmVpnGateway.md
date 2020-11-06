---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
ms.openlocfilehash: 34e143b3ca6114fd90d52a5ad6ee8c022fda5688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568449"
---
# <span data-ttu-id="57329-101">Remove-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="57329-101">Remove-AzureRmVpnGateway</span></span>

## <span data-ttu-id="57329-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57329-102">SYNOPSIS</span></span>
<span data-ttu-id="57329-103">Командлет Remove-AzureRmVpnGateway удаляет шлюз Azure VPN.</span><span class="sxs-lookup"><span data-stu-id="57329-103">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="57329-104">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="57329-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57329-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57329-105">SYNTAX</span></span>

### <span data-ttu-id="57329-106">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57329-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57329-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="57329-107">ByVpnGatewayObject</span></span>
```
Remove-AzureRmVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57329-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="57329-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzureRmVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57329-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57329-109">DESCRIPTION</span></span>
<span data-ttu-id="57329-110">Командлет Remove-AzureRmVpnGateway удаляет шлюз Azure VPN.</span><span class="sxs-lookup"><span data-stu-id="57329-110">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="57329-111">Это шлюз, специфичный для подключения по виртуальной глобальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="57329-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="57329-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57329-112">EXAMPLES</span></span>

### <span data-ttu-id="57329-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57329-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="57329-114">В этом примере создается группа ресурсов, Виртуальная глобальная сеть, виртуальный концентратор виртуальных частных сетей, масштабируемый шлюз VPN в центре US и сразу же удаляются.</span><span class="sxs-lookup"><span data-stu-id="57329-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="57329-115">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="57329-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="57329-116">Это приведет к удалению VpnGateway и всех VpnConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="57329-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="57329-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="57329-117">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzureRmVpnGateway-Passthru
```

<span data-ttu-id="57329-118">В этом примере создается группа ресурсов, Виртуальная глобальная сеть, виртуальный концентратор виртуальных частных сетей, масштабируемый шлюз VPN в центре US и сразу же удаляются.</span><span class="sxs-lookup"><span data-stu-id="57329-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="57329-119">Это удаление выполняется с помощью оболочки PowerShell, в которой используется объект VpnGateway, возвращенный командой "Get-AzureRmVpnGateway".</span><span class="sxs-lookup"><span data-stu-id="57329-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzureRmVpnGateway command.</span></span>
<span data-ttu-id="57329-120">Чтобы отключить вывод запроса при удалении виртуального шлюза, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="57329-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="57329-121">Это приведет к удалению VpnGateway и всех VpnConnections, прикрепленных к нему.</span><span class="sxs-lookup"><span data-stu-id="57329-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="57329-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57329-122">PARAMETERS</span></span>

### <span data-ttu-id="57329-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57329-123">-DefaultProfile</span></span>
<span data-ttu-id="57329-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57329-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57329-125">-Force</span><span class="sxs-lookup"><span data-stu-id="57329-125">-Force</span></span>
<span data-ttu-id="57329-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="57329-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="57329-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57329-127">-InputObject</span></span>
<span data-ttu-id="57329-128">Объект vpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="57329-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="57329-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="57329-129">-Name</span></span>
<span data-ttu-id="57329-130">Имя vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="57329-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="57329-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57329-131">-PassThru</span></span>
<span data-ttu-id="57329-132">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="57329-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="57329-133">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="57329-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="57329-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57329-134">-ResourceGroupName</span></span>
<span data-ttu-id="57329-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57329-135">The resource group name.</span></span>

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

### <span data-ttu-id="57329-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57329-136">-ResourceId</span></span>
<span data-ttu-id="57329-137">Идентификатор ресурса Azure для vpnGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="57329-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="57329-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57329-138">-Confirm</span></span>
<span data-ttu-id="57329-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57329-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57329-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57329-140">-WhatIf</span></span>
<span data-ttu-id="57329-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57329-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57329-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57329-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57329-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57329-143">CommonParameters</span></span>
<span data-ttu-id="57329-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57329-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57329-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57329-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57329-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57329-146">INPUTS</span></span>

### <span data-ttu-id="57329-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="57329-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="57329-148">System. String</span><span class="sxs-lookup"><span data-stu-id="57329-148">System.String</span></span>

## <span data-ttu-id="57329-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57329-149">OUTPUTS</span></span>

### <span data-ttu-id="57329-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57329-150">System.Boolean</span></span>

## <span data-ttu-id="57329-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="57329-151">NOTES</span></span>

## <span data-ttu-id="57329-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57329-152">RELATED LINKS</span></span>
