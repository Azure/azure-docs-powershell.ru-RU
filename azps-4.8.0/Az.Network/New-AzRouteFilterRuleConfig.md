---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236026"
---
# <span data-ttu-id="1cb09-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb09-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1cb09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1cb09-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb09-103">Создание правила фильтра маршрутов для фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="1cb09-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="1cb09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1cb09-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cb09-105">DESCRIPTION</span></span>
<span data-ttu-id="1cb09-106">Командлет New-AzRouteFilterRuleConfig создает правило фильтра маршрутов для фильтра маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb09-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="1cb09-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1cb09-107">EXAMPLES</span></span>

### <span data-ttu-id="1cb09-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1cb09-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="1cb09-109">Команда создаст новое правило фильтра маршрутов и сохранит его в переменной $rule 1.</span><span class="sxs-lookup"><span data-stu-id="1cb09-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="1cb09-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1cb09-110">PARAMETERS</span></span>

### <span data-ttu-id="1cb09-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="1cb09-111">-Access</span></span>
<span data-ttu-id="1cb09-112">Доступ к правилу фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="1cb09-112">Access for route filter rule.</span></span>
<span data-ttu-id="1cb09-113">Допустимые значения: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="1cb09-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="1cb09-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="1cb09-114">-CommunityList</span></span>
<span data-ttu-id="1cb09-115">Список значений сообщества, по которому будет фильтроваться фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="1cb09-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1cb09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb09-116">-DefaultProfile</span></span>
<span data-ttu-id="1cb09-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb09-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb09-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1cb09-118">-Force</span></span>
<span data-ttu-id="1cb09-119">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="1cb09-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1cb09-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1cb09-120">-Name</span></span>
<span data-ttu-id="1cb09-121">Задает имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="1cb09-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="1cb09-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1cb09-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="1cb09-123">Тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="1cb09-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="1cb09-124">Допустимые значения: Community</span><span class="sxs-lookup"><span data-stu-id="1cb09-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="1cb09-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb09-125">-Confirm</span></span>
<span data-ttu-id="1cb09-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1cb09-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb09-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb09-127">-WhatIf</span></span>
<span data-ttu-id="1cb09-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1cb09-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cb09-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1cb09-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb09-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb09-130">CommonParameters</span></span>
<span data-ttu-id="1cb09-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1cb09-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb09-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cb09-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb09-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1cb09-133">INPUTS</span></span>

### <span data-ttu-id="1cb09-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="1cb09-134">None</span></span>

## <span data-ttu-id="1cb09-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cb09-135">OUTPUTS</span></span>

### <span data-ttu-id="1cb09-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="1cb09-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="1cb09-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1cb09-137">NOTES</span></span>
<span data-ttu-id="1cb09-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="1cb09-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1cb09-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cb09-139">RELATED LINKS</span></span>

[<span data-ttu-id="1cb09-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb09-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1cb09-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb09-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1cb09-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb09-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1cb09-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb09-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1cb09-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1cb09-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="1cb09-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1cb09-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="1cb09-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1cb09-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="1cb09-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1cb09-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
