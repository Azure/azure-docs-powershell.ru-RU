---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: ebea93e7d59e0740aa21e909f35779857aacba01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559584"
---
# <span data-ttu-id="071ff-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="071ff-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="071ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="071ff-102">SYNOPSIS</span></span>
<span data-ttu-id="071ff-103">Обновление сохраненного поискового запроса, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="071ff-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="071ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="071ff-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="071ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="071ff-105">DESCRIPTION</span></span>
<span data-ttu-id="071ff-106">Командлет **Set-AzureRmOperationalInsightsSavedSearch** обновляет сохраненный поиск, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="071ff-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="071ff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="071ff-107">EXAMPLES</span></span>

### <span data-ttu-id="071ff-108">Пример 1: Установка сохраненного поиска с обновленными свойствами</span><span class="sxs-lookup"><span data-stu-id="071ff-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="071ff-109">Эта команда задает сохраненный поиск с обновленными свойствами.</span><span class="sxs-lookup"><span data-stu-id="071ff-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="071ff-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="071ff-110">PARAMETERS</span></span>

### <span data-ttu-id="071ff-111">-Категория</span><span class="sxs-lookup"><span data-stu-id="071ff-111">-Category</span></span>
<span data-ttu-id="071ff-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="071ff-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="071ff-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="071ff-113">-DisplayName</span></span>
<span data-ttu-id="071ff-114">Задает отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="071ff-114">Specifies the display name.</span></span>

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

### <span data-ttu-id="071ff-115">-ETag</span><span class="sxs-lookup"><span data-stu-id="071ff-115">-ETag</span></span>
<span data-ttu-id="071ff-116">Указывает имя ETag.</span><span class="sxs-lookup"><span data-stu-id="071ff-116">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="071ff-117">-Query</span><span class="sxs-lookup"><span data-stu-id="071ff-117">-Query</span></span>
<span data-ttu-id="071ff-118">Указывает имя запроса.</span><span class="sxs-lookup"><span data-stu-id="071ff-118">Specifies the query name.</span></span>

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

### <span data-ttu-id="071ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="071ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="071ff-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="071ff-120">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="071ff-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="071ff-121">-SavedSearchId</span></span>
<span data-ttu-id="071ff-122">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="071ff-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="071ff-123">-Теги</span><span class="sxs-lookup"><span data-stu-id="071ff-123">-Tags</span></span>
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

### <span data-ttu-id="071ff-124">-Version</span><span class="sxs-lookup"><span data-stu-id="071ff-124">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="071ff-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="071ff-125">-WorkspaceName</span></span>
<span data-ttu-id="071ff-126">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="071ff-126">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="071ff-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="071ff-127">-DefaultProfile</span></span>
<span data-ttu-id="071ff-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="071ff-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071ff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="071ff-129">CommonParameters</span></span>
<span data-ttu-id="071ff-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="071ff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="071ff-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="071ff-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="071ff-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="071ff-132">INPUTS</span></span>

## <span data-ttu-id="071ff-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="071ff-133">OUTPUTS</span></span>

## <span data-ttu-id="071ff-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="071ff-134">NOTES</span></span>

## <span data-ttu-id="071ff-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="071ff-135">RELATED LINKS</span></span>

[<span data-ttu-id="071ff-136">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="071ff-136">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


