---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: ab0da083957fe18d1bb30d0b3d08d33515d0ff13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904398"
---
# <span data-ttu-id="16e32-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16e32-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="16e32-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16e32-102">SYNOPSIS</span></span>
<span data-ttu-id="16e32-103">Обновляет фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="16e32-103">Updates a route filter.</span></span>

## <span data-ttu-id="16e32-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16e32-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e32-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16e32-105">DESCRIPTION</span></span>
<span data-ttu-id="16e32-106">Командлет **Set-AzApplicationGateway** обновляет фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="16e32-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="16e32-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16e32-107">EXAMPLES</span></span>

### <span data-ttu-id="16e32-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16e32-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="16e32-109">Эта команда обновляет фильтр маршрутов с параметрами, заданными в переменной $rf.</span><span class="sxs-lookup"><span data-stu-id="16e32-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="16e32-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16e32-110">PARAMETERS</span></span>

### <span data-ttu-id="16e32-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16e32-111">-AsJob</span></span>
<span data-ttu-id="16e32-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="16e32-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16e32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e32-113">-DefaultProfile</span></span>
<span data-ttu-id="16e32-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16e32-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16e32-115">-Force</span><span class="sxs-lookup"><span data-stu-id="16e32-115">-Force</span></span>
<span data-ttu-id="16e32-116">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="16e32-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="16e32-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="16e32-117">-RouteFilter</span></span>
<span data-ttu-id="16e32-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="16e32-118">The RouteFilter</span></span>

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

### <span data-ttu-id="16e32-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16e32-119">-Confirm</span></span>
<span data-ttu-id="16e32-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16e32-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e32-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e32-121">-WhatIf</span></span>
<span data-ttu-id="16e32-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16e32-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16e32-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16e32-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e32-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e32-124">CommonParameters</span></span>
<span data-ttu-id="16e32-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16e32-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e32-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e32-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e32-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16e32-127">INPUTS</span></span>

### <span data-ttu-id="16e32-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16e32-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="16e32-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16e32-129">OUTPUTS</span></span>

### <span data-ttu-id="16e32-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16e32-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="16e32-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="16e32-131">NOTES</span></span>

## <span data-ttu-id="16e32-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16e32-132">RELATED LINKS</span></span>

[<span data-ttu-id="16e32-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16e32-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="16e32-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16e32-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="16e32-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16e32-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="16e32-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e32-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="16e32-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e32-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="16e32-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e32-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="16e32-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e32-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="16e32-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16e32-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
