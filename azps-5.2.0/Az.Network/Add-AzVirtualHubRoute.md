---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397391"
---
# <span data-ttu-id="8c9a5-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8c9a5-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="8c9a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="8c9a5-103">Создает объект VirtualHubRoute, который можно передать в качестве параметра команде Add-AzVirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="8c9a5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c9a5-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c9a5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c9a5-105">DESCRIPTION</span></span>
<span data-ttu-id="8c9a5-106">Создание объекта VirtualHubRoute.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="8c9a5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c9a5-107">EXAMPLES</span></span>

### <span data-ttu-id="8c9a5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8c9a5-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="8c9a5-109">С этой командой создается объект VirtualHubRoute, который затем можно добавить на ресурс VirtualHubRouteTable и установить в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="8c9a5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c9a5-110">PARAMETERS</span></span>

### <span data-ttu-id="8c9a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c9a5-111">-DefaultProfile</span></span>
<span data-ttu-id="8c9a5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c9a5-113">-Destination</span><span class="sxs-lookup"><span data-stu-id="8c9a5-113">-Destination</span></span>
<span data-ttu-id="8c9a5-114">Список назначений.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-114">List of Destinations.</span></span>

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

### <span data-ttu-id="8c9a5-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="8c9a5-115">-DestinationType</span></span>
<span data-ttu-id="8c9a5-116">Тип назначения.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="8c9a5-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="8c9a5-117">-NextHop</span></span>
<span data-ttu-id="8c9a5-118">Список следующих переходов.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-118">List of Next hops.</span></span>

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

### <span data-ttu-id="8c9a5-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="8c9a5-119">-NextHopType</span></span>
<span data-ttu-id="8c9a5-120">Тип следующего перехода.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="8c9a5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c9a5-121">CommonParameters</span></span>
<span data-ttu-id="8c9a5-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c9a5-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c9a5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c9a5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c9a5-124">INPUTS</span></span>

### <span data-ttu-id="8c9a5-125">Нет</span><span class="sxs-lookup"><span data-stu-id="8c9a5-125">None</span></span>

## <span data-ttu-id="8c9a5-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c9a5-126">OUTPUTS</span></span>

### <span data-ttu-id="8c9a5-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8c9a5-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="8c9a5-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c9a5-128">NOTES</span></span>

## <span data-ttu-id="8c9a5-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c9a5-129">RELATED LINKS</span></span>
