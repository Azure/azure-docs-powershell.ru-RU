---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506822"
---
# <span data-ttu-id="245ae-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="245ae-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="245ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="245ae-102">SYNOPSIS</span></span>
<span data-ttu-id="245ae-103">Создает новый сохраненный поиск с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="245ae-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="245ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="245ae-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="245ae-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="245ae-105">DESCRIPTION</span></span>
<span data-ttu-id="245ae-106">С **помощью cmdlet New-AzOperationalInsightsSavedSearch** создается новый сохраненный поиск с указанными параметрами рабочей области.</span><span class="sxs-lookup"><span data-stu-id="245ae-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="245ae-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="245ae-107">EXAMPLES</span></span>

### <span data-ttu-id="245ae-108">Пример 1. Создание сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="245ae-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="245ae-109">Эта команда создает новый сохраненный поиск.</span><span class="sxs-lookup"><span data-stu-id="245ae-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="245ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="245ae-110">PARAMETERS</span></span>

### <span data-ttu-id="245ae-111">-Category</span><span class="sxs-lookup"><span data-stu-id="245ae-111">-Category</span></span>
<span data-ttu-id="245ae-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="245ae-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245ae-113">-DefaultProfile</span></span>
<span data-ttu-id="245ae-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="245ae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="245ae-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="245ae-115">-DisplayName</span></span>
<span data-ttu-id="245ae-116">Указывает сохраненное отображаемого имя поиска.</span><span class="sxs-lookup"><span data-stu-id="245ae-116">Specifies the saved search display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-117">-Force</span><span class="sxs-lookup"><span data-stu-id="245ae-117">-Force</span></span>
<span data-ttu-id="245ae-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="245ae-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="245ae-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="245ae-119">-FunctionAlias</span></span>
<span data-ttu-id="245ae-120">Псевдоним функции, если запрос служит функцией.</span><span class="sxs-lookup"><span data-stu-id="245ae-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="245ae-121">-FunctionParameter</span></span>
<span data-ttu-id="245ae-122">Необязательные параметры функции, если запрос служит функцией.</span><span class="sxs-lookup"><span data-stu-id="245ae-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="245ae-123">Значение должно иметь следующий формат: "параметр-имя1:тип1 = default_value1, параметр-имя2:тип2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="245ae-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="245ae-124">Дополнительные примеры и синтаксис нужно найти в соответствующем синтаксисе. https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions</span><span class="sxs-lookup"><span data-stu-id="245ae-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-125">-Query</span><span class="sxs-lookup"><span data-stu-id="245ae-125">-Query</span></span>
<span data-ttu-id="245ae-126">Определяет выражение запроса для сохраненного поиска.</span><span class="sxs-lookup"><span data-stu-id="245ae-126">Specifies the query expression for the saved search.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="245ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="245ae-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="245ae-128">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="245ae-129">-SavedSearchId</span></span>
<span data-ttu-id="245ae-130">Определяет сохраненный ИД поиска.</span><span class="sxs-lookup"><span data-stu-id="245ae-130">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="245ae-131">-Tag</span></span>
<span data-ttu-id="245ae-132">Сохраненные теги поиска.</span><span class="sxs-lookup"><span data-stu-id="245ae-132">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-133">-Версия</span><span class="sxs-lookup"><span data-stu-id="245ae-133">-Version</span></span>
<span data-ttu-id="245ae-134">Определяет версию.</span><span class="sxs-lookup"><span data-stu-id="245ae-134">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="245ae-135">-WorkspaceName</span></span>
<span data-ttu-id="245ae-136">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="245ae-136">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="245ae-137">-Confirm</span></span>
<span data-ttu-id="245ae-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="245ae-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="245ae-139">-WhatIf</span></span>
<span data-ttu-id="245ae-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="245ae-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="245ae-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="245ae-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245ae-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245ae-142">CommonParameters</span></span>
<span data-ttu-id="245ae-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="245ae-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245ae-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="245ae-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245ae-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="245ae-145">INPUTS</span></span>

### <span data-ttu-id="245ae-146">System.String</span><span class="sxs-lookup"><span data-stu-id="245ae-146">System.String</span></span>

### <span data-ttu-id="245ae-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="245ae-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="245ae-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="245ae-148">System.Int64</span></span>

## <span data-ttu-id="245ae-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="245ae-149">OUTPUTS</span></span>

### <span data-ttu-id="245ae-150">System.Net.httpStatusCode</span><span class="sxs-lookup"><span data-stu-id="245ae-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="245ae-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="245ae-151">NOTES</span></span>

## <span data-ttu-id="245ae-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="245ae-152">RELATED LINKS</span></span>

[<span data-ttu-id="245ae-153">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="245ae-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


