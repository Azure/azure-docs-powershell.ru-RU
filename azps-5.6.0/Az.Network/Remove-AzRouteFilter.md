---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 0b75cdb63d2a8bb3c01a93a90ee01db096cf7fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976616"
---
# <span data-ttu-id="a2f2b-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a2f2b-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="a2f2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f2b-103">Удаляет фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-103">Removes a route filter.</span></span>

## <span data-ttu-id="a2f2b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2f2b-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2f2b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="a2f2b-106">Для **удаления фильтра маршрутов удаляется cmdlet Remove-AzRouteFilter.**</span><span class="sxs-lookup"><span data-stu-id="a2f2b-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="a2f2b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2f2b-107">EXAMPLES</span></span>

### <span data-ttu-id="a2f2b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2f2b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a2f2b-109">Команда удаляет фильтр маршрутов с именем RouteFilter01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a2f2b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2f2b-110">PARAMETERS</span></span>

### <span data-ttu-id="a2f2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f2b-111">-DefaultProfile</span></span>
<span data-ttu-id="a2f2b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2f2b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a2f2b-113">-Force</span></span>
<span data-ttu-id="a2f2b-114">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a2f2b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a2f2b-115">-Name</span></span>
<span data-ttu-id="a2f2b-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-116">The resource name.</span></span>

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

### <span data-ttu-id="a2f2b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2f2b-117">-PassThru</span></span>
<span data-ttu-id="a2f2b-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="a2f2b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f2b-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2f2b-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-120">The resource group name.</span></span>

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

### <span data-ttu-id="a2f2b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2f2b-121">-Confirm</span></span>
<span data-ttu-id="a2f2b-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2f2b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2f2b-123">-WhatIf</span></span>
<span data-ttu-id="a2f2b-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2f2b-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2f2b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f2b-126">CommonParameters</span></span>
<span data-ttu-id="a2f2b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f2b-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2f2b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f2b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2f2b-129">INPUTS</span></span>

### <span data-ttu-id="a2f2b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a2f2b-130">System.String</span></span>

## <span data-ttu-id="a2f2b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2f2b-131">OUTPUTS</span></span>

### <span data-ttu-id="a2f2b-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2f2b-132">System.Boolean</span></span>

## <span data-ttu-id="a2f2b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2f2b-133">NOTES</span></span>

## <span data-ttu-id="a2f2b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2f2b-134">RELATED LINKS</span></span>

[<span data-ttu-id="a2f2b-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a2f2b-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="a2f2b-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a2f2b-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="a2f2b-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a2f2b-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="a2f2b-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a2f2b-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a2f2b-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a2f2b-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a2f2b-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a2f2b-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a2f2b-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a2f2b-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a2f2b-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a2f2b-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
