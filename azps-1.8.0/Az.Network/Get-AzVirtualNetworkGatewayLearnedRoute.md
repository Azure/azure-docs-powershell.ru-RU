---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 80bb8e05b110f1b3e9689895ae9bea2aad1207b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730470"
---
# <span data-ttu-id="a4cc5-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="a4cc5-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="a4cc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cc5-103">Список маршрутов, полученных шлюзом виртуальной сети Azure</span><span class="sxs-lookup"><span data-stu-id="a4cc5-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="a4cc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4cc5-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4cc5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4cc5-105">DESCRIPTION</span></span>
<span data-ttu-id="a4cc5-106">Перечисление маршрутов, полученных шлюзом виртуальных сетей Azure, из различных источников.</span><span class="sxs-lookup"><span data-stu-id="a4cc5-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="a4cc5-107">Сюда входят маршруты, полученные по протоколу BGP, а также статические маршруты.</span><span class="sxs-lookup"><span data-stu-id="a4cc5-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="a4cc5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4cc5-108">EXAMPLES</span></span>

### <span data-ttu-id="a4cc5-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4cc5-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

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

<span data-ttu-id="a4cc5-110">Для шлюза виртуальной сети Azure с именем gatewayname в группе ресурсов "resourceGroup" можно получить маршруты, которые шлюз Azure знает.</span><span class="sxs-lookup"><span data-stu-id="a4cc5-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="a4cc5-111">Шлюз виртуальных сетей Azure в этом случае имеет два статических маршрута (10.1.0.0/16 и 10.0.0.254/32), а также один маршрут, полученный по протоколу BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="a4cc5-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="a4cc5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4cc5-112">PARAMETERS</span></span>

### <span data-ttu-id="a4cc5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4cc5-113">-AsJob</span></span>
<span data-ttu-id="a4cc5-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a4cc5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4cc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4cc5-115">-DefaultProfile</span></span>
<span data-ttu-id="a4cc5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4cc5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4cc5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4cc5-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4cc5-118">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a4cc5-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="a4cc5-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a4cc5-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a4cc5-120">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a4cc5-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="a4cc5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cc5-121">CommonParameters</span></span>
<span data-ttu-id="a4cc5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4cc5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cc5-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4cc5-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cc5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4cc5-124">INPUTS</span></span>

### <span data-ttu-id="a4cc5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a4cc5-125">System.String</span></span>

## <span data-ttu-id="a4cc5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4cc5-126">OUTPUTS</span></span>

### <span data-ttu-id="a4cc5-127">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="a4cc5-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="a4cc5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4cc5-128">NOTES</span></span>

## <span data-ttu-id="a4cc5-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4cc5-129">RELATED LINKS</span></span>
