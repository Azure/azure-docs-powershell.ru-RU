---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: baf349f56d3ebbf55c21d99dbfefd64ad7b295a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507825"
---
# <span data-ttu-id="b805d-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b805d-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="b805d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b805d-102">SYNOPSIS</span></span>
<span data-ttu-id="b805d-103">Создает объект виртуального концентратора Azure Route.</span><span class="sxs-lookup"><span data-stu-id="b805d-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="b805d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b805d-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b805d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b805d-105">DESCRIPTION</span></span>
<span data-ttu-id="b805d-106">Создает объект виртуального концентратора Azure Route.</span><span class="sxs-lookup"><span data-stu-id="b805d-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="b805d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b805d-107">EXAMPLES</span></span>

### <span data-ttu-id="b805d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b805d-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="b805d-109">Выше будет создаваться объект маршрутов виртуального концентратора, который можно включить в таблицу маршрутов виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="b805d-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="b805d-110">Виртуальный маршрут концентратора — это объект в памяти, который можно использовать для создания объекта VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="b805d-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="b805d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b805d-111">PARAMETERS</span></span>

### <span data-ttu-id="b805d-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b805d-112">-AddressPrefix</span></span>
<span data-ttu-id="b805d-113">Список префиксов адресов.</span><span class="sxs-lookup"><span data-stu-id="b805d-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="b805d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b805d-114">-DefaultProfile</span></span>
<span data-ttu-id="b805d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b805d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b805d-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="b805d-116">-NextHopIpAddress</span></span>
<span data-ttu-id="b805d-117">IpAddress следующего перехода.</span><span class="sxs-lookup"><span data-stu-id="b805d-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="b805d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b805d-118">CommonParameters</span></span>
<span data-ttu-id="b805d-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b805d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b805d-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b805d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b805d-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b805d-121">INPUTS</span></span>

### <span data-ttu-id="b805d-122">Нет</span><span class="sxs-lookup"><span data-stu-id="b805d-122">None</span></span>

## <span data-ttu-id="b805d-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b805d-123">OUTPUTS</span></span>

### <span data-ttu-id="b805d-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b805d-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="b805d-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b805d-125">NOTES</span></span>

## <span data-ttu-id="b805d-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b805d-126">RELATED LINKS</span></span>

[<span data-ttu-id="b805d-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b805d-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
