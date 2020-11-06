---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: b6a4899fb54ffc4305f6b512046e00bda994b02e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565589"
---
# <span data-ttu-id="999ea-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="999ea-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="999ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="999ea-102">SYNOPSIS</span></span>
<span data-ttu-id="999ea-103">Список маршрутов, полученных шлюзом виртуальной сети Azure</span><span class="sxs-lookup"><span data-stu-id="999ea-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="999ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="999ea-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="999ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="999ea-105">DESCRIPTION</span></span>
<span data-ttu-id="999ea-106">Перечисление маршрутов, полученных шлюзом виртуальных сетей Azure, из различных источников.</span><span class="sxs-lookup"><span data-stu-id="999ea-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="999ea-107">Сюда входят маршруты, полученные по протоколу BGP, а также статические маршруты.</span><span class="sxs-lookup"><span data-stu-id="999ea-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="999ea-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="999ea-108">EXAMPLES</span></span>

### <span data-ttu-id="999ea-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="999ea-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="999ea-110">Для шлюза виртуальной сети Azure с именем gatewayname в группе ресурсов "resourceGroup" можно получить маршруты, которые шлюз Azure знает.</span><span class="sxs-lookup"><span data-stu-id="999ea-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="999ea-111">Шлюз виртуальных сетей Azure в этом случае имеет два статических маршрута (10.1.0.0/16 и 10.0.0.254/32), а также один маршрут, полученный по протоколу BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="999ea-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="999ea-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="999ea-112">PARAMETERS</span></span>

### <span data-ttu-id="999ea-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="999ea-113">-ResourceGroupName</span></span>
<span data-ttu-id="999ea-114">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="999ea-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999ea-115">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="999ea-115">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="999ea-116">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="999ea-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="999ea-117">-DefaultProfile</span></span>
<span data-ttu-id="999ea-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="999ea-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="999ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999ea-119">CommonParameters</span></span>
<span data-ttu-id="999ea-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="999ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999ea-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="999ea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999ea-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="999ea-122">INPUTS</span></span>

### <span data-ttu-id="999ea-123">System. String</span><span class="sxs-lookup"><span data-stu-id="999ea-123">System.String</span></span>

## <span data-ttu-id="999ea-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="999ea-124">OUTPUTS</span></span>

### <span data-ttu-id="999ea-125">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="999ea-125">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="999ea-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="999ea-126">NOTES</span></span>

## <span data-ttu-id="999ea-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="999ea-127">RELATED LINKS</span></span>

