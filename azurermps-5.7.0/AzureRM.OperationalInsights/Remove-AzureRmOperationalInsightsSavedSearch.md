---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: e66ca332d2fd59faa64e4360d00af714cfa28475
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557304"
---
# <span data-ttu-id="11c0d-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="11c0d-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="11c0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="11c0d-103">Удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="11c0d-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11c0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11c0d-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c0d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="11c0d-106">Командлет **Remove-AzureRmOperationalInsightsSavedSearch** удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="11c0d-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="11c0d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11c0d-107">EXAMPLES</span></span>

### <span data-ttu-id="11c0d-108">Пример 1: удаление сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="11c0d-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="11c0d-109">Эта команда удаляет сохраненный поиск из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="11c0d-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="11c0d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11c0d-110">PARAMETERS</span></span>

### <span data-ttu-id="11c0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c0d-111">-DefaultProfile</span></span>
<span data-ttu-id="11c0d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="11c0d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11c0d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c0d-113">-ResourceGroupName</span></span>
<span data-ttu-id="11c0d-114">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="11c0d-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="11c0d-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="11c0d-115">-SavedSearchId</span></span>
<span data-ttu-id="11c0d-116">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="11c0d-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="11c0d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11c0d-117">-WorkspaceName</span></span>
<span data-ttu-id="11c0d-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="11c0d-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="11c0d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11c0d-119">-Confirm</span></span>
<span data-ttu-id="11c0d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11c0d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c0d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c0d-121">-WhatIf</span></span>
<span data-ttu-id="11c0d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11c0d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11c0d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11c0d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c0d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c0d-124">CommonParameters</span></span>
<span data-ttu-id="11c0d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11c0d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c0d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11c0d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c0d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11c0d-127">INPUTS</span></span>

### <span data-ttu-id="11c0d-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="11c0d-128">None</span></span>
<span data-ttu-id="11c0d-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="11c0d-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11c0d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11c0d-130">OUTPUTS</span></span>

## <span data-ttu-id="11c0d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="11c0d-131">NOTES</span></span>

## <span data-ttu-id="11c0d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11c0d-132">RELATED LINKS</span></span>

[<span data-ttu-id="11c0d-133">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="11c0d-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


