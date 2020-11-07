---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7e93042ab376ff0020067a29f9b0642e0ab04de9
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913078"
---
# <span data-ttu-id="de0e4-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="de0e4-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="de0e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="de0e4-103">Создание нового сохраненного поиска с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="de0e4-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="de0e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de0e4-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de0e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de0e4-105">DESCRIPTION</span></span>
<span data-ttu-id="de0e4-106">Командлет **New-AzOperationalInsightsSavedSearch** создает новый сохраненный поиск с заданными параметрами для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="de0e4-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="de0e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de0e4-107">EXAMPLES</span></span>

### <span data-ttu-id="de0e4-108">Пример 1: создание нового сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="de0e4-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="de0e4-109">Эта команда создает новый сохраненный поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="de0e4-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="de0e4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de0e4-110">PARAMETERS</span></span>

### <span data-ttu-id="de0e4-111">-Категория</span><span class="sxs-lookup"><span data-stu-id="de0e4-111">-Category</span></span>
<span data-ttu-id="de0e4-112">Указывает имя категории.</span><span class="sxs-lookup"><span data-stu-id="de0e4-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="de0e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0e4-113">-DefaultProfile</span></span>
<span data-ttu-id="de0e4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="de0e4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de0e4-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="de0e4-115">-DisplayName</span></span>
<span data-ttu-id="de0e4-116">Указывает имя сохраненного отображаемого поиска.</span><span class="sxs-lookup"><span data-stu-id="de0e4-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="de0e4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="de0e4-117">-Force</span></span>
<span data-ttu-id="de0e4-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="de0e4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de0e4-119">-Query</span><span class="sxs-lookup"><span data-stu-id="de0e4-119">-Query</span></span>
<span data-ttu-id="de0e4-120">Указывает выражение запроса для сохраненного поиска.</span><span class="sxs-lookup"><span data-stu-id="de0e4-120">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="de0e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="de0e4-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de0e4-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="de0e4-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="de0e4-123">-SavedSearchId</span></span>
<span data-ttu-id="de0e4-124">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="de0e4-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="de0e4-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="de0e4-125">-Tag</span></span>
<span data-ttu-id="de0e4-126">Сохраненные теги поиска.</span><span class="sxs-lookup"><span data-stu-id="de0e4-126">The saved search tags.</span></span>

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

### <span data-ttu-id="de0e4-127">-Version</span><span class="sxs-lookup"><span data-stu-id="de0e4-127">-Version</span></span>
<span data-ttu-id="de0e4-128">Указывает версию.</span><span class="sxs-lookup"><span data-stu-id="de0e4-128">Specifies the version.</span></span>

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

### <span data-ttu-id="de0e4-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="de0e4-129">-WorkspaceName</span></span>
<span data-ttu-id="de0e4-130">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="de0e4-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="de0e4-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de0e4-131">-Confirm</span></span>
<span data-ttu-id="de0e4-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de0e4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de0e4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de0e4-133">-WhatIf</span></span>
<span data-ttu-id="de0e4-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de0e4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de0e4-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de0e4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de0e4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0e4-136">CommonParameters</span></span>
<span data-ttu-id="de0e4-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de0e4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0e4-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de0e4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0e4-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de0e4-139">INPUTS</span></span>

### <span data-ttu-id="de0e4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="de0e4-140">System.String</span></span>

### <span data-ttu-id="de0e4-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="de0e4-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="de0e4-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="de0e4-142">System.Int64</span></span>

## <span data-ttu-id="de0e4-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de0e4-143">OUTPUTS</span></span>

### <span data-ttu-id="de0e4-144">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="de0e4-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="de0e4-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="de0e4-145">NOTES</span></span>

## <span data-ttu-id="de0e4-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de0e4-146">RELATED LINKS</span></span>

[<span data-ttu-id="de0e4-147">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="de0e4-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


