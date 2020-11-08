---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: b6537b9b8501aa2ec0aa76c9ede080893bf136ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236065"
---
# <span data-ttu-id="4e470-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4e470-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="4e470-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e470-102">SYNOPSIS</span></span>
<span data-ttu-id="4e470-103">Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName или перечисляет все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="4e470-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="4e470-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e470-104">SYNTAX</span></span>

### <span data-ttu-id="4e470-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e470-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e470-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e470-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e470-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e470-107">DESCRIPTION</span></span>
<span data-ttu-id="4e470-108">Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName или перечисляет все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="4e470-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="4e470-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e470-109">EXAMPLES</span></span>

### <span data-ttu-id="4e470-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e470-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="4e470-111">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="4e470-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4e470-112">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="4e470-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4e470-113">Затем он получает VpnGateway, используя его resourceGroupName и имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="4e470-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="4e470-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4e470-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="4e470-115">Этот командлет получает все шлюзы, которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="4e470-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="4e470-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e470-116">PARAMETERS</span></span>

### <span data-ttu-id="4e470-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e470-117">-DefaultProfile</span></span>
<span data-ttu-id="4e470-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e470-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e470-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e470-119">-Name</span></span>
<span data-ttu-id="4e470-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e470-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4e470-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e470-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e470-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e470-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4e470-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e470-123">CommonParameters</span></span>
<span data-ttu-id="4e470-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e470-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e470-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e470-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e470-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e470-126">INPUTS</span></span>

### <span data-ttu-id="4e470-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="4e470-127">None</span></span>

## <span data-ttu-id="4e470-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e470-128">OUTPUTS</span></span>

### <span data-ttu-id="4e470-129">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4e470-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="4e470-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e470-130">NOTES</span></span>

## <span data-ttu-id="4e470-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e470-131">RELATED LINKS</span></span>

[<span data-ttu-id="4e470-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4e470-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="4e470-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4e470-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="4e470-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4e470-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)