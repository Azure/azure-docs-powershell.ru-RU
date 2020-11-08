---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236008"
---
# <span data-ttu-id="bf03d-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bf03d-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="bf03d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf03d-102">SYNOPSIS</span></span>
<span data-ttu-id="bf03d-103">Удаление фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="bf03d-103">Removes a route filter.</span></span>

## <span data-ttu-id="bf03d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf03d-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf03d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf03d-105">DESCRIPTION</span></span>
<span data-ttu-id="bf03d-106">Командлет **Remove-AzRouteFilter** удаляет фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="bf03d-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="bf03d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf03d-107">EXAMPLES</span></span>

### <span data-ttu-id="bf03d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf03d-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bf03d-109">Команда удаляет фильтр маршрутов с именем RouteFilter01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="bf03d-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="bf03d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf03d-110">PARAMETERS</span></span>

### <span data-ttu-id="bf03d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf03d-111">-DefaultProfile</span></span>
<span data-ttu-id="bf03d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf03d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf03d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bf03d-113">-Force</span></span>
<span data-ttu-id="bf03d-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bf03d-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bf03d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf03d-115">-Name</span></span>
<span data-ttu-id="bf03d-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="bf03d-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf03d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf03d-117">-PassThru</span></span>
<span data-ttu-id="bf03d-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="bf03d-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="bf03d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf03d-119">-ResourceGroupName</span></span>
<span data-ttu-id="bf03d-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bf03d-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf03d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf03d-121">-Confirm</span></span>
<span data-ttu-id="bf03d-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bf03d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf03d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf03d-123">-WhatIf</span></span>
<span data-ttu-id="bf03d-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bf03d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf03d-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bf03d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf03d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf03d-126">CommonParameters</span></span>
<span data-ttu-id="bf03d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf03d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf03d-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf03d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf03d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf03d-129">INPUTS</span></span>

### <span data-ttu-id="bf03d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bf03d-130">System.String</span></span>

## <span data-ttu-id="bf03d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf03d-131">OUTPUTS</span></span>

### <span data-ttu-id="bf03d-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf03d-132">System.Boolean</span></span>

## <span data-ttu-id="bf03d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf03d-133">NOTES</span></span>

## <span data-ttu-id="bf03d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf03d-134">RELATED LINKS</span></span>

[<span data-ttu-id="bf03d-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bf03d-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="bf03d-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bf03d-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="bf03d-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bf03d-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="bf03d-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf03d-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bf03d-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf03d-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bf03d-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf03d-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bf03d-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf03d-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bf03d-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf03d-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
