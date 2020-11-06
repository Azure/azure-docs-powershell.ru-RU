---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 6e0ff70671ceff4094d7f1a48bbebcc81398d5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559004"
---
# <span data-ttu-id="e2fac-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2fac-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="e2fac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2fac-102">SYNOPSIS</span></span>
<span data-ttu-id="e2fac-103">Создание правила фильтра маршрутов для фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="e2fac-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2fac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2fac-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2fac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2fac-105">DESCRIPTION</span></span>
<span data-ttu-id="e2fac-106">Командлет New-AzureRmRouteFilterRuleConfig создает правило фильтра маршрутов для фильтра маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="e2fac-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="e2fac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2fac-107">EXAMPLES</span></span>

### <span data-ttu-id="e2fac-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2fac-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e2fac-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="e2fac-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e2fac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2fac-110">PARAMETERS</span></span>

### <span data-ttu-id="e2fac-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="e2fac-111">-Access</span></span>
<span data-ttu-id="e2fac-112">Доступ к правилу фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="e2fac-112">Access for route filter rule.</span></span>
<span data-ttu-id="e2fac-113">Допустимые значения: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="e2fac-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fac-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="e2fac-114">-CommunityList</span></span>
<span data-ttu-id="e2fac-115">Список значений сообщества, по которому будет фильтроваться фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="e2fac-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2fac-116">-DefaultProfile</span></span>
<span data-ttu-id="e2fac-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2fac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fac-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e2fac-118">-Force</span></span>
<span data-ttu-id="e2fac-119">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="e2fac-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fac-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2fac-120">-Name</span></span>
<span data-ttu-id="e2fac-121">Задает имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="e2fac-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="e2fac-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="e2fac-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="e2fac-123">Тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="e2fac-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="e2fac-124">Допустимые значения: Community</span><span class="sxs-lookup"><span data-stu-id="e2fac-124">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fac-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2fac-125">-Confirm</span></span>
<span data-ttu-id="e2fac-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2fac-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fac-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2fac-127">-WhatIf</span></span>
<span data-ttu-id="e2fac-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2fac-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2fac-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2fac-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2fac-130">CommonParameters</span></span>
<span data-ttu-id="e2fac-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2fac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2fac-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2fac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2fac-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2fac-133">INPUTS</span></span>

### <span data-ttu-id="e2fac-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="e2fac-134">None</span></span>
<span data-ttu-id="e2fac-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e2fac-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2fac-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2fac-136">OUTPUTS</span></span>

### <span data-ttu-id="e2fac-137">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="e2fac-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="e2fac-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2fac-138">NOTES</span></span>
<span data-ttu-id="e2fac-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="e2fac-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e2fac-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2fac-140">RELATED LINKS</span></span>

[<span data-ttu-id="e2fac-141">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2fac-141">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="e2fac-142">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2fac-142">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="e2fac-143">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2fac-143">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="e2fac-144">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2fac-144">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

