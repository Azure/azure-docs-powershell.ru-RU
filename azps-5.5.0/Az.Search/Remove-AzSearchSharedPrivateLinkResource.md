---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 922989583a071384de98343e12d48ce68cc32db8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239992"
---
# <span data-ttu-id="8e378-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8e378-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="8e378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e378-102">SYNOPSIS</span></span>
<span data-ttu-id="8e378-103">Удалите ресурс общей личной ссылки из службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="8e378-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8e378-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e378-104">SYNTAX</span></span>

### <span data-ttu-id="8e378-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e378-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e378-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e378-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e378-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e378-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e378-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e378-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e378-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e378-109">DESCRIPTION</span></span>
<span data-ttu-id="8e378-110">С **помощью cmdlet Remove-AzSearchSharedPrivateLinkResource** ресурс общей частной ссылки удаляется из службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="8e378-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8e378-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e378-111">EXAMPLES</span></span>

### <span data-ttu-id="8e378-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e378-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="8e378-113">В этом примере удаляется ресурс общей частной ссылки по имени службы Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="8e378-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8e378-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e378-114">PARAMETERS</span></span>

### <span data-ttu-id="8e378-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e378-115">-AsJob</span></span>
<span data-ttu-id="8e378-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8e378-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e378-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e378-117">-DefaultProfile</span></span>
<span data-ttu-id="8e378-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e378-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e378-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8e378-119">-Force</span></span>
<span data-ttu-id="8e378-120">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8e378-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8e378-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e378-121">-InputObject</span></span>
<span data-ttu-id="8e378-122">Объект ввода ресурсов общей частной ссылки</span><span class="sxs-lookup"><span data-stu-id="8e378-122">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e378-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8e378-123">-Name</span></span>
<span data-ttu-id="8e378-124">Ресурс личной ссылки "Общий поиск" в Azure Cognitive Search</span><span class="sxs-lookup"><span data-stu-id="8e378-124">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="8e378-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e378-125">-ParentObject</span></span>
<span data-ttu-id="8e378-126">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="8e378-126">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="8e378-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e378-127">-PassThru</span></span>
<span data-ttu-id="8e378-128">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8e378-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8e378-129">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="8e378-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8e378-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e378-130">-ResourceGroupName</span></span>
<span data-ttu-id="8e378-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e378-131">Resource Group name.</span></span>

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

### <span data-ttu-id="8e378-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e378-132">-ResourceId</span></span>
<span data-ttu-id="8e378-133">ИД ресурса общей личной ссылки</span><span class="sxs-lookup"><span data-stu-id="8e378-133">Shared private link resource id</span></span>

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

### <span data-ttu-id="8e378-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8e378-134">-ServiceName</span></span>
<span data-ttu-id="8e378-135">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="8e378-135">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="8e378-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e378-136">-Confirm</span></span>
<span data-ttu-id="8e378-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8e378-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e378-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e378-138">-WhatIf</span></span>
<span data-ttu-id="8e378-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e378-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e378-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8e378-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e378-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e378-141">CommonParameters</span></span>
<span data-ttu-id="8e378-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e378-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e378-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e378-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e378-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e378-144">INPUTS</span></span>

### <span data-ttu-id="8e378-145">Нет</span><span class="sxs-lookup"><span data-stu-id="8e378-145">None</span></span>

## <span data-ttu-id="8e378-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e378-146">OUTPUTS</span></span>

### <span data-ttu-id="8e378-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e378-147">System.Boolean</span></span>

## <span data-ttu-id="8e378-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e378-148">NOTES</span></span>

## <span data-ttu-id="8e378-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e378-149">RELATED LINKS</span></span>

[<span data-ttu-id="8e378-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="8e378-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="8e378-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="8e378-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="8e378-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="8e378-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)