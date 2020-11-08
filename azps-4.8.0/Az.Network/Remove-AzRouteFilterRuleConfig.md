---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236004"
---
# <span data-ttu-id="88a65-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88a65-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="88a65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88a65-102">SYNOPSIS</span></span>
<span data-ttu-id="88a65-103">Удаляет правило фильтра маршрутов из фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="88a65-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="88a65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88a65-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88a65-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88a65-105">DESCRIPTION</span></span>
<span data-ttu-id="88a65-106">Командлет **Remove-AzRouteFilterRuleConfig** удаляет правило фильтра маршрутов из фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="88a65-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="88a65-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88a65-107">EXAMPLES</span></span>

### <span data-ttu-id="88a65-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88a65-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="88a65-109">Первая команда получает фильтр маршрутов с именем RouteFilter01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $rf.</span><span class="sxs-lookup"><span data-stu-id="88a65-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="88a65-110">Вторая команда удаляет правило фильтра маршрутов с именем Rule01 из фильтра маршрутов, хранящегося в $rf.</span><span class="sxs-lookup"><span data-stu-id="88a65-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="88a65-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88a65-111">PARAMETERS</span></span>

### <span data-ttu-id="88a65-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a65-112">-DefaultProfile</span></span>
<span data-ttu-id="88a65-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88a65-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88a65-114">-Force</span><span class="sxs-lookup"><span data-stu-id="88a65-114">-Force</span></span>
<span data-ttu-id="88a65-115">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="88a65-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="88a65-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88a65-116">-Name</span></span>
<span data-ttu-id="88a65-117">Имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="88a65-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="88a65-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="88a65-118">-RouteFilter</span></span>
<span data-ttu-id="88a65-119">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="88a65-119">The RouteFilter</span></span>

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

### <span data-ttu-id="88a65-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88a65-120">-Confirm</span></span>
<span data-ttu-id="88a65-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88a65-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88a65-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88a65-122">-WhatIf</span></span>
<span data-ttu-id="88a65-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88a65-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88a65-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88a65-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88a65-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a65-125">CommonParameters</span></span>
<span data-ttu-id="88a65-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88a65-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a65-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a65-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a65-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88a65-128">INPUTS</span></span>

### <span data-ttu-id="88a65-129">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="88a65-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="88a65-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88a65-130">OUTPUTS</span></span>

### <span data-ttu-id="88a65-131">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="88a65-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="88a65-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="88a65-132">NOTES</span></span>

## <span data-ttu-id="88a65-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88a65-133">RELATED LINKS</span></span>

[<span data-ttu-id="88a65-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88a65-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="88a65-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88a65-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="88a65-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88a65-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="88a65-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88a65-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="88a65-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="88a65-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="88a65-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="88a65-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="88a65-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="88a65-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="88a65-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="88a65-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
