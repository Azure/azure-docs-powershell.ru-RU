---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: f5b2a3f66a1972edbf6d3e475f5f30fc9530929f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562379"
---
# <span data-ttu-id="7065a-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7065a-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="7065a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7065a-102">SYNOPSIS</span></span>
<span data-ttu-id="7065a-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="7065a-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7065a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7065a-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7065a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7065a-105">DESCRIPTION</span></span>
<span data-ttu-id="7065a-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="7065a-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7065a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7065a-107">EXAMPLES</span></span>

### <span data-ttu-id="7065a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7065a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7065a-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="7065a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7065a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7065a-110">PARAMETERS</span></span>

### <span data-ttu-id="7065a-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="7065a-111">-Access</span></span>
<span data-ttu-id="7065a-112">Тип доступа для правила.</span><span class="sxs-lookup"><span data-stu-id="7065a-112">The access type of the rule.</span></span>
<span data-ttu-id="7065a-113">Возможные значения: "разрешить", "запретить"</span><span class="sxs-lookup"><span data-stu-id="7065a-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="7065a-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="7065a-114">-CommunityList</span></span>
<span data-ttu-id="7065a-115">Список значений сообщества, по которому будет фильтроваться фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="7065a-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="7065a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7065a-116">-Force</span></span>
<span data-ttu-id="7065a-117">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="7065a-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="7065a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7065a-118">-Name</span></span>
<span data-ttu-id="7065a-119">Имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7065a-119">The name of the route filter rule</span></span>

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

### <span data-ttu-id="7065a-120">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7065a-120">-RouteFilter</span></span>
<span data-ttu-id="7065a-121">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7065a-121">The RouteFilter</span></span>

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

### <span data-ttu-id="7065a-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="7065a-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="7065a-123">Тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7065a-123">The route filter rule type of the rule.</span></span>
<span data-ttu-id="7065a-124">Возможные значения: "сообщество"</span><span class="sxs-lookup"><span data-stu-id="7065a-124">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="7065a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7065a-125">-Confirm</span></span>
<span data-ttu-id="7065a-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7065a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7065a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7065a-127">-WhatIf</span></span>
<span data-ttu-id="7065a-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7065a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7065a-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7065a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7065a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7065a-130">-DefaultProfile</span></span>
<span data-ttu-id="7065a-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7065a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7065a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7065a-132">CommonParameters</span></span>
<span data-ttu-id="7065a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7065a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7065a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7065a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7065a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7065a-135">INPUTS</span></span>

### <span data-ttu-id="7065a-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7065a-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7065a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7065a-137">OUTPUTS</span></span>

### <span data-ttu-id="7065a-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7065a-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7065a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="7065a-139">NOTES</span></span>

## <span data-ttu-id="7065a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7065a-140">RELATED LINKS</span></span>

