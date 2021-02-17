---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218745"
---
# <span data-ttu-id="5ed7e-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5ed7e-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="5ed7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ed7e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed7e-103">Получает правило фильтрации маршрутов в фильтре маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5ed7e-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="5ed7e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ed7e-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ed7e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ed7e-105">DESCRIPTION</span></span>
<span data-ttu-id="5ed7e-106">Для получения правила фильтрации маршрутов или списка правил фильтрации маршрутов в фильтре маршрутов возвращается cmdlet **Get-AzRouteFilterRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="5ed7e-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="5ed7e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ed7e-107">EXAMPLES</span></span>

### <span data-ttu-id="5ed7e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ed7e-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="5ed7e-109">Первая команда получает фильтр маршрутов MyRouteFilter, а затем сохраняет его в переменной $rf.</span><span class="sxs-lookup"><span data-stu-id="5ed7e-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="5ed7e-110">Вторая команда получает правило фильтра маршрутов с именем "Правило01", связанное с этим фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="5ed7e-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="5ed7e-111">Третья команда получает список правил фильтрации маршрутов, связанных с этим фильтром.</span><span class="sxs-lookup"><span data-stu-id="5ed7e-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="5ed7e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ed7e-112">PARAMETERS</span></span>

### <span data-ttu-id="5ed7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed7e-113">-DefaultProfile</span></span>
<span data-ttu-id="5ed7e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed7e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ed7e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5ed7e-115">-Name</span></span>
<span data-ttu-id="5ed7e-116">Имя правила фильтрации маршрутов</span><span class="sxs-lookup"><span data-stu-id="5ed7e-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="5ed7e-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="5ed7e-117">-RouteFilter</span></span>
<span data-ttu-id="5ed7e-118">Маршрутизатор</span><span class="sxs-lookup"><span data-stu-id="5ed7e-118">The RouteFilter</span></span>

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

### <span data-ttu-id="5ed7e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed7e-119">CommonParameters</span></span>
<span data-ttu-id="5ed7e-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed7e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed7e-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ed7e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed7e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ed7e-122">INPUTS</span></span>

### <span data-ttu-id="5ed7e-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5ed7e-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="5ed7e-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ed7e-124">OUTPUTS</span></span>

### <span data-ttu-id="5ed7e-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="5ed7e-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="5ed7e-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ed7e-126">NOTES</span></span>

## <span data-ttu-id="5ed7e-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ed7e-127">RELATED LINKS</span></span>

[<span data-ttu-id="5ed7e-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5ed7e-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5ed7e-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5ed7e-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5ed7e-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5ed7e-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5ed7e-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5ed7e-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5ed7e-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5ed7e-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="5ed7e-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5ed7e-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="5ed7e-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5ed7e-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="5ed7e-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5ed7e-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
