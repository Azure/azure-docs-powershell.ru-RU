---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417676"
---
# <span data-ttu-id="674e6-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="674e6-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="674e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="674e6-102">SYNOPSIS</span></span>
<span data-ttu-id="674e6-103">Обновляет сохраненный поиск, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="674e6-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="674e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="674e6-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="674e6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="674e6-105">DESCRIPTION</span></span>
<span data-ttu-id="674e6-106">Для **уже сохраненного** поискового запроса обновляется сохраненный поиск, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="674e6-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="674e6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="674e6-107">EXAMPLES</span></span>

### <span data-ttu-id="674e6-108">Пример 1. Набор сохраненного поиска с обновленными свойствами</span><span class="sxs-lookup"><span data-stu-id="674e6-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="674e6-109">Эта команда задает сохраненный поиск с обновленными свойствами.</span><span class="sxs-lookup"><span data-stu-id="674e6-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="674e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="674e6-110">PARAMETERS</span></span>

### <span data-ttu-id="674e6-111">-Category</span><span class="sxs-lookup"><span data-stu-id="674e6-111">-Category</span></span>
<span data-ttu-id="674e6-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="674e6-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="674e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="674e6-113">-DefaultProfile</span></span>
<span data-ttu-id="674e6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="674e6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="674e6-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="674e6-115">-DisplayName</span></span>
<span data-ttu-id="674e6-116">Указывает отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="674e6-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="674e6-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="674e6-117">-ETag</span></span>
<span data-ttu-id="674e6-118">Определяет имя ETag.</span><span class="sxs-lookup"><span data-stu-id="674e6-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674e6-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="674e6-119">-FunctionAlias</span></span>
<span data-ttu-id="674e6-120">Псевдоним функции, если запрос служит функцией.</span><span class="sxs-lookup"><span data-stu-id="674e6-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674e6-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="674e6-121">-FunctionParameter</span></span>
<span data-ttu-id="674e6-122">Необязательные параметры функции, если запрос служит функцией.</span><span class="sxs-lookup"><span data-stu-id="674e6-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="674e6-123">Значение должно иметь следующий формат: "параметр-имя1:тип1 = default_value1, параметр-имя2:тип2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="674e6-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="674e6-124">Дополнительные примеры и синтаксис нужно найти в соответствующем синтаксисе. https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions</span><span class="sxs-lookup"><span data-stu-id="674e6-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674e6-125">-Query</span><span class="sxs-lookup"><span data-stu-id="674e6-125">-Query</span></span>
<span data-ttu-id="674e6-126">Указывает имя запроса.</span><span class="sxs-lookup"><span data-stu-id="674e6-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="674e6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="674e6-127">-ResourceGroupName</span></span>
<span data-ttu-id="674e6-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="674e6-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="674e6-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="674e6-129">-SavedSearchId</span></span>
<span data-ttu-id="674e6-130">Определяет сохраненный ИД поиска.</span><span class="sxs-lookup"><span data-stu-id="674e6-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="674e6-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="674e6-131">-Tag</span></span>
<span data-ttu-id="674e6-132">Сохраненные теги поиска.</span><span class="sxs-lookup"><span data-stu-id="674e6-132">The saved search tags.</span></span>

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

### <span data-ttu-id="674e6-133">-Версия</span><span class="sxs-lookup"><span data-stu-id="674e6-133">-Version</span></span>
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

### <span data-ttu-id="674e6-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="674e6-134">-WorkspaceName</span></span>
<span data-ttu-id="674e6-135">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="674e6-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="674e6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="674e6-136">CommonParameters</span></span>
<span data-ttu-id="674e6-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="674e6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="674e6-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="674e6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="674e6-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="674e6-139">INPUTS</span></span>

### <span data-ttu-id="674e6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="674e6-140">System.String</span></span>

### <span data-ttu-id="674e6-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="674e6-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="674e6-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="674e6-142">System.Int64</span></span>

## <span data-ttu-id="674e6-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="674e6-143">OUTPUTS</span></span>

### <span data-ttu-id="674e6-144">System.Net.httpStatusCode</span><span class="sxs-lookup"><span data-stu-id="674e6-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="674e6-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="674e6-145">NOTES</span></span>

## <span data-ttu-id="674e6-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="674e6-146">RELATED LINKS</span></span>

[<span data-ttu-id="674e6-147">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="674e6-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


