---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: cba56fd21263d4accba296cd7aab181f18b09200
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989904"
---
# <span data-ttu-id="fd1e9-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="fd1e9-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="fd1e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd1e9-103">Создает новый сохраненный поиск с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="fd1e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd1e9-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd1e9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="fd1e9-106">С **помощью cmdlet New-AzOperationalInsightsSavedSearch** создается новый сохраненный поиск с указанными параметрами рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="fd1e9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd1e9-107">EXAMPLES</span></span>

### <span data-ttu-id="fd1e9-108">Пример 1. Создание сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="fd1e9-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="fd1e9-109">Эта команда создает новый сохраненный поиск.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="fd1e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd1e9-110">PARAMETERS</span></span>

### <span data-ttu-id="fd1e9-111">-Category</span><span class="sxs-lookup"><span data-stu-id="fd1e9-111">-Category</span></span>
<span data-ttu-id="fd1e9-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="fd1e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd1e9-113">-DefaultProfile</span></span>
<span data-ttu-id="fd1e9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fd1e9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd1e9-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fd1e9-115">-DisplayName</span></span>
<span data-ttu-id="fd1e9-116">Определяет сохраненное отображаемого имя поиска.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="fd1e9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fd1e9-117">-Force</span></span>
<span data-ttu-id="fd1e9-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd1e9-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="fd1e9-119">-FunctionAlias</span></span>
<span data-ttu-id="fd1e9-120">Псевдоним функции, если запрос служит функцией.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="fd1e9-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="fd1e9-121">-FunctionParameter</span></span>
<span data-ttu-id="fd1e9-122">Необязательные параметры функции, если запрос служит функцией.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="fd1e9-123">Значение должно иметь следующий формат: "параметр-имя1:тип1 = default_value1, параметр-имя2:тип2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="fd1e9-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="fd1e9-124">Дополнительные примеры и синтаксис нужно найти в соответствующем синтаксисе. https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions</span><span class="sxs-lookup"><span data-stu-id="fd1e9-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="fd1e9-125">-Query</span><span class="sxs-lookup"><span data-stu-id="fd1e9-125">-Query</span></span>
<span data-ttu-id="fd1e9-126">Определяет выражение запроса для сохраненного поиска.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="fd1e9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd1e9-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd1e9-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="fd1e9-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="fd1e9-129">-SavedSearchId</span></span>
<span data-ttu-id="fd1e9-130">Определяет сохраненный ИД поиска.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="fd1e9-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd1e9-131">-Tag</span></span>
<span data-ttu-id="fd1e9-132">Сохраненные теги поиска.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-132">The saved search tags.</span></span>

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

### <span data-ttu-id="fd1e9-133">-Version</span><span class="sxs-lookup"><span data-stu-id="fd1e9-133">-Version</span></span>
<span data-ttu-id="fd1e9-134">Определяет версию.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-134">Specifies the version.</span></span>

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

### <span data-ttu-id="fd1e9-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd1e9-135">-WorkspaceName</span></span>
<span data-ttu-id="fd1e9-136">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="fd1e9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd1e9-137">-Confirm</span></span>
<span data-ttu-id="fd1e9-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd1e9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd1e9-139">-WhatIf</span></span>
<span data-ttu-id="fd1e9-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd1e9-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd1e9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd1e9-142">CommonParameters</span></span>
<span data-ttu-id="fd1e9-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd1e9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd1e9-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd1e9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd1e9-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd1e9-145">INPUTS</span></span>

### <span data-ttu-id="fd1e9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fd1e9-146">System.String</span></span>

### <span data-ttu-id="fd1e9-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd1e9-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fd1e9-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="fd1e9-148">System.Int64</span></span>

## <span data-ttu-id="fd1e9-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd1e9-149">OUTPUTS</span></span>

### <span data-ttu-id="fd1e9-150">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="fd1e9-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="fd1e9-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd1e9-151">NOTES</span></span>

## <span data-ttu-id="fd1e9-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd1e9-152">RELATED LINKS</span></span>

[<span data-ttu-id="fd1e9-153">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fd1e9-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


