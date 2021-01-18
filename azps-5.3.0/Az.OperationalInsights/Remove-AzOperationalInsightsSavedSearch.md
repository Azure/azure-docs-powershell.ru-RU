---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519803"
---
# <span data-ttu-id="e039f-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="e039f-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="e039f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e039f-102">SYNOPSIS</span></span>
<span data-ttu-id="e039f-103">Удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e039f-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="e039f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e039f-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e039f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e039f-105">DESCRIPTION</span></span>
<span data-ttu-id="e039f-106">Cmdlet **Remove-AzOperationalInsightsSavedSearch** удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e039f-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="e039f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e039f-107">EXAMPLES</span></span>

### <span data-ttu-id="e039f-108">Пример 1. Удаление сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="e039f-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="e039f-109">Эта команда удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e039f-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="e039f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e039f-110">PARAMETERS</span></span>

### <span data-ttu-id="e039f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e039f-111">-DefaultProfile</span></span>
<span data-ttu-id="e039f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e039f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e039f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e039f-113">-ResourceGroupName</span></span>
<span data-ttu-id="e039f-114">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e039f-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e039f-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="e039f-115">-SavedSearchId</span></span>
<span data-ttu-id="e039f-116">Определяет сохраненный ИД поиска.</span><span class="sxs-lookup"><span data-stu-id="e039f-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="e039f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e039f-117">-WorkspaceName</span></span>
<span data-ttu-id="e039f-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e039f-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e039f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e039f-119">-Confirm</span></span>
<span data-ttu-id="e039f-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e039f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e039f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e039f-121">-WhatIf</span></span>
<span data-ttu-id="e039f-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e039f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e039f-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e039f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e039f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e039f-124">CommonParameters</span></span>
<span data-ttu-id="e039f-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e039f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e039f-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e039f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e039f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e039f-127">INPUTS</span></span>

### <span data-ttu-id="e039f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e039f-128">System.String</span></span>

## <span data-ttu-id="e039f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e039f-129">OUTPUTS</span></span>

### <span data-ttu-id="e039f-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="e039f-130">System.Void</span></span>

## <span data-ttu-id="e039f-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e039f-131">NOTES</span></span>

## <span data-ttu-id="e039f-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e039f-132">RELATED LINKS</span></span>

[<span data-ttu-id="e039f-133">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e039f-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


