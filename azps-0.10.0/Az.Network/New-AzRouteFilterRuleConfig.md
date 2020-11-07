---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 6f8943fb4e75c96a97ad2b7f128d671a8be7c906
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909626"
---
# <span data-ttu-id="0682b-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0682b-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="0682b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0682b-102">SYNOPSIS</span></span>
<span data-ttu-id="0682b-103">Создание правила фильтра маршрутов для фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0682b-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="0682b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0682b-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0682b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0682b-105">DESCRIPTION</span></span>
<span data-ttu-id="0682b-106">Командлет New-AzRouteFilterRuleConfig создает правило фильтра маршрутов для фильтра маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="0682b-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="0682b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0682b-107">EXAMPLES</span></span>

### <span data-ttu-id="0682b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0682b-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0682b-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="0682b-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="0682b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0682b-110">PARAMETERS</span></span>

### <span data-ttu-id="0682b-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="0682b-111">-Access</span></span>
<span data-ttu-id="0682b-112">Доступ к правилу фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0682b-112">Access for route filter rule.</span></span>
<span data-ttu-id="0682b-113">Допустимые значения: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="0682b-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="0682b-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="0682b-114">-CommunityList</span></span>
<span data-ttu-id="0682b-115">Список значений сообщества, по которому будет фильтроваться фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="0682b-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="0682b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0682b-116">-DefaultProfile</span></span>
<span data-ttu-id="0682b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0682b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0682b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0682b-118">-Force</span></span>
<span data-ttu-id="0682b-119">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="0682b-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="0682b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0682b-120">-Name</span></span>
<span data-ttu-id="0682b-121">Задает имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0682b-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="0682b-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="0682b-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="0682b-123">Тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0682b-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="0682b-124">Допустимые значения: Community</span><span class="sxs-lookup"><span data-stu-id="0682b-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="0682b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0682b-125">-Confirm</span></span>
<span data-ttu-id="0682b-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0682b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0682b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0682b-127">-WhatIf</span></span>
<span data-ttu-id="0682b-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0682b-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0682b-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0682b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0682b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0682b-130">CommonParameters</span></span>
<span data-ttu-id="0682b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0682b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0682b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0682b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0682b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0682b-133">INPUTS</span></span>

## <span data-ttu-id="0682b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0682b-134">OUTPUTS</span></span>

### <span data-ttu-id="0682b-135">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="0682b-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="0682b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0682b-136">NOTES</span></span>
<span data-ttu-id="0682b-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="0682b-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0682b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0682b-138">RELATED LINKS</span></span>

[<span data-ttu-id="0682b-139">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0682b-139">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0682b-140">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0682b-140">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0682b-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0682b-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0682b-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0682b-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

