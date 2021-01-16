---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507873"
---
# <span data-ttu-id="d411b-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d411b-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="d411b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d411b-102">SYNOPSIS</span></span>
<span data-ttu-id="d411b-103">Создает политику выбора трафика.</span><span class="sxs-lookup"><span data-stu-id="d411b-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="d411b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d411b-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d411b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d411b-105">DESCRIPTION</span></span>
<span data-ttu-id="d411b-106">С New-AzTrafficSelectorPolicy создается предложение политики выбора трафика, которое будет использоваться в подсети виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="d411b-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="d411b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d411b-107">EXAMPLES</span></span>

### <span data-ttu-id="d411b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d411b-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="d411b-109">Создает экземпляр политики выбора трафика и добавляет ее в качестве параметра при создании подключения виртуального сетевого шлюза с протоколом IKEv2.</span><span class="sxs-lookup"><span data-stu-id="d411b-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="d411b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d411b-110">PARAMETERS</span></span>

### <span data-ttu-id="d411b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d411b-111">-DefaultProfile</span></span>
<span data-ttu-id="d411b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d411b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d411b-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="d411b-113">-LocalAddressRange</span></span>
<span data-ttu-id="d411b-114">Коллекция диапазонов адресов CIDR</span><span class="sxs-lookup"><span data-stu-id="d411b-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d411b-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="d411b-115">-RemoteAddressRange</span></span>
<span data-ttu-id="d411b-116">Коллекция диапазонов адресов CIDR</span><span class="sxs-lookup"><span data-stu-id="d411b-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d411b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d411b-117">CommonParameters</span></span>
<span data-ttu-id="d411b-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d411b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d411b-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d411b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d411b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d411b-120">INPUTS</span></span>

### <span data-ttu-id="d411b-121">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d411b-121">System.String[]</span></span>

## <span data-ttu-id="d411b-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d411b-122">OUTPUTS</span></span>

### <span data-ttu-id="d411b-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d411b-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="d411b-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d411b-124">NOTES</span></span>

## <span data-ttu-id="d411b-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d411b-125">RELATED LINKS</span></span>
