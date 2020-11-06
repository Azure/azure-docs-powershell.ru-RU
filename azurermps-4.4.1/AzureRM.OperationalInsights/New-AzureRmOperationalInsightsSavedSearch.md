---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a233e41ed91a40e8fb16ccda7ed640f8ad5239ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562320"
---
# <span data-ttu-id="a83a8-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a83a8-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="a83a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a83a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a83a8-103">Создание нового сохраненного поиска с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="a83a8-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a83a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a83a8-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a83a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a83a8-105">DESCRIPTION</span></span>
<span data-ttu-id="a83a8-106">Командлет **New-AzureRmOperationalInsightsSavedSearch** создает новый сохраненный поиск с заданными параметрами для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a83a8-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="a83a8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a83a8-107">EXAMPLES</span></span>

### <span data-ttu-id="a83a8-108">Пример 1: создание нового сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="a83a8-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="a83a8-109">Эта команда создает новый сохраненный поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="a83a8-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="a83a8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a83a8-110">PARAMETERS</span></span>

### <span data-ttu-id="a83a8-111">-Категория</span><span class="sxs-lookup"><span data-stu-id="a83a8-111">-Category</span></span>
<span data-ttu-id="a83a8-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="a83a8-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="a83a8-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a83a8-113">-DisplayName</span></span>
<span data-ttu-id="a83a8-114">Указывает имя сохраненного отображаемого поиска.</span><span class="sxs-lookup"><span data-stu-id="a83a8-114">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="a83a8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a83a8-115">-Force</span></span>
<span data-ttu-id="a83a8-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a83a8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a83a8-117">-Query</span><span class="sxs-lookup"><span data-stu-id="a83a8-117">-Query</span></span>
<span data-ttu-id="a83a8-118">Указывает имя запроса.</span><span class="sxs-lookup"><span data-stu-id="a83a8-118">Specifies the query name.</span></span>

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

### <span data-ttu-id="a83a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a83a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="a83a8-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a83a8-120">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="a83a8-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="a83a8-121">-SavedSearchId</span></span>
<span data-ttu-id="a83a8-122">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="a83a8-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="a83a8-123">-Теги</span><span class="sxs-lookup"><span data-stu-id="a83a8-123">-Tags</span></span>
<span data-ttu-id="a83a8-124">Указывает Теги ресурсов для сохраненного поиска.</span><span class="sxs-lookup"><span data-stu-id="a83a8-124">Specifies the resource tags for the saved search.</span></span>

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

### <span data-ttu-id="a83a8-125">-Version</span><span class="sxs-lookup"><span data-stu-id="a83a8-125">-Version</span></span>
<span data-ttu-id="a83a8-126">Указывает версию.</span><span class="sxs-lookup"><span data-stu-id="a83a8-126">Specifies the version.</span></span>

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

### <span data-ttu-id="a83a8-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a83a8-127">-WorkspaceName</span></span>
<span data-ttu-id="a83a8-128">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a83a8-128">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="a83a8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a83a8-129">-Confirm</span></span>
<span data-ttu-id="a83a8-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a83a8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a83a8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a83a8-131">-WhatIf</span></span>
<span data-ttu-id="a83a8-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a83a8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a83a8-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a83a8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a83a8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83a8-134">-DefaultProfile</span></span>
<span data-ttu-id="a83a8-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a83a8-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a83a8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83a8-136">CommonParameters</span></span>
<span data-ttu-id="a83a8-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a83a8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83a8-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a83a8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83a8-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a83a8-139">INPUTS</span></span>

## <span data-ttu-id="a83a8-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a83a8-140">OUTPUTS</span></span>

## <span data-ttu-id="a83a8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a83a8-141">NOTES</span></span>

## <span data-ttu-id="a83a8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a83a8-142">RELATED LINKS</span></span>

[<span data-ttu-id="a83a8-143">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="a83a8-143">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


