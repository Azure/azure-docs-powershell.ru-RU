---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3c3e20762bcf8e48fc3f01d750419493a81ca8aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732435"
---
# <span data-ttu-id="8823e-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8823e-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8823e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8823e-102">SYNOPSIS</span></span>
<span data-ttu-id="8823e-103">Создание правила фильтра маршрутов для фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8823e-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8823e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8823e-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8823e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8823e-105">DESCRIPTION</span></span>
<span data-ttu-id="8823e-106">Командлет New-AzureRmRouteFilterRuleConfig создает правило фильтра маршрутов для фильтра маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="8823e-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="8823e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8823e-107">EXAMPLES</span></span>

### <span data-ttu-id="8823e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8823e-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8823e-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="8823e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8823e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8823e-110">PARAMETERS</span></span>

### <span data-ttu-id="8823e-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="8823e-111">-Access</span></span>
<span data-ttu-id="8823e-112">Доступ к правилу фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8823e-112">Access for route filter rule.</span></span>
<span data-ttu-id="8823e-113">Допустимые значения: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="8823e-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="8823e-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="8823e-114">-CommunityList</span></span>
<span data-ttu-id="8823e-115">Список значений сообщества, по которому будет фильтроваться фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="8823e-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="8823e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8823e-116">-Force</span></span>
<span data-ttu-id="8823e-117">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="8823e-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="8823e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8823e-118">-Name</span></span>
<span data-ttu-id="8823e-119">Задает имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8823e-119">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="8823e-120">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="8823e-120">-RouteFilterRuleType</span></span>
<span data-ttu-id="8823e-121">Тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8823e-121">Route Filter Rule Type.</span></span>
<span data-ttu-id="8823e-122">Допустимые значения: Community</span><span class="sxs-lookup"><span data-stu-id="8823e-122">Valid values are: Community</span></span>

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

### <span data-ttu-id="8823e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8823e-123">-Confirm</span></span>
<span data-ttu-id="8823e-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8823e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8823e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8823e-125">-WhatIf</span></span>
<span data-ttu-id="8823e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8823e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8823e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8823e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8823e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8823e-128">-DefaultProfile</span></span>
<span data-ttu-id="8823e-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8823e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8823e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8823e-130">CommonParameters</span></span>
<span data-ttu-id="8823e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8823e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8823e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8823e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8823e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8823e-133">INPUTS</span></span>

## <span data-ttu-id="8823e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8823e-134">OUTPUTS</span></span>

### <span data-ttu-id="8823e-135">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="8823e-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="8823e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8823e-136">NOTES</span></span>
<span data-ttu-id="8823e-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="8823e-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8823e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8823e-138">RELATED LINKS</span></span>

[<span data-ttu-id="8823e-139">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8823e-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8823e-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8823e-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8823e-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8823e-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8823e-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8823e-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

