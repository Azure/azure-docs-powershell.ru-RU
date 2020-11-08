---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248075"
---
# <span data-ttu-id="09e43-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="09e43-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="09e43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09e43-102">SYNOPSIS</span></span>
<span data-ttu-id="09e43-103">Обновление сохраненного поискового запроса, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="09e43-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="09e43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09e43-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09e43-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09e43-105">DESCRIPTION</span></span>
<span data-ttu-id="09e43-106">Командлет **Set-AzOperationalInsightsSavedSearch** обновляет сохраненный поиск, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="09e43-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="09e43-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09e43-107">EXAMPLES</span></span>

### <span data-ttu-id="09e43-108">Пример 1: Установка сохраненного поиска с обновленными свойствами</span><span class="sxs-lookup"><span data-stu-id="09e43-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="09e43-109">Эта команда задает сохраненный поиск с обновленными свойствами.</span><span class="sxs-lookup"><span data-stu-id="09e43-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="09e43-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09e43-110">PARAMETERS</span></span>

### <span data-ttu-id="09e43-111">-Категория</span><span class="sxs-lookup"><span data-stu-id="09e43-111">-Category</span></span>
<span data-ttu-id="09e43-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="09e43-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="09e43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e43-113">-DefaultProfile</span></span>
<span data-ttu-id="09e43-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="09e43-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09e43-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="09e43-115">-DisplayName</span></span>
<span data-ttu-id="09e43-116">Задает отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="09e43-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="09e43-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="09e43-117">-ETag</span></span>
<span data-ttu-id="09e43-118">Указывает имя ETag.</span><span class="sxs-lookup"><span data-stu-id="09e43-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="09e43-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="09e43-119">-FunctionAlias</span></span>
<span data-ttu-id="09e43-120">Псевдоним функции, если запрос играет роль функции.</span><span class="sxs-lookup"><span data-stu-id="09e43-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="09e43-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="09e43-121">-FunctionParameter</span></span>
<span data-ttu-id="09e43-122">Необязательные параметры функции, если Query используется как функция.</span><span class="sxs-lookup"><span data-stu-id="09e43-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="09e43-123">Значение должно быть представлено в следующем формате: "param-файл1: тип1 = default_value1, param-имя2: тип2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="09e43-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="09e43-124">Дополнительные примеры и правильный синтаксис см https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="09e43-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="09e43-125">-Query</span><span class="sxs-lookup"><span data-stu-id="09e43-125">-Query</span></span>
<span data-ttu-id="09e43-126">Указывает имя запроса.</span><span class="sxs-lookup"><span data-stu-id="09e43-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="09e43-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e43-127">-ResourceGroupName</span></span>
<span data-ttu-id="09e43-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09e43-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="09e43-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="09e43-129">-SavedSearchId</span></span>
<span data-ttu-id="09e43-130">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="09e43-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="09e43-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="09e43-131">-Tag</span></span>
<span data-ttu-id="09e43-132">Сохраненные теги поиска.</span><span class="sxs-lookup"><span data-stu-id="09e43-132">The saved search tags.</span></span>

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

### <span data-ttu-id="09e43-133">-Version</span><span class="sxs-lookup"><span data-stu-id="09e43-133">-Version</span></span>
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

### <span data-ttu-id="09e43-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09e43-134">-WorkspaceName</span></span>
<span data-ttu-id="09e43-135">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="09e43-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="09e43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e43-136">CommonParameters</span></span>
<span data-ttu-id="09e43-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09e43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e43-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09e43-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e43-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09e43-139">INPUTS</span></span>

### <span data-ttu-id="09e43-140">System. String</span><span class="sxs-lookup"><span data-stu-id="09e43-140">System.String</span></span>

### <span data-ttu-id="09e43-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="09e43-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="09e43-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="09e43-142">System.Int64</span></span>

## <span data-ttu-id="09e43-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09e43-143">OUTPUTS</span></span>

### <span data-ttu-id="09e43-144">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="09e43-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="09e43-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="09e43-145">NOTES</span></span>

## <span data-ttu-id="09e43-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09e43-146">RELATED LINKS</span></span>

[<span data-ttu-id="09e43-147">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="09e43-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


