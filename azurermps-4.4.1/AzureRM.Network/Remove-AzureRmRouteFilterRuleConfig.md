---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: d73fbe14e4b1d4c4ea34c7405ad7da5b7954ffd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568322"
---
# <span data-ttu-id="6c579-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c579-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="6c579-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c579-102">SYNOPSIS</span></span>
<span data-ttu-id="6c579-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="6c579-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c579-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c579-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c579-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c579-105">DESCRIPTION</span></span>
<span data-ttu-id="6c579-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="6c579-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="6c579-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c579-107">EXAMPLES</span></span>

### <span data-ttu-id="6c579-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c579-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6c579-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="6c579-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="6c579-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c579-110">PARAMETERS</span></span>

### <span data-ttu-id="6c579-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6c579-111">-Force</span></span>
<span data-ttu-id="6c579-112">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="6c579-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="6c579-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c579-113">-Name</span></span>
<span data-ttu-id="6c579-114">Имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="6c579-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="6c579-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="6c579-115">-RouteFilter</span></span>
<span data-ttu-id="6c579-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="6c579-116">The RouteFilter</span></span>

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

### <span data-ttu-id="6c579-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c579-117">-Confirm</span></span>
<span data-ttu-id="6c579-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6c579-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c579-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c579-119">-WhatIf</span></span>
<span data-ttu-id="6c579-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6c579-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c579-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6c579-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c579-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c579-122">-DefaultProfile</span></span>
<span data-ttu-id="6c579-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c579-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c579-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c579-124">CommonParameters</span></span>
<span data-ttu-id="6c579-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c579-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c579-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c579-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c579-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c579-127">INPUTS</span></span>

### <span data-ttu-id="6c579-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6c579-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="6c579-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c579-129">OUTPUTS</span></span>

### <span data-ttu-id="6c579-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="6c579-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="6c579-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c579-131">NOTES</span></span>

## <span data-ttu-id="6c579-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c579-132">RELATED LINKS</span></span>

