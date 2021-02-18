---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223708"
---
# <span data-ttu-id="9a891-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a891-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="9a891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a891-102">SYNOPSIS</span></span>
<span data-ttu-id="9a891-103">Создает правило фильтрации маршрутов для фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9a891-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="9a891-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a891-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a891-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a891-105">DESCRIPTION</span></span>
<span data-ttu-id="9a891-106">С New-AzRouteFilterRuleConfig создается правило фильтрации маршрутов для фильтра маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="9a891-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="9a891-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a891-107">EXAMPLES</span></span>

### <span data-ttu-id="9a891-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a891-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="9a891-109">Команда создает новое правило фильтра маршрутов и сохраняет его в переменной $rule 1.</span><span class="sxs-lookup"><span data-stu-id="9a891-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="9a891-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a891-110">PARAMETERS</span></span>

### <span data-ttu-id="9a891-111">-Access</span><span class="sxs-lookup"><span data-stu-id="9a891-111">-Access</span></span>
<span data-ttu-id="9a891-112">Access для правила фильтрации маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9a891-112">Access for route filter rule.</span></span>
<span data-ttu-id="9a891-113">Допустимые значения: "Разрешить" или "Запретить".</span><span class="sxs-lookup"><span data-stu-id="9a891-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a891-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="9a891-114">-CommunityList</span></span>
<span data-ttu-id="9a891-115">Список значений сообщества, по которые фильтр маршрутов будет фильтроваться по</span><span class="sxs-lookup"><span data-stu-id="9a891-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="9a891-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a891-116">-DefaultProfile</span></span>
<span data-ttu-id="9a891-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a891-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a891-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9a891-118">-Force</span></span>
<span data-ttu-id="9a891-119">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="9a891-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9a891-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9a891-120">-Name</span></span>
<span data-ttu-id="9a891-121">Указывает имя правила фильтрации маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9a891-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="9a891-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="9a891-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="9a891-123">Тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9a891-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="9a891-124">Допустимые значения: Community</span><span class="sxs-lookup"><span data-stu-id="9a891-124">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a891-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a891-125">-Confirm</span></span>
<span data-ttu-id="9a891-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9a891-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a891-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a891-127">-WhatIf</span></span>
<span data-ttu-id="9a891-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a891-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a891-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a891-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a891-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a891-130">CommonParameters</span></span>
<span data-ttu-id="9a891-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a891-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a891-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a891-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a891-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a891-133">INPUTS</span></span>

### <span data-ttu-id="9a891-134">Нет</span><span class="sxs-lookup"><span data-stu-id="9a891-134">None</span></span>

## <span data-ttu-id="9a891-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a891-135">OUTPUTS</span></span>

### <span data-ttu-id="9a891-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="9a891-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="9a891-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a891-137">NOTES</span></span>
<span data-ttu-id="9a891-138">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="9a891-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9a891-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a891-139">RELATED LINKS</span></span>

[<span data-ttu-id="9a891-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a891-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9a891-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a891-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9a891-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a891-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9a891-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a891-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9a891-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9a891-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="9a891-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9a891-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="9a891-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9a891-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="9a891-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9a891-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
