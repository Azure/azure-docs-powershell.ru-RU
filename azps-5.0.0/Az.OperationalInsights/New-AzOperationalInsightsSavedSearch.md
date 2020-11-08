---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246038"
---
# <span data-ttu-id="71f20-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="71f20-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="71f20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71f20-102">SYNOPSIS</span></span>
<span data-ttu-id="71f20-103">Создание нового сохраненного поиска с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="71f20-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="71f20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71f20-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71f20-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71f20-105">DESCRIPTION</span></span>
<span data-ttu-id="71f20-106">Командлет **New-AzOperationalInsightsSavedSearch** создает новый сохраненный поиск с заданными параметрами для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="71f20-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="71f20-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71f20-107">EXAMPLES</span></span>

### <span data-ttu-id="71f20-108">Пример 1: создание нового сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="71f20-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="71f20-109">Эта команда создает новый сохраненный поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="71f20-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="71f20-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71f20-110">PARAMETERS</span></span>

### <span data-ttu-id="71f20-111">-Категория</span><span class="sxs-lookup"><span data-stu-id="71f20-111">-Category</span></span>
<span data-ttu-id="71f20-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="71f20-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="71f20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f20-113">-DefaultProfile</span></span>
<span data-ttu-id="71f20-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="71f20-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71f20-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="71f20-115">-DisplayName</span></span>
<span data-ttu-id="71f20-116">Указывает имя сохраненного отображаемого поиска.</span><span class="sxs-lookup"><span data-stu-id="71f20-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="71f20-117">-Force</span><span class="sxs-lookup"><span data-stu-id="71f20-117">-Force</span></span>
<span data-ttu-id="71f20-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="71f20-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71f20-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="71f20-119">-FunctionAlias</span></span>
<span data-ttu-id="71f20-120">Псевдоним функции, если запрос играет роль функции.</span><span class="sxs-lookup"><span data-stu-id="71f20-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="71f20-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="71f20-121">-FunctionParameter</span></span>
<span data-ttu-id="71f20-122">Необязательные параметры функции, если Query используется как функция.</span><span class="sxs-lookup"><span data-stu-id="71f20-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="71f20-123">Значение должно быть представлено в следующем формате: "param-файл1: тип1 = default_value1, param-имя2: тип2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="71f20-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="71f20-124">Дополнительные примеры и правильный синтаксис см https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="71f20-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="71f20-125">-Query</span><span class="sxs-lookup"><span data-stu-id="71f20-125">-Query</span></span>
<span data-ttu-id="71f20-126">Указывает выражение запроса для сохраненного поиска.</span><span class="sxs-lookup"><span data-stu-id="71f20-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="71f20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f20-127">-ResourceGroupName</span></span>
<span data-ttu-id="71f20-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71f20-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="71f20-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="71f20-129">-SavedSearchId</span></span>
<span data-ttu-id="71f20-130">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="71f20-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="71f20-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="71f20-131">-Tag</span></span>
<span data-ttu-id="71f20-132">Сохраненные теги поиска.</span><span class="sxs-lookup"><span data-stu-id="71f20-132">The saved search tags.</span></span>

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

### <span data-ttu-id="71f20-133">-Version</span><span class="sxs-lookup"><span data-stu-id="71f20-133">-Version</span></span>
<span data-ttu-id="71f20-134">Указывает версию.</span><span class="sxs-lookup"><span data-stu-id="71f20-134">Specifies the version.</span></span>

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

### <span data-ttu-id="71f20-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="71f20-135">-WorkspaceName</span></span>
<span data-ttu-id="71f20-136">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="71f20-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="71f20-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71f20-137">-Confirm</span></span>
<span data-ttu-id="71f20-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71f20-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71f20-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71f20-139">-WhatIf</span></span>
<span data-ttu-id="71f20-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71f20-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71f20-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71f20-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71f20-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f20-142">CommonParameters</span></span>
<span data-ttu-id="71f20-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71f20-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f20-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71f20-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f20-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71f20-145">INPUTS</span></span>

### <span data-ttu-id="71f20-146">System. String</span><span class="sxs-lookup"><span data-stu-id="71f20-146">System.String</span></span>

### <span data-ttu-id="71f20-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="71f20-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="71f20-148">System. Int64</span><span class="sxs-lookup"><span data-stu-id="71f20-148">System.Int64</span></span>

## <span data-ttu-id="71f20-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71f20-149">OUTPUTS</span></span>

### <span data-ttu-id="71f20-150">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="71f20-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="71f20-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="71f20-151">NOTES</span></span>

## <span data-ttu-id="71f20-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71f20-152">RELATED LINKS</span></span>

[<span data-ttu-id="71f20-153">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="71f20-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


