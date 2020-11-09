---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318557"
---
# <span data-ttu-id="d57a8-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d57a8-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="d57a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d57a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d57a8-103">Обновляет фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="d57a8-103">Updates a route filter.</span></span>

## <span data-ttu-id="d57a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d57a8-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d57a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d57a8-105">DESCRIPTION</span></span>
<span data-ttu-id="d57a8-106">Командлет **Set-AzApplicationGateway** обновляет фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="d57a8-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="d57a8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d57a8-107">EXAMPLES</span></span>

### <span data-ttu-id="d57a8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d57a8-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="d57a8-109">Эта команда обновляет фильтр маршрутов с параметрами, заданными в переменной $rf.</span><span class="sxs-lookup"><span data-stu-id="d57a8-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="d57a8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d57a8-110">PARAMETERS</span></span>

### <span data-ttu-id="d57a8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d57a8-111">-AsJob</span></span>
<span data-ttu-id="d57a8-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d57a8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d57a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57a8-113">-DefaultProfile</span></span>
<span data-ttu-id="d57a8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d57a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d57a8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d57a8-115">-Force</span></span>
<span data-ttu-id="d57a8-116">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="d57a8-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d57a8-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d57a8-117">-RouteFilter</span></span>
<span data-ttu-id="d57a8-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d57a8-118">The RouteFilter</span></span>

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

### <span data-ttu-id="d57a8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d57a8-119">-Confirm</span></span>
<span data-ttu-id="d57a8-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d57a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d57a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57a8-121">-WhatIf</span></span>
<span data-ttu-id="d57a8-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d57a8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d57a8-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d57a8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d57a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57a8-124">CommonParameters</span></span>
<span data-ttu-id="d57a8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d57a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57a8-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57a8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57a8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d57a8-127">INPUTS</span></span>

### <span data-ttu-id="d57a8-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d57a8-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d57a8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d57a8-129">OUTPUTS</span></span>

### <span data-ttu-id="d57a8-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d57a8-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d57a8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d57a8-131">NOTES</span></span>

## <span data-ttu-id="d57a8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d57a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="d57a8-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d57a8-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="d57a8-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d57a8-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="d57a8-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d57a8-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="d57a8-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d57a8-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d57a8-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d57a8-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d57a8-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d57a8-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d57a8-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d57a8-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d57a8-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d57a8-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
