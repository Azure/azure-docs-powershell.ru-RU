---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235010"
---
# <span data-ttu-id="ed1aa-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed1aa-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ed1aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1aa-103">Возвращает правило фильтра маршрутов в фильтре маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="ed1aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed1aa-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed1aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-105">DESCRIPTION</span></span>
<span data-ttu-id="ed1aa-106">Командлет **Get-AzRouteFilterRuleConfig** получает правило фильтра маршрутов или список правил фильтрации маршрутов в фильтре маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="ed1aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-107">EXAMPLES</span></span>

### <span data-ttu-id="ed1aa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed1aa-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="ed1aa-109">Первая команда получает фильтр маршрутов с именем MyRouteFilter и сохраняет его в переменной $rf.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="ed1aa-110">Вторая команда получает правило фильтра маршрутов с именем Rule01, связанное с фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="ed1aa-111">Третья команда получает список правил фильтрации маршрутов, связанных с этим фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="ed1aa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-112">PARAMETERS</span></span>

### <span data-ttu-id="ed1aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1aa-113">-DefaultProfile</span></span>
<span data-ttu-id="ed1aa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed1aa-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed1aa-115">-Name</span></span>
<span data-ttu-id="ed1aa-116">Имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-116">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed1aa-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed1aa-117">-RouteFilter</span></span>
<span data-ttu-id="ed1aa-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed1aa-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed1aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1aa-119">CommonParameters</span></span>
<span data-ttu-id="ed1aa-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed1aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1aa-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed1aa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1aa-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed1aa-122">INPUTS</span></span>

### <span data-ttu-id="ed1aa-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed1aa-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ed1aa-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-124">OUTPUTS</span></span>

### <span data-ttu-id="ed1aa-125">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="ed1aa-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ed1aa-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed1aa-126">NOTES</span></span>

## <span data-ttu-id="ed1aa-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed1aa-127">RELATED LINKS</span></span>

[<span data-ttu-id="ed1aa-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed1aa-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ed1aa-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed1aa-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ed1aa-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed1aa-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ed1aa-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed1aa-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ed1aa-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed1aa-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="ed1aa-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed1aa-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="ed1aa-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed1aa-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="ed1aa-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed1aa-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)