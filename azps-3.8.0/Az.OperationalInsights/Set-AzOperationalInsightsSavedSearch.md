---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 441e27692c0f61f040feb7ca01e7f2514fc72320
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077283"
---
# <span data-ttu-id="2e1aa-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2e1aa-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="2e1aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1aa-103">Обновление сохраненного поискового запроса, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="2e1aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e1aa-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e1aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e1aa-105">DESCRIPTION</span></span>
<span data-ttu-id="2e1aa-106">Командлет **Set-AzOperationalInsightsSavedSearch** обновляет сохраненный поиск, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="2e1aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e1aa-107">EXAMPLES</span></span>

### <span data-ttu-id="2e1aa-108">Пример 1: Установка сохраненного поиска с обновленными свойствами</span><span class="sxs-lookup"><span data-stu-id="2e1aa-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="2e1aa-109">Эта команда задает сохраненный поиск с обновленными свойствами.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="2e1aa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e1aa-110">PARAMETERS</span></span>

### <span data-ttu-id="2e1aa-111">-Категория</span><span class="sxs-lookup"><span data-stu-id="2e1aa-111">-Category</span></span>
<span data-ttu-id="2e1aa-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="2e1aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1aa-113">-DefaultProfile</span></span>
<span data-ttu-id="2e1aa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2e1aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e1aa-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2e1aa-115">-DisplayName</span></span>
<span data-ttu-id="2e1aa-116">Задает отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="2e1aa-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="2e1aa-117">-ETag</span></span>
<span data-ttu-id="2e1aa-118">Указывает имя ETag.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="2e1aa-119">-Query</span><span class="sxs-lookup"><span data-stu-id="2e1aa-119">-Query</span></span>
<span data-ttu-id="2e1aa-120">Указывает имя запроса.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="2e1aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e1aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e1aa-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="2e1aa-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="2e1aa-123">-SavedSearchId</span></span>
<span data-ttu-id="2e1aa-124">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="2e1aa-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="2e1aa-125">-Tag</span></span>
<span data-ttu-id="2e1aa-126">Сохраненные теги поиска.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-126">The saved search tags.</span></span>

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

### <span data-ttu-id="2e1aa-127">-Version</span><span class="sxs-lookup"><span data-stu-id="2e1aa-127">-Version</span></span>
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

### <span data-ttu-id="2e1aa-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2e1aa-128">-WorkspaceName</span></span>
<span data-ttu-id="2e1aa-129">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2e1aa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1aa-130">CommonParameters</span></span>
<span data-ttu-id="2e1aa-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e1aa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1aa-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e1aa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1aa-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e1aa-133">INPUTS</span></span>

### <span data-ttu-id="2e1aa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2e1aa-134">System.String</span></span>

### <span data-ttu-id="2e1aa-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e1aa-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2e1aa-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="2e1aa-136">System.Int64</span></span>

## <span data-ttu-id="2e1aa-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e1aa-137">OUTPUTS</span></span>

### <span data-ttu-id="2e1aa-138">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="2e1aa-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="2e1aa-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e1aa-139">NOTES</span></span>

## <span data-ttu-id="2e1aa-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e1aa-140">RELATED LINKS</span></span>

[<span data-ttu-id="2e1aa-141">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="2e1aa-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


