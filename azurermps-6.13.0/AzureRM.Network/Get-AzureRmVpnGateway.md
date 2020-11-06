---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562908"
---
# <span data-ttu-id="e8635-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e8635-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="e8635-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8635-102">SYNOPSIS</span></span>
<span data-ttu-id="e8635-103">Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName или перечисляет все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="e8635-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8635-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8635-104">SYNTAX</span></span>

### <span data-ttu-id="e8635-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8635-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8635-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8635-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8635-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8635-107">DESCRIPTION</span></span>
<span data-ttu-id="e8635-108">Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName или перечисляет все шлюзы с помощью ResourceGroupName или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="e8635-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="e8635-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8635-109">EXAMPLES</span></span>

### <span data-ttu-id="e8635-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8635-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

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

<span data-ttu-id="e8635-111">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="e8635-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e8635-112">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="e8635-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e8635-113">Затем он получает VpnGateway, используя его resourceGroupName и имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="e8635-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="e8635-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8635-114">PARAMETERS</span></span>

### <span data-ttu-id="e8635-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8635-115">-DefaultProfile</span></span>
<span data-ttu-id="e8635-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8635-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8635-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8635-117">-Name</span></span>
<span data-ttu-id="e8635-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8635-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8635-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8635-119">-ResourceGroupName</span></span>
<span data-ttu-id="e8635-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8635-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8635-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8635-121">CommonParameters</span></span>
<span data-ttu-id="e8635-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8635-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8635-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8635-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8635-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8635-124">INPUTS</span></span>

### <span data-ttu-id="e8635-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e8635-125">System.String</span></span>

## <span data-ttu-id="e8635-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8635-126">OUTPUTS</span></span>

### <span data-ttu-id="e8635-127">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e8635-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="e8635-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8635-128">NOTES</span></span>

## <span data-ttu-id="e8635-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8635-129">RELATED LINKS</span></span>
