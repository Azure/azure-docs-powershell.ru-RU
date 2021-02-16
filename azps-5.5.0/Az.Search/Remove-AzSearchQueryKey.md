---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: 3d4610f83b348864fc57cf6894db1ab7455a8485
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240008"
---
# <span data-ttu-id="896a0-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="896a0-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="896a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="896a0-102">SYNOPSIS</span></span>
<span data-ttu-id="896a0-103">Удалите ключ запроса из службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="896a0-103">Remove the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="896a0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="896a0-104">SYNTAX</span></span>

### <span data-ttu-id="896a0-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="896a0-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="896a0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="896a0-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="896a0-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="896a0-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="896a0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="896a0-108">DESCRIPTION</span></span>
<span data-ttu-id="896a0-109">С **помощью cmdlet Remove-AzSearchQueryKey** клавиша запроса удаляется из службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="896a0-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="896a0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="896a0-110">EXAMPLES</span></span>

### <span data-ttu-id="896a0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="896a0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="896a0-112">В этом примере ключ запроса удаляется из службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="896a0-112">The example removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="896a0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="896a0-113">PARAMETERS</span></span>

### <span data-ttu-id="896a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="896a0-114">-DefaultProfile</span></span>
<span data-ttu-id="896a0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="896a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="896a0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="896a0-116">-Force</span></span>
<span data-ttu-id="896a0-117">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="896a0-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="896a0-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="896a0-118">-KeyValue</span></span>
<span data-ttu-id="896a0-119">Значение ключа запроса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="896a0-119">Azure Cognitive Search Service query key value.</span></span>

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

### <span data-ttu-id="896a0-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="896a0-120">-ParentObject</span></span>
<span data-ttu-id="896a0-121">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="896a0-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="896a0-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="896a0-122">-ParentResourceId</span></span>
<span data-ttu-id="896a0-123">ИД ресурса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="896a0-123">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896a0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="896a0-124">-PassThru</span></span>
<span data-ttu-id="896a0-125">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="896a0-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="896a0-126">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="896a0-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="896a0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="896a0-127">-ResourceGroupName</span></span>
<span data-ttu-id="896a0-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="896a0-128">Resource Group name.</span></span>

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

### <span data-ttu-id="896a0-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="896a0-129">-ServiceName</span></span>
<span data-ttu-id="896a0-130">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="896a0-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="896a0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="896a0-131">-Confirm</span></span>
<span data-ttu-id="896a0-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="896a0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="896a0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="896a0-133">-WhatIf</span></span>
<span data-ttu-id="896a0-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="896a0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="896a0-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="896a0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="896a0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896a0-136">CommonParameters</span></span>
<span data-ttu-id="896a0-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="896a0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="896a0-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="896a0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896a0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="896a0-139">INPUTS</span></span>

### <span data-ttu-id="896a0-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="896a0-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="896a0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="896a0-141">System.String</span></span>

## <span data-ttu-id="896a0-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="896a0-142">OUTPUTS</span></span>

### <span data-ttu-id="896a0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="896a0-143">System.Boolean</span></span>

## <span data-ttu-id="896a0-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="896a0-144">NOTES</span></span>

## <span data-ttu-id="896a0-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="896a0-145">RELATED LINKS</span></span>

[<span data-ttu-id="896a0-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="896a0-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="896a0-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="896a0-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
