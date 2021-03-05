---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 02dded0f03b1ba7bd0936e364b229864e0955022
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989775"
---
# <span data-ttu-id="ebab1-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="ebab1-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="ebab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebab1-102">SYNOPSIS</span></span>
<span data-ttu-id="ebab1-103">Удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ebab1-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="ebab1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ebab1-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebab1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebab1-105">DESCRIPTION</span></span>
<span data-ttu-id="ebab1-106">Cmdlet **Remove-AzOperationalInsightsSavedSearch** удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ebab1-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="ebab1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ebab1-107">EXAMPLES</span></span>

### <span data-ttu-id="ebab1-108">Пример 1. Удаление сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="ebab1-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="ebab1-109">Эта команда удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ebab1-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="ebab1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebab1-110">PARAMETERS</span></span>

### <span data-ttu-id="ebab1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebab1-111">-DefaultProfile</span></span>
<span data-ttu-id="ebab1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ebab1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebab1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebab1-113">-ResourceGroupName</span></span>
<span data-ttu-id="ebab1-114">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ebab1-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ebab1-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ebab1-115">-SavedSearchId</span></span>
<span data-ttu-id="ebab1-116">Определяет сохраненный ИД поиска.</span><span class="sxs-lookup"><span data-stu-id="ebab1-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="ebab1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ebab1-117">-WorkspaceName</span></span>
<span data-ttu-id="ebab1-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ebab1-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ebab1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebab1-119">-Confirm</span></span>
<span data-ttu-id="ebab1-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ebab1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebab1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebab1-121">-WhatIf</span></span>
<span data-ttu-id="ebab1-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebab1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebab1-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ebab1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebab1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebab1-124">CommonParameters</span></span>
<span data-ttu-id="ebab1-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebab1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebab1-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebab1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebab1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebab1-127">INPUTS</span></span>

### <span data-ttu-id="ebab1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ebab1-128">System.String</span></span>

## <span data-ttu-id="ebab1-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ebab1-129">OUTPUTS</span></span>

### <span data-ttu-id="ebab1-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="ebab1-130">System.Void</span></span>

## <span data-ttu-id="ebab1-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ebab1-131">NOTES</span></span>

## <span data-ttu-id="ebab1-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebab1-132">RELATED LINKS</span></span>

[<span data-ttu-id="ebab1-133">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ebab1-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


