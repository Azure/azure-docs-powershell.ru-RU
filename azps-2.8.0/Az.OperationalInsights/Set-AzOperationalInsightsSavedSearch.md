---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 535fbe737184b996ee0caa030c83137ea8cd1019
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913195"
---
# <span data-ttu-id="1ad38-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="1ad38-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="1ad38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ad38-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad38-103">Обновление сохраненного поискового запроса, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="1ad38-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="1ad38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ad38-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ad38-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ad38-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad38-106">Командлет **Set-AzOperationalInsightsSavedSearch** обновляет сохраненный поиск, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="1ad38-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="1ad38-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ad38-107">EXAMPLES</span></span>

### <span data-ttu-id="1ad38-108">Пример 1: Установка сохраненного поиска с обновленными свойствами</span><span class="sxs-lookup"><span data-stu-id="1ad38-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="1ad38-109">Эта команда задает сохраненный поиск с обновленными свойствами.</span><span class="sxs-lookup"><span data-stu-id="1ad38-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="1ad38-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ad38-110">PARAMETERS</span></span>

### <span data-ttu-id="1ad38-111">-Категория</span><span class="sxs-lookup"><span data-stu-id="1ad38-111">-Category</span></span>
<span data-ttu-id="1ad38-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="1ad38-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="1ad38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad38-113">-DefaultProfile</span></span>
<span data-ttu-id="1ad38-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1ad38-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ad38-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1ad38-115">-DisplayName</span></span>
<span data-ttu-id="1ad38-116">Задает отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="1ad38-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="1ad38-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="1ad38-117">-ETag</span></span>
<span data-ttu-id="1ad38-118">Указывает имя ETag.</span><span class="sxs-lookup"><span data-stu-id="1ad38-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="1ad38-119">-Query</span><span class="sxs-lookup"><span data-stu-id="1ad38-119">-Query</span></span>
<span data-ttu-id="1ad38-120">Указывает имя запроса.</span><span class="sxs-lookup"><span data-stu-id="1ad38-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="1ad38-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad38-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ad38-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ad38-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="1ad38-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="1ad38-123">-SavedSearchId</span></span>
<span data-ttu-id="1ad38-124">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="1ad38-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="1ad38-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="1ad38-125">-Tag</span></span>
<span data-ttu-id="1ad38-126">Сохраненные теги поиска.</span><span class="sxs-lookup"><span data-stu-id="1ad38-126">The saved search tags.</span></span>

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

### <span data-ttu-id="1ad38-127">-Version</span><span class="sxs-lookup"><span data-stu-id="1ad38-127">-Version</span></span>
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

### <span data-ttu-id="1ad38-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1ad38-128">-WorkspaceName</span></span>
<span data-ttu-id="1ad38-129">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1ad38-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="1ad38-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad38-130">CommonParameters</span></span>
<span data-ttu-id="1ad38-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ad38-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad38-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad38-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad38-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ad38-133">INPUTS</span></span>

### <span data-ttu-id="1ad38-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1ad38-134">System.String</span></span>

### <span data-ttu-id="1ad38-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ad38-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1ad38-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="1ad38-136">System.Int64</span></span>

## <span data-ttu-id="1ad38-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ad38-137">OUTPUTS</span></span>

### <span data-ttu-id="1ad38-138">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="1ad38-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="1ad38-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ad38-139">NOTES</span></span>

## <span data-ttu-id="1ad38-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ad38-140">RELATED LINKS</span></span>

[<span data-ttu-id="1ad38-141">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="1ad38-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


