---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236481"
---
# <span data-ttu-id="56af4-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56af4-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="56af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56af4-102">SYNOPSIS</span></span>
<span data-ttu-id="56af4-103">Обновляет фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="56af4-103">Updates a route filter.</span></span>

## <span data-ttu-id="56af4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56af4-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56af4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56af4-105">DESCRIPTION</span></span>
<span data-ttu-id="56af4-106">**Cmdlet Set-AzApplicationGateway** обновляет фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="56af4-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="56af4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56af4-107">EXAMPLES</span></span>

### <span data-ttu-id="56af4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56af4-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="56af4-109">Эта команда обновляет фильтр маршрутов с параметрами в $rf переменной.</span><span class="sxs-lookup"><span data-stu-id="56af4-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="56af4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56af4-110">PARAMETERS</span></span>

### <span data-ttu-id="56af4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56af4-111">-AsJob</span></span>
<span data-ttu-id="56af4-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="56af4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56af4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56af4-113">-DefaultProfile</span></span>
<span data-ttu-id="56af4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56af4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56af4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="56af4-115">-Force</span></span>
<span data-ttu-id="56af4-116">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="56af4-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="56af4-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="56af4-117">-RouteFilter</span></span>
<span data-ttu-id="56af4-118">Маршрутизатор</span><span class="sxs-lookup"><span data-stu-id="56af4-118">The RouteFilter</span></span>

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

### <span data-ttu-id="56af4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56af4-119">-Confirm</span></span>
<span data-ttu-id="56af4-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="56af4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56af4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56af4-121">-WhatIf</span></span>
<span data-ttu-id="56af4-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56af4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56af4-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56af4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56af4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56af4-124">CommonParameters</span></span>
<span data-ttu-id="56af4-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56af4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56af4-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56af4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56af4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56af4-127">INPUTS</span></span>

### <span data-ttu-id="56af4-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56af4-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="56af4-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56af4-129">OUTPUTS</span></span>

### <span data-ttu-id="56af4-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56af4-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="56af4-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56af4-131">NOTES</span></span>

## <span data-ttu-id="56af4-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56af4-132">RELATED LINKS</span></span>

[<span data-ttu-id="56af4-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56af4-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="56af4-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56af4-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="56af4-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="56af4-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="56af4-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56af4-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="56af4-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56af4-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="56af4-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56af4-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="56af4-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56af4-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="56af4-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56af4-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
