---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249887"
---
# <span data-ttu-id="01c33-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="01c33-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="01c33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01c33-102">SYNOPSIS</span></span>
<span data-ttu-id="01c33-103">Создает объект VirtualHubRoute, который можно передать как параметр для команды Add-AzVirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="01c33-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="01c33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01c33-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01c33-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01c33-105">DESCRIPTION</span></span>
<span data-ttu-id="01c33-106">Создает объект VirtualHubRoute.</span><span class="sxs-lookup"><span data-stu-id="01c33-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="01c33-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01c33-107">EXAMPLES</span></span>

### <span data-ttu-id="01c33-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01c33-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="01c33-109">Вышеприведенная команда создаст объект VirtualHubRoute, который затем можно добавить в ресурс VirtualHubRouteTable и задать в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="01c33-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="01c33-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01c33-110">PARAMETERS</span></span>

### <span data-ttu-id="01c33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c33-111">-DefaultProfile</span></span>
<span data-ttu-id="01c33-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01c33-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c33-113">-Destination</span><span class="sxs-lookup"><span data-stu-id="01c33-113">-Destination</span></span>
<span data-ttu-id="01c33-114">Список назначений.</span><span class="sxs-lookup"><span data-stu-id="01c33-114">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c33-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="01c33-115">-DestinationType</span></span>
<span data-ttu-id="01c33-116">Тип назначений.</span><span class="sxs-lookup"><span data-stu-id="01c33-116">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c33-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="01c33-117">-NextHop</span></span>
<span data-ttu-id="01c33-118">Список последующих переходов.</span><span class="sxs-lookup"><span data-stu-id="01c33-118">List of Next hops.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c33-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="01c33-119">-NextHopType</span></span>
<span data-ttu-id="01c33-120">Тип следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="01c33-120">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c33-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c33-121">CommonParameters</span></span>
<span data-ttu-id="01c33-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01c33-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c33-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01c33-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c33-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01c33-124">INPUTS</span></span>

### <span data-ttu-id="01c33-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="01c33-125">None</span></span>

## <span data-ttu-id="01c33-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01c33-126">OUTPUTS</span></span>

### <span data-ttu-id="01c33-127">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="01c33-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="01c33-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="01c33-128">NOTES</span></span>

## <span data-ttu-id="01c33-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01c33-129">RELATED LINKS</span></span>