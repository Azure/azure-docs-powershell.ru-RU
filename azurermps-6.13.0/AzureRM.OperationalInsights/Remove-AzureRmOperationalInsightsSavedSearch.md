---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a438a84a25e100539f485b5d3a7012f03ee355a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565809"
---
# <span data-ttu-id="3bcb4-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3bcb4-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="3bcb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bcb4-102">SYNOPSIS</span></span>
<span data-ttu-id="3bcb4-103">Удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bcb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bcb4-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bcb4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bcb4-105">DESCRIPTION</span></span>
<span data-ttu-id="3bcb4-106">Командлет **Remove-AzureRmOperationalInsightsSavedSearch** удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="3bcb4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bcb4-107">EXAMPLES</span></span>

### <span data-ttu-id="3bcb4-108">Пример 1: удаление сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="3bcb4-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="3bcb4-109">Эта команда удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="3bcb4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bcb4-110">PARAMETERS</span></span>

### <span data-ttu-id="3bcb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bcb4-111">-DefaultProfile</span></span>
<span data-ttu-id="3bcb4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3bcb4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bcb4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bcb4-113">-ResourceGroupName</span></span>
<span data-ttu-id="3bcb4-114">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="3bcb4-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="3bcb4-115">-SavedSearchId</span></span>
<span data-ttu-id="3bcb4-116">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="3bcb4-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3bcb4-117">-WorkspaceName</span></span>
<span data-ttu-id="3bcb4-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="3bcb4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bcb4-119">-Confirm</span></span>
<span data-ttu-id="3bcb4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bcb4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bcb4-121">-WhatIf</span></span>
<span data-ttu-id="3bcb4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bcb4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bcb4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bcb4-124">CommonParameters</span></span>
<span data-ttu-id="3bcb4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bcb4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bcb4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bcb4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bcb4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bcb4-127">INPUTS</span></span>

### <span data-ttu-id="3bcb4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3bcb4-128">System.String</span></span>

## <span data-ttu-id="3bcb4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bcb4-129">OUTPUTS</span></span>

### <span data-ttu-id="3bcb4-130">System. void</span><span class="sxs-lookup"><span data-stu-id="3bcb4-130">System.Void</span></span>

## <span data-ttu-id="3bcb4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bcb4-131">NOTES</span></span>

## <span data-ttu-id="3bcb4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bcb4-132">RELATED LINKS</span></span>

[<span data-ttu-id="3bcb4-133">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="3bcb4-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


