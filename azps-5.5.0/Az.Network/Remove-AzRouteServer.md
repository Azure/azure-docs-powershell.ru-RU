---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 2b50d49c108408e1639b5f5f490c2aaafc7bbd82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225788"
---
# <span data-ttu-id="77be4-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="77be4-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="77be4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77be4-102">SYNOPSIS</span></span>
<span data-ttu-id="77be4-103">Удаляет azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="77be4-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="77be4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77be4-104">SYNTAX</span></span>

### <span data-ttu-id="77be4-105">RouteServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77be4-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77be4-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77be4-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77be4-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77be4-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77be4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77be4-108">DESCRIPTION</span></span>
<span data-ttu-id="77be4-109">**Из-за настройки Remove-AzRouteServer** удаляется azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="77be4-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="77be4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77be4-110">EXAMPLES</span></span>

### <span data-ttu-id="77be4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77be4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="77be4-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="77be4-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="77be4-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="77be4-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="77be4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77be4-114">PARAMETERS</span></span>

### <span data-ttu-id="77be4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77be4-115">-AsJob</span></span>
<span data-ttu-id="77be4-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="77be4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77be4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77be4-117">-DefaultProfile</span></span>
<span data-ttu-id="77be4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77be4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77be4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="77be4-119">-Force</span></span>
<span data-ttu-id="77be4-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="77be4-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="77be4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77be4-121">-InputObject</span></span>
<span data-ttu-id="77be4-122">Объект ввода сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="77be4-122">The route server input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServer
Parameter Sets: RouteServerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77be4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77be4-123">-PassThru</span></span>
<span data-ttu-id="77be4-124">Возвращает объект, представляющий элемент, с которым выполняется данной операция.</span><span class="sxs-lookup"><span data-stu-id="77be4-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="77be4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77be4-125">-ResourceGroupName</span></span>
<span data-ttu-id="77be4-126">Имя группы ресурсов сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="77be4-126">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77be4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77be4-127">-ResourceId</span></span>
<span data-ttu-id="77be4-128">ИД ресурса сервера маршрутных маршрутов.</span><span class="sxs-lookup"><span data-stu-id="77be4-128">The route server resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77be4-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="77be4-129">-RouteServerName</span></span>
<span data-ttu-id="77be4-130">Имя сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="77be4-130">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77be4-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77be4-131">-Confirm</span></span>
<span data-ttu-id="77be4-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77be4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77be4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77be4-133">-WhatIf</span></span>
<span data-ttu-id="77be4-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77be4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77be4-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="77be4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77be4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77be4-136">CommonParameters</span></span>
<span data-ttu-id="77be4-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77be4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77be4-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77be4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77be4-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77be4-139">INPUTS</span></span>

### <span data-ttu-id="77be4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="77be4-140">System.String</span></span>

### <span data-ttu-id="77be4-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="77be4-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="77be4-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77be4-142">OUTPUTS</span></span>

### <span data-ttu-id="77be4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77be4-143">System.Boolean</span></span>

## <span data-ttu-id="77be4-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77be4-144">NOTES</span></span>

## <span data-ttu-id="77be4-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77be4-145">RELATED LINKS</span></span>
