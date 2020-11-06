---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
ms.openlocfilehash: b29b57ea7d7a5182a25cb05ae05e6d1644a5c18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562863"
---
# <span data-ttu-id="35420-101">New-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="35420-101">New-AzureRmVpnGateway</span></span>

## <span data-ttu-id="35420-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35420-102">SYNOPSIS</span></span>
<span data-ttu-id="35420-103">Создает масштабируемый шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="35420-103">Creates a Scalable VPN Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35420-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35420-104">SYNTAX</span></span>

### <span data-ttu-id="35420-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35420-105">ByVirtualHubName (Default)</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35420-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="35420-106">ByVirtualHubObject</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35420-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="35420-107">ByVirtualHubResourceId</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35420-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35420-108">DESCRIPTION</span></span>

<span data-ttu-id="35420-109">New-AzureRmVpnGateway создает масштабируемый шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="35420-109">New-AzureRmVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="35420-110">Это программное обеспечение может определять связь между сайтами и подключениями к сайту в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="35420-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="35420-111">Этот шлюз изменяет размер и масштабируется с учетом единиц масштабирования, указанных в этом или Set-AzureRmVpnGatewayом командлете.</span><span class="sxs-lookup"><span data-stu-id="35420-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzureRmVpnGateway cmdlet.</span></span> 

<span data-ttu-id="35420-112">Соединение настраивается из ветви или сайта, известного как VPNSite, на масштабируемый шлюз.</span><span class="sxs-lookup"><span data-stu-id="35420-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="35420-113">Каждое соединение состоит из двух туннелей Active-Active.</span><span class="sxs-lookup"><span data-stu-id="35420-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="35420-114">VpnGateway будет находиться в той же папке, что и VirtualHub, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="35420-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="35420-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35420-115">EXAMPLES</span></span>

### <span data-ttu-id="35420-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35420-116">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

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

<span data-ttu-id="35420-117">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="35420-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="35420-118">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="35420-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="35420-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35420-119">PARAMETERS</span></span>

### <span data-ttu-id="35420-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35420-120">-AsJob</span></span>
<span data-ttu-id="35420-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="35420-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35420-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35420-122">-DefaultProfile</span></span>
<span data-ttu-id="35420-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35420-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35420-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35420-124">-Name</span></span>
<span data-ttu-id="35420-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="35420-125">The resource name.</span></span>

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

### <span data-ttu-id="35420-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35420-126">-ResourceGroupName</span></span>
<span data-ttu-id="35420-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="35420-127">The resource name.</span></span>

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

### <span data-ttu-id="35420-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="35420-128">-Tag</span></span>
<span data-ttu-id="35420-129">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35420-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="35420-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="35420-130">-VirtualHub</span></span>
<span data-ttu-id="35420-131">VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35420-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="35420-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="35420-132">-VirtualHubId</span></span>
<span data-ttu-id="35420-133">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35420-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="35420-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="35420-134">-VirtualHubName</span></span>
<span data-ttu-id="35420-135">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35420-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="35420-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="35420-136">-VpnConnection</span></span>
<span data-ttu-id="35420-137">Список VpnConnections, который должен иметь этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35420-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="35420-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="35420-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="35420-139">Единица масштабирования для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35420-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="35420-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35420-140">-Confirm</span></span>
<span data-ttu-id="35420-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35420-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35420-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35420-142">-WhatIf</span></span>
<span data-ttu-id="35420-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35420-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35420-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35420-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35420-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35420-145">CommonParameters</span></span>
<span data-ttu-id="35420-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35420-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35420-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35420-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35420-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35420-148">INPUTS</span></span>

### <span data-ttu-id="35420-149">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="35420-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="35420-150">System. String</span><span class="sxs-lookup"><span data-stu-id="35420-150">System.String</span></span>

## <span data-ttu-id="35420-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35420-151">OUTPUTS</span></span>

### <span data-ttu-id="35420-152">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="35420-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="35420-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="35420-153">NOTES</span></span>

## <span data-ttu-id="35420-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35420-154">RELATED LINKS</span></span>
