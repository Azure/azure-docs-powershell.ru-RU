---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
ms.openlocfilehash: 020a0684d6fe3a14b61b8582d8ad8427e68d8855
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077227"
---
# <span data-ttu-id="5ee78-101">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="5ee78-101">Get-AzOperationalInsightsSavedSearchResult</span></span>

## <span data-ttu-id="5ee78-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ee78-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee78-103">Возвращает результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="5ee78-103">Returns the results from a query.</span></span>

## <span data-ttu-id="5ee78-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ee78-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ee78-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ee78-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee78-106">Командлет **Get-AzOperationalInsightsSavedSearchResult** возвращает результаты запроса, указанного идентификатором поиска.</span><span class="sxs-lookup"><span data-stu-id="5ee78-106">The **Get-AzOperationalInsightsSavedSearchResult** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="5ee78-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ee78-107">EXAMPLES</span></span>

### <span data-ttu-id="5ee78-108">Пример 1: получение всех результатов поиска для сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="5ee78-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzOperationalInsightSavedSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="5ee78-109">Эта команда возвращает все результаты поиска для сохраненного поиска.</span><span class="sxs-lookup"><span data-stu-id="5ee78-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="5ee78-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ee78-110">PARAMETERS</span></span>

### <span data-ttu-id="5ee78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee78-111">-DefaultProfile</span></span>
<span data-ttu-id="5ee78-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ee78-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ee78-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee78-113">-ResourceGroupName</span></span>
<span data-ttu-id="5ee78-114">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="5ee78-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="5ee78-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="5ee78-115">-SavedSearchId</span></span>
<span data-ttu-id="5ee78-116">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="5ee78-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="5ee78-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ee78-117">-WorkspaceName</span></span>
<span data-ttu-id="5ee78-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5ee78-118">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="5ee78-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee78-119">CommonParameters</span></span>
<span data-ttu-id="5ee78-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ee78-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee78-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee78-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee78-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ee78-122">INPUTS</span></span>

### <span data-ttu-id="5ee78-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5ee78-123">System.String</span></span>

## <span data-ttu-id="5ee78-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ee78-124">OUTPUTS</span></span>

### <span data-ttu-id="5ee78-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="5ee78-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="5ee78-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ee78-126">NOTES</span></span>

## <span data-ttu-id="5ee78-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ee78-127">RELATED LINKS</span></span>

[<span data-ttu-id="5ee78-128">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="5ee78-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


