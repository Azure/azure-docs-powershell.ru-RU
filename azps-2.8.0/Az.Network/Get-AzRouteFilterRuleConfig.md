---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 5d83678d26804c97a0e21da4dcbff3f5af75d409
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902853"
---
# <span data-ttu-id="5238a-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5238a-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="5238a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5238a-102">SYNOPSIS</span></span>
<span data-ttu-id="5238a-103">Возвращает правило фильтра маршрутов в фильтре маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5238a-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="5238a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5238a-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5238a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5238a-105">DESCRIPTION</span></span>
<span data-ttu-id="5238a-106">Командлет **Get-AzRouteFilterRuleConfig** получает правило фильтра маршрутов или список правил фильтрации маршрутов в фильтре маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5238a-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="5238a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5238a-107">EXAMPLES</span></span>

### <span data-ttu-id="5238a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5238a-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="5238a-109">Первая команда получает фильтр маршрутов с именем MyRouteFilter и сохраняет его в переменной $rf.</span><span class="sxs-lookup"><span data-stu-id="5238a-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="5238a-110">Вторая команда получает правило фильтра маршрутов с именем Rule01, связанное с фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5238a-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="5238a-111">Третья команда получает список правил фильтрации маршрутов, связанных с этим фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5238a-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="5238a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5238a-112">PARAMETERS</span></span>

### <span data-ttu-id="5238a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5238a-113">-DefaultProfile</span></span>
<span data-ttu-id="5238a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5238a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5238a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5238a-115">-Name</span></span>
<span data-ttu-id="5238a-116">Имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5238a-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="5238a-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="5238a-117">-RouteFilter</span></span>
<span data-ttu-id="5238a-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="5238a-118">The RouteFilter</span></span>

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

### <span data-ttu-id="5238a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5238a-119">CommonParameters</span></span>
<span data-ttu-id="5238a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5238a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5238a-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5238a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5238a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5238a-122">INPUTS</span></span>

### <span data-ttu-id="5238a-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5238a-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="5238a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5238a-124">OUTPUTS</span></span>

### <span data-ttu-id="5238a-125">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="5238a-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="5238a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5238a-126">NOTES</span></span>

## <span data-ttu-id="5238a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5238a-127">RELATED LINKS</span></span>

[<span data-ttu-id="5238a-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5238a-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5238a-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5238a-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5238a-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5238a-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5238a-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5238a-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5238a-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5238a-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="5238a-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5238a-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="5238a-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5238a-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="5238a-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5238a-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
