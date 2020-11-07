---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaylearnedroute
schema: 2.0.0
ms.openlocfilehash: 39bf91e5d346b475fe0c4b79b9128648555c6379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913827"
---
# <span data-ttu-id="6687c-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="6687c-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="6687c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6687c-102">SYNOPSIS</span></span>
<span data-ttu-id="6687c-103">Список маршрутов, полученных шлюзом виртуальной сети Azure</span><span class="sxs-lookup"><span data-stu-id="6687c-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6687c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6687c-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6687c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6687c-105">DESCRIPTION</span></span>
<span data-ttu-id="6687c-106">Перечисление маршрутов, полученных шлюзом виртуальных сетей Azure, из различных источников.</span><span class="sxs-lookup"><span data-stu-id="6687c-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="6687c-107">Сюда входят маршруты, полученные по протоколу BGP, а также статические маршруты.</span><span class="sxs-lookup"><span data-stu-id="6687c-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="6687c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6687c-108">EXAMPLES</span></span>

### <span data-ttu-id="6687c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6687c-109">Example 1</span></span>
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

<span data-ttu-id="6687c-110">Для шлюза виртуальной сети Azure с именем gatewayname в группе ресурсов "resourceGroup" можно получить маршруты, которые шлюз Azure знает.</span><span class="sxs-lookup"><span data-stu-id="6687c-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="6687c-111">Шлюз виртуальных сетей Azure в этом случае имеет два статических маршрута (10.1.0.0/16 и 10.0.0.254/32), а также один маршрут, полученный по протоколу BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="6687c-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="6687c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6687c-112">PARAMETERS</span></span>

### <span data-ttu-id="6687c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6687c-113">-AsJob</span></span>
<span data-ttu-id="6687c-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6687c-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6687c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6687c-115">-DefaultProfile</span></span>
<span data-ttu-id="6687c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6687c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6687c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6687c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6687c-118">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="6687c-118">Virtual network gateway resource group's name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6687c-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="6687c-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="6687c-120">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="6687c-120">Virtual network gateway name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6687c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6687c-121">CommonParameters</span></span>
<span data-ttu-id="6687c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6687c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6687c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6687c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6687c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6687c-124">INPUTS</span></span>

### <span data-ttu-id="6687c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6687c-125">System.String</span></span>

## <span data-ttu-id="6687c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6687c-126">OUTPUTS</span></span>

### <span data-ttu-id="6687c-127">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="6687c-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="6687c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6687c-128">NOTES</span></span>

## <span data-ttu-id="6687c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6687c-129">RELATED LINKS</span></span>

