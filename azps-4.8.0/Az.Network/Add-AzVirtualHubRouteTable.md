---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243046"
---
# <span data-ttu-id="5e152-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e152-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="5e152-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e152-102">SYNOPSIS</span></span>
<span data-ttu-id="5e152-103">Создает виртуальный ресурс-разветвитель маршрута, который является дочерним элементом VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="5e152-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="5e152-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e152-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e152-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e152-105">DESCRIPTION</span></span>
<span data-ttu-id="5e152-106">Ресурс «Таблица маршрутов виртуального концентратора» содержит список маршрутов и список подключений, к которым он может быть присоединен, и используется для маршрутизации трафика на виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="5e152-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="5e152-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e152-107">EXAMPLES</span></span>

### <span data-ttu-id="5e152-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e152-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="5e152-109">Вышеприведенная команда создаст ресурс таблицы виртуального маршрутизатора из переданных маршрутов, и этот объект можно использовать для маршрутизации трафика на виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="5e152-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="5e152-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e152-110">PARAMETERS</span></span>

### <span data-ttu-id="5e152-111">-Подключение</span><span class="sxs-lookup"><span data-stu-id="5e152-111">-Connection</span></span>
<span data-ttu-id="5e152-112">Список подключений, к которым присоединена таблица маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5e152-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="5e152-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e152-113">-DefaultProfile</span></span>
<span data-ttu-id="5e152-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e152-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e152-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e152-115">-Name</span></span>
<span data-ttu-id="5e152-116">Имя таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5e152-116">Name of the route table.</span></span>

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

### <span data-ttu-id="5e152-117">-Route</span><span class="sxs-lookup"><span data-stu-id="5e152-117">-Route</span></span>
<span data-ttu-id="5e152-118">Список маршрутов виртуальных концентраторов.</span><span class="sxs-lookup"><span data-stu-id="5e152-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e152-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e152-119">CommonParameters</span></span>
<span data-ttu-id="5e152-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e152-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e152-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e152-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e152-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e152-122">INPUTS</span></span>

### <span data-ttu-id="5e152-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="5e152-123">None</span></span>

## <span data-ttu-id="5e152-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e152-124">OUTPUTS</span></span>

### <span data-ttu-id="5e152-125">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e152-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="5e152-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e152-126">NOTES</span></span>

## <span data-ttu-id="5e152-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e152-127">RELATED LINKS</span></span>
