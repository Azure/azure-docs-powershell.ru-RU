---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: fa7374264e46e65dcddacb9f35e5822f18294147
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319214"
---
# <span data-ttu-id="c06e1-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c06e1-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="c06e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c06e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c06e1-103">Создает масштабируемый шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="c06e1-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="c06e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c06e1-104">SYNTAX</span></span>

### <span data-ttu-id="c06e1-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c06e1-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c06e1-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="c06e1-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c06e1-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c06e1-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c06e1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c06e1-108">DESCRIPTION</span></span>

<span data-ttu-id="c06e1-109">New-AzVpnGateway создает масштабируемый шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="c06e1-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="c06e1-110">Это программное обеспечение может определять связь между сайтами и подключениями к сайту в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c06e1-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="c06e1-111">Этот шлюз изменяет размер и масштабируется с учетом единиц масштабирования, указанных в этом или Set-AzVpnGatewayом командлете.</span><span class="sxs-lookup"><span data-stu-id="c06e1-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="c06e1-112">Соединение настраивается из ветви или сайта, известного как VPNSite, на масштабируемый шлюз.</span><span class="sxs-lookup"><span data-stu-id="c06e1-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="c06e1-113">Каждое соединение состоит из двух туннелей Active-Active.</span><span class="sxs-lookup"><span data-stu-id="c06e1-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="c06e1-114">VpnGateway будет находиться в той же папке, что и VirtualHub, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="c06e1-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="c06e1-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c06e1-115">EXAMPLES</span></span>

### <span data-ttu-id="c06e1-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c06e1-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="c06e1-117">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="c06e1-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c06e1-118">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c06e1-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="c06e1-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c06e1-119">PARAMETERS</span></span>

### <span data-ttu-id="c06e1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c06e1-120">-AsJob</span></span>
<span data-ttu-id="c06e1-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c06e1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c06e1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06e1-122">-DefaultProfile</span></span>
<span data-ttu-id="c06e1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c06e1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c06e1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c06e1-124">-Name</span></span>
<span data-ttu-id="c06e1-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c06e1-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c06e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="c06e1-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c06e1-127">The resource name.</span></span>

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

### <span data-ttu-id="c06e1-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="c06e1-128">-Tag</span></span>
<span data-ttu-id="c06e1-129">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c06e1-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c06e1-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="c06e1-130">-VirtualHub</span></span>
<span data-ttu-id="c06e1-131">VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c06e1-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="c06e1-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="c06e1-132">-VirtualHubId</span></span>
<span data-ttu-id="c06e1-133">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c06e1-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="c06e1-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="c06e1-134">-VirtualHubName</span></span>
<span data-ttu-id="c06e1-135">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c06e1-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="c06e1-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c06e1-136">-VpnConnection</span></span>
<span data-ttu-id="c06e1-137">Список VpnConnections, который должен иметь этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c06e1-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c06e1-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c06e1-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="c06e1-139">Единица масштабирования для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c06e1-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="c06e1-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c06e1-140">-Confirm</span></span>
<span data-ttu-id="c06e1-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c06e1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c06e1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c06e1-142">-WhatIf</span></span>
<span data-ttu-id="c06e1-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c06e1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c06e1-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c06e1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c06e1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06e1-145">CommonParameters</span></span>
<span data-ttu-id="c06e1-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c06e1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06e1-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c06e1-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06e1-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c06e1-148">INPUTS</span></span>

### <span data-ttu-id="c06e1-149">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c06e1-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="c06e1-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c06e1-150">System.String</span></span>

## <span data-ttu-id="c06e1-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c06e1-151">OUTPUTS</span></span>

### <span data-ttu-id="c06e1-152">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c06e1-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="c06e1-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="c06e1-153">NOTES</span></span>

## <span data-ttu-id="c06e1-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c06e1-154">RELATED LINKS</span></span>

[<span data-ttu-id="c06e1-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c06e1-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="c06e1-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c06e1-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="c06e1-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c06e1-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
