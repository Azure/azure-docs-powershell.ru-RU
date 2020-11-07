---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
ms.openlocfilehash: 00730f6e252373eebbbbc476fdd889b2eeb39e12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732912"
---
# <span data-ttu-id="d6f43-101">Update-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d6f43-101">Update-AzureRmVpnGateway</span></span>

## <span data-ttu-id="d6f43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6f43-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f43-103">Update-AzureRmVpnGateway обновляет масштабируемый шлюз VPN до соответствующего состояния цели.</span><span class="sxs-lookup"><span data-stu-id="d6f43-103">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6f43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6f43-104">SYNTAX</span></span>

### <span data-ttu-id="d6f43-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6f43-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f43-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d6f43-106">ByVpnGatewayObject</span></span>
```
Update-AzureRmVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f43-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f43-107">ByVpnGatewayResourceId</span></span>
```
Update-AzureRmVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f43-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6f43-108">DESCRIPTION</span></span>
<span data-ttu-id="d6f43-109">Update-AzureRmVpnGateway обновляет масштабируемый шлюз VPN до соответствующего состояния цели.</span><span class="sxs-lookup"><span data-stu-id="d6f43-109">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span> <span data-ttu-id="d6f43-110">AzureRmVpnGateway — это программное обеспечение, которое позволяет подключаться к подключениям к сайту в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d6f43-110">An AzureRmVpnGateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="d6f43-111">Этот шлюз изменяет размер и масштабируется в соответствии с единицей масштабирования, заданной пользователем.</span><span class="sxs-lookup"><span data-stu-id="d6f43-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="d6f43-112">Подключение можно настроить из ветви или сайта, известного как VPNSite, на масштабируемый шлюз.</span><span class="sxs-lookup"><span data-stu-id="d6f43-112">A connection can be set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="d6f43-113">Каждое соединение состоит из двух туннелей Active-Active</span><span class="sxs-lookup"><span data-stu-id="d6f43-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="d6f43-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6f43-114">EXAMPLES</span></span>

### <span data-ttu-id="d6f43-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6f43-115">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="d6f43-116">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f43-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d6f43-117">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d6f43-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d6f43-118">После создания шлюза он использует Set-AzureRmVpnGateway для обновления шлюза до 3 единиц масштаба.</span><span class="sxs-lookup"><span data-stu-id="d6f43-118">After the gateway has been created, it uses Set-AzureRmVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="d6f43-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6f43-119">PARAMETERS</span></span>

### <span data-ttu-id="d6f43-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6f43-120">-AsJob</span></span>
<span data-ttu-id="d6f43-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d6f43-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6f43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f43-122">-DefaultProfile</span></span>
<span data-ttu-id="d6f43-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f43-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f43-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6f43-124">-InputObject</span></span>
<span data-ttu-id="d6f43-125">Объект VPN-шлюза, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="d6f43-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="d6f43-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6f43-126">-Name</span></span>
<span data-ttu-id="d6f43-127">Имя виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="d6f43-127">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f43-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f43-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6f43-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6f43-129">The resource group name.</span></span>

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

### <span data-ttu-id="d6f43-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f43-130">-ResourceId</span></span>
<span data-ttu-id="d6f43-131">Идентификатор ресурса Azure VpnGateway, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="d6f43-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f43-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="d6f43-132">-Tag</span></span>
<span data-ttu-id="d6f43-133">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6f43-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d6f43-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d6f43-134">-VpnConnection</span></span>
<span data-ttu-id="d6f43-135">Список VpnConnections, который должен иметь этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d6f43-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="d6f43-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="d6f43-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="d6f43-137">Единица масштабирования для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d6f43-137">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f43-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6f43-138">-Confirm</span></span>
<span data-ttu-id="d6f43-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6f43-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f43-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f43-140">-WhatIf</span></span>
<span data-ttu-id="d6f43-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6f43-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f43-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6f43-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f43-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f43-143">CommonParameters</span></span>
<span data-ttu-id="d6f43-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6f43-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f43-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f43-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f43-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6f43-146">INPUTS</span></span>

### <span data-ttu-id="d6f43-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d6f43-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="d6f43-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d6f43-148">System.String</span></span>

## <span data-ttu-id="d6f43-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6f43-149">OUTPUTS</span></span>

### <span data-ttu-id="d6f43-150">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d6f43-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="d6f43-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6f43-151">NOTES</span></span>

## <span data-ttu-id="d6f43-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6f43-152">RELATED LINKS</span></span>
