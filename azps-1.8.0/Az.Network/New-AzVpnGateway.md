---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 08915aaf72fbab91d8173480f4e608ebdbaa28ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730240"
---
# <span data-ttu-id="6133d-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6133d-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="6133d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6133d-102">SYNOPSIS</span></span>
<span data-ttu-id="6133d-103">Создает масштабируемый шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="6133d-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="6133d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6133d-104">SYNTAX</span></span>

### <span data-ttu-id="6133d-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6133d-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6133d-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6133d-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6133d-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6133d-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6133d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6133d-108">DESCRIPTION</span></span>

<span data-ttu-id="6133d-109">New-AzVpnGateway создает масштабируемый шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="6133d-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="6133d-110">Это программное обеспечение может определять связь между сайтами и подключениями к сайту в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="6133d-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="6133d-111">Этот шлюз изменяет размер и масштабируется с учетом единиц масштабирования, указанных в этом или Set-AzVpnGatewayом командлете.</span><span class="sxs-lookup"><span data-stu-id="6133d-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="6133d-112">Соединение настраивается из ветви или сайта, известного как VPNSite, на масштабируемый шлюз.</span><span class="sxs-lookup"><span data-stu-id="6133d-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="6133d-113">Каждое соединение состоит из двух туннелей Active-Active.</span><span class="sxs-lookup"><span data-stu-id="6133d-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="6133d-114">VpnGateway будет находиться в той же папке, что и VirtualHub, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="6133d-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="6133d-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6133d-115">EXAMPLES</span></span>

### <span data-ttu-id="6133d-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6133d-116">Example 1</span></span>

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

<span data-ttu-id="6133d-117">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="6133d-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6133d-118">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="6133d-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="6133d-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6133d-119">PARAMETERS</span></span>

### <span data-ttu-id="6133d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6133d-120">-AsJob</span></span>
<span data-ttu-id="6133d-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6133d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6133d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6133d-122">-DefaultProfile</span></span>
<span data-ttu-id="6133d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6133d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6133d-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6133d-124">-Name</span></span>
<span data-ttu-id="6133d-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="6133d-125">The resource name.</span></span>

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

### <span data-ttu-id="6133d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6133d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6133d-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="6133d-127">The resource name.</span></span>

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

### <span data-ttu-id="6133d-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="6133d-128">-Tag</span></span>
<span data-ttu-id="6133d-129">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6133d-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6133d-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6133d-130">-VirtualHub</span></span>
<span data-ttu-id="6133d-131">VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6133d-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="6133d-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="6133d-132">-VirtualHubId</span></span>
<span data-ttu-id="6133d-133">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6133d-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="6133d-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="6133d-134">-VirtualHubName</span></span>
<span data-ttu-id="6133d-135">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6133d-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="6133d-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6133d-136">-VpnConnection</span></span>
<span data-ttu-id="6133d-137">Список VpnConnections, который должен иметь этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6133d-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="6133d-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="6133d-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="6133d-139">Единица масштабирования для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6133d-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="6133d-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6133d-140">-Confirm</span></span>
<span data-ttu-id="6133d-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6133d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6133d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6133d-142">-WhatIf</span></span>
<span data-ttu-id="6133d-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6133d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6133d-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6133d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6133d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6133d-145">CommonParameters</span></span>
<span data-ttu-id="6133d-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6133d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6133d-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6133d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6133d-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6133d-148">INPUTS</span></span>

### <span data-ttu-id="6133d-149">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6133d-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6133d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6133d-150">System.String</span></span>

## <span data-ttu-id="6133d-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6133d-151">OUTPUTS</span></span>

### <span data-ttu-id="6133d-152">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6133d-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="6133d-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="6133d-153">NOTES</span></span>

## <span data-ttu-id="6133d-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6133d-154">RELATED LINKS</span></span>

[<span data-ttu-id="6133d-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6133d-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="6133d-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6133d-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="6133d-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6133d-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
