---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 98b5f30bfe3a829d276c435c9beef71cf8a2f7de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986628"
---
# <span data-ttu-id="4a1f7-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4a1f7-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="4a1f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1f7-103">Удалите подключение закрытой конечной точки из службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4a1f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a1f7-104">SYNTAX</span></span>

### <span data-ttu-id="4a1f7-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a1f7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a1f7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a1f7-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a1f7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a1f7-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a1f7-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a1f7-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a1f7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a1f7-109">DESCRIPTION</span></span>
<span data-ttu-id="4a1f7-110">Служба **Remove-AzSearchPrivateEndpointConnection** удаляет частное подключение конечной точки из службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4a1f7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a1f7-111">EXAMPLES</span></span>

### <span data-ttu-id="4a1f7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a1f7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="4a1f7-113">В этом примере подключение к частной конечной точке удаляется из службы поиска по имени.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="4a1f7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a1f7-114">PARAMETERS</span></span>

### <span data-ttu-id="4a1f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1f7-115">-DefaultProfile</span></span>
<span data-ttu-id="4a1f7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a1f7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4a1f7-117">-Force</span></span>
<span data-ttu-id="4a1f7-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4a1f7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a1f7-119">-InputObject</span></span>
<span data-ttu-id="4a1f7-120">Объект ввода подключения к закрытой конечной точке</span><span class="sxs-lookup"><span data-stu-id="4a1f7-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4a1f7-121">-Name</span></span>
<span data-ttu-id="4a1f7-122">Имя частного подключения конечной точки службы поиска Azure Cognitive Search</span><span class="sxs-lookup"><span data-stu-id="4a1f7-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f7-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4a1f7-123">-ParentObject</span></span>
<span data-ttu-id="4a1f7-124">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a1f7-125">-PassThru</span></span>
<span data-ttu-id="4a1f7-126">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4a1f7-127">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4a1f7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a1f7-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a1f7-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-129">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a1f7-130">-ResourceId</span></span>
<span data-ttu-id="4a1f7-131">Private link service resource id</span><span class="sxs-lookup"><span data-stu-id="4a1f7-131">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f7-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4a1f7-132">-ServiceName</span></span>
<span data-ttu-id="4a1f7-133">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-133">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1f7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a1f7-134">-Confirm</span></span>
<span data-ttu-id="4a1f7-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a1f7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a1f7-136">-WhatIf</span></span>
<span data-ttu-id="4a1f7-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a1f7-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a1f7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1f7-139">CommonParameters</span></span>
<span data-ttu-id="4a1f7-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a1f7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1f7-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a1f7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1f7-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a1f7-142">INPUTS</span></span>

### <span data-ttu-id="4a1f7-143">Нет</span><span class="sxs-lookup"><span data-stu-id="4a1f7-143">None</span></span>

## <span data-ttu-id="4a1f7-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a1f7-144">OUTPUTS</span></span>

### <span data-ttu-id="4a1f7-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a1f7-145">System.Boolean</span></span>

## <span data-ttu-id="4a1f7-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a1f7-146">NOTES</span></span>

## <span data-ttu-id="4a1f7-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a1f7-147">RELATED LINKS</span></span>

[<span data-ttu-id="4a1f7-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="4a1f7-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="4a1f7-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="4a1f7-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)