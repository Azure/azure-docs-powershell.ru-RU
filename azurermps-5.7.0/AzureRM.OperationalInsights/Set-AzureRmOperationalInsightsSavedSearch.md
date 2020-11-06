---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: fdfe52151346bbf173226213c9450484d49fe040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560212"
---
# <span data-ttu-id="ffd3c-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="ffd3c-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="ffd3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd3c-103">Обновление сохраненного поискового запроса, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffd3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffd3c-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffd3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffd3c-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd3c-106">Командлет **Set-AzureRmOperationalInsightsSavedSearch** обновляет сохраненный поиск, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="ffd3c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffd3c-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd3c-108">Пример 1: Установка сохраненного поиска с обновленными свойствами</span><span class="sxs-lookup"><span data-stu-id="ffd3c-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="ffd3c-109">Эта команда задает сохраненный поиск с обновленными свойствами.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="ffd3c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffd3c-110">PARAMETERS</span></span>

### <span data-ttu-id="ffd3c-111">-Категория</span><span class="sxs-lookup"><span data-stu-id="ffd3c-111">-Category</span></span>
<span data-ttu-id="ffd3c-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-112">Specifies the category name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd3c-113">-DefaultProfile</span></span>
<span data-ttu-id="ffd3c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ffd3c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ffd3c-115">-DisplayName</span></span>
<span data-ttu-id="ffd3c-116">Задает отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-116">Specifies the display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="ffd3c-117">-ETag</span></span>
<span data-ttu-id="ffd3c-118">Указывает имя ETag.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-118">Specifies the ETag name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-119">-Query</span><span class="sxs-lookup"><span data-stu-id="ffd3c-119">-Query</span></span>
<span data-ttu-id="ffd3c-120">Указывает имя запроса.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-120">Specifies the query name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="ffd3c-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-122">Specifies the resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ffd3c-123">-SavedSearchId</span></span>
<span data-ttu-id="ffd3c-124">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-124">Specifies the saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="ffd3c-125">-Tag</span></span>
<span data-ttu-id="ffd3c-126">Сохраненные теги поиска.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-126">The saved search tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-127">-Version</span><span class="sxs-lookup"><span data-stu-id="ffd3c-127">-Version</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ffd3c-128">-WorkspaceName</span></span>
<span data-ttu-id="ffd3c-129">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-129">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd3c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd3c-130">CommonParameters</span></span>
<span data-ttu-id="ffd3c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd3c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd3c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd3c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffd3c-133">INPUTS</span></span>

### <span data-ttu-id="ffd3c-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="ffd3c-134">None</span></span>
<span data-ttu-id="ffd3c-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ffd3c-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ffd3c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffd3c-136">OUTPUTS</span></span>

## <span data-ttu-id="ffd3c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffd3c-137">NOTES</span></span>

## <span data-ttu-id="ffd3c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffd3c-138">RELATED LINKS</span></span>

[<span data-ttu-id="ffd3c-139">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="ffd3c-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


