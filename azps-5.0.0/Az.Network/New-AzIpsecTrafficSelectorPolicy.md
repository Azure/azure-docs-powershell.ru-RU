---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247270"
---
# <span data-ttu-id="f10e6-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f10e6-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="f10e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f10e6-102">SYNOPSIS</span></span>
<span data-ttu-id="f10e6-103">Создание политики выбора трафика.</span><span class="sxs-lookup"><span data-stu-id="f10e6-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="f10e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f10e6-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f10e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f10e6-105">DESCRIPTION</span></span>
<span data-ttu-id="f10e6-106">Командлет New-AzTrafficSelectorPolicy создает предложение политики выбора трафика, которое будет использоваться в соединении с шлюзом виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="f10e6-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="f10e6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f10e6-107">EXAMPLES</span></span>

### <span data-ttu-id="f10e6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f10e6-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="f10e6-109">Создает экземпляр политики выбора трафика и добавляет ее как параметр при создании подключения к виртуальному сетевому шлюзу с помощью протокола IKEv2.</span><span class="sxs-lookup"><span data-stu-id="f10e6-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="f10e6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f10e6-110">PARAMETERS</span></span>

### <span data-ttu-id="f10e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10e6-111">-DefaultProfile</span></span>
<span data-ttu-id="f10e6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f10e6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f10e6-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="f10e6-113">-LocalAddressRange</span></span>
<span data-ttu-id="f10e6-114">Коллекция диапазонов адресов CIDR</span><span class="sxs-lookup"><span data-stu-id="f10e6-114">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="f10e6-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="f10e6-115">-RemoteAddressRange</span></span>
<span data-ttu-id="f10e6-116">Коллекция диапазонов адресов CIDR</span><span class="sxs-lookup"><span data-stu-id="f10e6-116">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="f10e6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10e6-117">CommonParameters</span></span>
<span data-ttu-id="f10e6-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f10e6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10e6-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f10e6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10e6-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f10e6-120">INPUTS</span></span>

### <span data-ttu-id="f10e6-121">System. String []</span><span class="sxs-lookup"><span data-stu-id="f10e6-121">System.String[]</span></span>

## <span data-ttu-id="f10e6-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f10e6-122">OUTPUTS</span></span>

### <span data-ttu-id="f10e6-123">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f10e6-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="f10e6-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="f10e6-124">NOTES</span></span>

## <span data-ttu-id="f10e6-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f10e6-125">RELATED LINKS</span></span>
