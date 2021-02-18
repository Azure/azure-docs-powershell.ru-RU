---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228012"
---
# <span data-ttu-id="fe1fd-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe1fd-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="fe1fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1fd-103">Создает ресурс виртуальной таблицы маршрутов hub, который является частью VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fe1fd-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="fe1fd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe1fd-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe1fd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1fd-105">DESCRIPTION</span></span>
<span data-ttu-id="fe1fd-106">Ресурс виртуальной таблицы маршрутов концентратора содержит список маршрутов и список подключений, к которым он может быть подключен и используется для маршрутивки трафика в виртуальном центре.</span><span class="sxs-lookup"><span data-stu-id="fe1fd-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="fe1fd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe1fd-107">EXAMPLES</span></span>

### <span data-ttu-id="fe1fd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe1fd-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="fe1fd-109">С этой командой создается ресурс виртуальной таблицы маршрутов концентратора из маршрутов, переданных ему, и этот объект можно использовать для маршрутинга трафика в виртуальном центре.</span><span class="sxs-lookup"><span data-stu-id="fe1fd-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="fe1fd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe1fd-110">PARAMETERS</span></span>

### <span data-ttu-id="fe1fd-111">-Подключение</span><span class="sxs-lookup"><span data-stu-id="fe1fd-111">-Connection</span></span>
<span data-ttu-id="fe1fd-112">Список подключений, к которые подключена эта таблица маршрутов.</span><span class="sxs-lookup"><span data-stu-id="fe1fd-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="fe1fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1fd-113">-DefaultProfile</span></span>
<span data-ttu-id="fe1fd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe1fd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fe1fd-115">-Name</span></span>
<span data-ttu-id="fe1fd-116">Имя таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="fe1fd-116">Name of the route table.</span></span>

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

### <span data-ttu-id="fe1fd-117">-Route</span><span class="sxs-lookup"><span data-stu-id="fe1fd-117">-Route</span></span>
<span data-ttu-id="fe1fd-118">Список маршрутов виртуальных концентраторов.</span><span class="sxs-lookup"><span data-stu-id="fe1fd-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="fe1fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1fd-119">CommonParameters</span></span>
<span data-ttu-id="fe1fd-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe1fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1fd-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe1fd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1fd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe1fd-122">INPUTS</span></span>

### <span data-ttu-id="fe1fd-123">Нет</span><span class="sxs-lookup"><span data-stu-id="fe1fd-123">None</span></span>

## <span data-ttu-id="fe1fd-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe1fd-124">OUTPUTS</span></span>

### <span data-ttu-id="fe1fd-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe1fd-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="fe1fd-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe1fd-126">NOTES</span></span>

## <span data-ttu-id="fe1fd-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe1fd-127">RELATED LINKS</span></span>
