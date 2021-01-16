---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519956"
---
# <span data-ttu-id="2251e-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2251e-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="2251e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2251e-102">SYNOPSIS</span></span>
<span data-ttu-id="2251e-103">Удаляет фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2251e-103">Removes a route filter.</span></span>

## <span data-ttu-id="2251e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2251e-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2251e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2251e-105">DESCRIPTION</span></span>
<span data-ttu-id="2251e-106">Для **удаления фильтра маршрутов удаляется cmdlet Remove-AzRouteFilter.**</span><span class="sxs-lookup"><span data-stu-id="2251e-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="2251e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2251e-107">EXAMPLES</span></span>

### <span data-ttu-id="2251e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2251e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2251e-109">Команда удаляет фильтр маршрутов с именем RouteFilter01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2251e-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="2251e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2251e-110">PARAMETERS</span></span>

### <span data-ttu-id="2251e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2251e-111">-DefaultProfile</span></span>
<span data-ttu-id="2251e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2251e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2251e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2251e-113">-Force</span></span>
<span data-ttu-id="2251e-114">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2251e-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2251e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2251e-115">-Name</span></span>
<span data-ttu-id="2251e-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2251e-116">The resource name.</span></span>

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

### <span data-ttu-id="2251e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2251e-117">-PassThru</span></span>
<span data-ttu-id="2251e-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2251e-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="2251e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2251e-119">-ResourceGroupName</span></span>
<span data-ttu-id="2251e-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2251e-120">The resource group name.</span></span>

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

### <span data-ttu-id="2251e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2251e-121">-Confirm</span></span>
<span data-ttu-id="2251e-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2251e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2251e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2251e-123">-WhatIf</span></span>
<span data-ttu-id="2251e-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2251e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2251e-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2251e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2251e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2251e-126">CommonParameters</span></span>
<span data-ttu-id="2251e-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2251e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2251e-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2251e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2251e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2251e-129">INPUTS</span></span>

### <span data-ttu-id="2251e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2251e-130">System.String</span></span>

## <span data-ttu-id="2251e-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2251e-131">OUTPUTS</span></span>

### <span data-ttu-id="2251e-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2251e-132">System.Boolean</span></span>

## <span data-ttu-id="2251e-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2251e-133">NOTES</span></span>

## <span data-ttu-id="2251e-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2251e-134">RELATED LINKS</span></span>

[<span data-ttu-id="2251e-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2251e-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="2251e-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2251e-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="2251e-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2251e-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="2251e-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2251e-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2251e-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2251e-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2251e-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2251e-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2251e-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2251e-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2251e-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2251e-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
