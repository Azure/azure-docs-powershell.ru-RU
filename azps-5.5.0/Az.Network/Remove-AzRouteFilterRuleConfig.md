---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227532"
---
# <span data-ttu-id="72cba-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72cba-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="72cba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72cba-102">SYNOPSIS</span></span>
<span data-ttu-id="72cba-103">Удаляет правило фильтра маршрутов из фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="72cba-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="72cba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="72cba-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72cba-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72cba-105">DESCRIPTION</span></span>
<span data-ttu-id="72cba-106">Чтобы удалить правило фильтра маршрутов из фильтра маршрутов, можно удалить правило фильтрации маршрутов из **azRouteFilterRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="72cba-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="72cba-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="72cba-107">EXAMPLES</span></span>

### <span data-ttu-id="72cba-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72cba-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="72cba-109">Первая команда получает фильтр маршрутов с именем RouteFilter01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет его в переменной $rf ресурса.</span><span class="sxs-lookup"><span data-stu-id="72cba-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="72cba-110">Вторая команда удаляет правило фильтра маршрутов "Правило01" из фильтра маршрутов, $rf.</span><span class="sxs-lookup"><span data-stu-id="72cba-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="72cba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72cba-111">PARAMETERS</span></span>

### <span data-ttu-id="72cba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cba-112">-DefaultProfile</span></span>
<span data-ttu-id="72cba-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72cba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72cba-114">-Force</span><span class="sxs-lookup"><span data-stu-id="72cba-114">-Force</span></span>
<span data-ttu-id="72cba-115">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="72cba-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="72cba-116">-Name</span><span class="sxs-lookup"><span data-stu-id="72cba-116">-Name</span></span>
<span data-ttu-id="72cba-117">Имя правила фильтрации маршрутов</span><span class="sxs-lookup"><span data-stu-id="72cba-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="72cba-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="72cba-118">-RouteFilter</span></span>
<span data-ttu-id="72cba-119">Маршрутизатор</span><span class="sxs-lookup"><span data-stu-id="72cba-119">The RouteFilter</span></span>

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

### <span data-ttu-id="72cba-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72cba-120">-Confirm</span></span>
<span data-ttu-id="72cba-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72cba-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cba-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72cba-122">-WhatIf</span></span>
<span data-ttu-id="72cba-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72cba-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72cba-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="72cba-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cba-125">CommonParameters</span></span>
<span data-ttu-id="72cba-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72cba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cba-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72cba-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cba-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72cba-128">INPUTS</span></span>

### <span data-ttu-id="72cba-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="72cba-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="72cba-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72cba-130">OUTPUTS</span></span>

### <span data-ttu-id="72cba-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="72cba-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="72cba-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="72cba-132">NOTES</span></span>

## <span data-ttu-id="72cba-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72cba-133">RELATED LINKS</span></span>

[<span data-ttu-id="72cba-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72cba-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="72cba-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72cba-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="72cba-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72cba-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="72cba-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72cba-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="72cba-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="72cba-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="72cba-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="72cba-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="72cba-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="72cba-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="72cba-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="72cba-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
