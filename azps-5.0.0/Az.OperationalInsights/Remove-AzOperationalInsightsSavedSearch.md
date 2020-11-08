---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246881"
---
# <span data-ttu-id="c1202-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="c1202-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="c1202-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1202-102">SYNOPSIS</span></span>
<span data-ttu-id="c1202-103">Удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c1202-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="c1202-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1202-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1202-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1202-105">DESCRIPTION</span></span>
<span data-ttu-id="c1202-106">Командлет **Remove-AzOperationalInsightsSavedSearch** удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c1202-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="c1202-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1202-107">EXAMPLES</span></span>

### <span data-ttu-id="c1202-108">Пример 1: удаление сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="c1202-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="c1202-109">Эта команда удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c1202-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="c1202-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1202-110">PARAMETERS</span></span>

### <span data-ttu-id="c1202-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1202-111">-DefaultProfile</span></span>
<span data-ttu-id="c1202-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c1202-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1202-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1202-113">-ResourceGroupName</span></span>
<span data-ttu-id="c1202-114">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c1202-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="c1202-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c1202-115">-SavedSearchId</span></span>
<span data-ttu-id="c1202-116">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="c1202-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="c1202-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c1202-117">-WorkspaceName</span></span>
<span data-ttu-id="c1202-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c1202-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="c1202-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1202-119">-Confirm</span></span>
<span data-ttu-id="c1202-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1202-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1202-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1202-121">-WhatIf</span></span>
<span data-ttu-id="c1202-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1202-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1202-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1202-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1202-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1202-124">CommonParameters</span></span>
<span data-ttu-id="c1202-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1202-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1202-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1202-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1202-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1202-127">INPUTS</span></span>

### <span data-ttu-id="c1202-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c1202-128">System.String</span></span>

## <span data-ttu-id="c1202-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1202-129">OUTPUTS</span></span>

### <span data-ttu-id="c1202-130">System. void</span><span class="sxs-lookup"><span data-stu-id="c1202-130">System.Void</span></span>

## <span data-ttu-id="c1202-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1202-131">NOTES</span></span>

## <span data-ttu-id="c1202-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1202-132">RELATED LINKS</span></span>

[<span data-ttu-id="c1202-133">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="c1202-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


