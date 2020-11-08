---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: baf349f56d3ebbf55c21d99dbfefd64ad7b295a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248531"
---
# <span data-ttu-id="72cc9-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="72cc9-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="72cc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="72cc9-103">Создает объект-маршрут виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="72cc9-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="72cc9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72cc9-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72cc9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72cc9-105">DESCRIPTION</span></span>
<span data-ttu-id="72cc9-106">Создает объект-маршрут виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="72cc9-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="72cc9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72cc9-107">EXAMPLES</span></span>

### <span data-ttu-id="72cc9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72cc9-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="72cc9-109">В приведенном выше примере создается объект-маршрут виртуального концентратора, который может быть включен в таблицу виртуальных маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="72cc9-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="72cc9-110">Виртуальный серверный маршрут — это объект в памяти, который можно использовать для создания объекта VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="72cc9-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="72cc9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72cc9-111">PARAMETERS</span></span>

### <span data-ttu-id="72cc9-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="72cc9-112">-AddressPrefix</span></span>
<span data-ttu-id="72cc9-113">Список префиксов адресов.</span><span class="sxs-lookup"><span data-stu-id="72cc9-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cc9-114">-DefaultProfile</span></span>
<span data-ttu-id="72cc9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72cc9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72cc9-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="72cc9-116">-NextHopIpAddress</span></span>
<span data-ttu-id="72cc9-117">IP-адрес следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="72cc9-117">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cc9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cc9-118">CommonParameters</span></span>
<span data-ttu-id="72cc9-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72cc9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cc9-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72cc9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cc9-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72cc9-121">INPUTS</span></span>

### <span data-ttu-id="72cc9-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="72cc9-122">None</span></span>

## <span data-ttu-id="72cc9-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72cc9-123">OUTPUTS</span></span>

### <span data-ttu-id="72cc9-124">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="72cc9-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="72cc9-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="72cc9-125">NOTES</span></span>

## <span data-ttu-id="72cc9-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72cc9-126">RELATED LINKS</span></span>

[<span data-ttu-id="72cc9-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="72cc9-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
