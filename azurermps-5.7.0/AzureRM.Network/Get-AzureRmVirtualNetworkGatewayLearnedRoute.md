---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: f8847e0b94a6501184e74234abda2c0b1836a152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564776"
---
# <span data-ttu-id="b9f4b-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="b9f4b-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="b9f4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f4b-103">Список маршрутов, полученных шлюзом виртуальной сети Azure</span><span class="sxs-lookup"><span data-stu-id="b9f4b-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9f4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9f4b-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9f4b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="b9f4b-106">Перечисление маршрутов, полученных шлюзом виртуальных сетей Azure, из различных источников.</span><span class="sxs-lookup"><span data-stu-id="b9f4b-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="b9f4b-107">Сюда входят маршруты, полученные по протоколу BGP, а также статические маршруты.</span><span class="sxs-lookup"><span data-stu-id="b9f4b-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="b9f4b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9f4b-108">EXAMPLES</span></span>

### <span data-ttu-id="b9f4b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9f4b-109">Example 1</span></span>
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

<span data-ttu-id="b9f4b-110">Для шлюза виртуальной сети Azure с именем gatewayname в группе ресурсов "resourceGroup" можно получить маршруты, которые шлюз Azure знает.</span><span class="sxs-lookup"><span data-stu-id="b9f4b-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="b9f4b-111">Шлюз виртуальных сетей Azure в этом случае имеет два статических маршрута (10.1.0.0/16 и 10.0.0.254/32), а также один маршрут, полученный по протоколу BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="b9f4b-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="b9f4b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9f4b-112">PARAMETERS</span></span>

### <span data-ttu-id="b9f4b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9f4b-113">-AsJob</span></span>
<span data-ttu-id="b9f4b-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b9f4b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9f4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f4b-115">-DefaultProfile</span></span>
<span data-ttu-id="b9f4b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9f4b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9f4b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9f4b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9f4b-118">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b9f4b-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="b9f4b-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b9f4b-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b9f4b-120">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b9f4b-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="b9f4b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f4b-121">CommonParameters</span></span>
<span data-ttu-id="b9f4b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9f4b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f4b-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9f4b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f4b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9f4b-124">INPUTS</span></span>

### <span data-ttu-id="b9f4b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b9f4b-125">System.String</span></span>

## <span data-ttu-id="b9f4b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9f4b-126">OUTPUTS</span></span>

### <span data-ttu-id="b9f4b-127">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="b9f4b-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="b9f4b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9f4b-128">NOTES</span></span>

## <span data-ttu-id="b9f4b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9f4b-129">RELATED LINKS</span></span>

