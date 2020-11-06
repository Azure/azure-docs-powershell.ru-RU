---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 202fafead72ec57f3f03460093791943d36a2ba3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556576"
---
# <span data-ttu-id="1f15a-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="1f15a-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="1f15a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f15a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f15a-103">Возвращает результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="1f15a-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f15a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f15a-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f15a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f15a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f15a-106">Командлет **Get-AzureRmOperationalInsightsSavedSearchResults** возвращает результаты запроса, указанного идентификатором поиска.</span><span class="sxs-lookup"><span data-stu-id="1f15a-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="1f15a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f15a-107">EXAMPLES</span></span>

### <span data-ttu-id="1f15a-108">Пример 1: получение всех результатов поиска для сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="1f15a-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="1f15a-109">Эта команда возвращает все результаты поиска для сохраненного поиска.</span><span class="sxs-lookup"><span data-stu-id="1f15a-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="1f15a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f15a-110">PARAMETERS</span></span>

### <span data-ttu-id="1f15a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f15a-111">-DefaultProfile</span></span>
<span data-ttu-id="1f15a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f15a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f15a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f15a-113">-ResourceGroupName</span></span>
<span data-ttu-id="1f15a-114">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="1f15a-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="1f15a-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="1f15a-115">-SavedSearchId</span></span>
<span data-ttu-id="1f15a-116">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="1f15a-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="1f15a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1f15a-117">-WorkspaceName</span></span>
<span data-ttu-id="1f15a-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1f15a-118">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="1f15a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f15a-119">CommonParameters</span></span>
<span data-ttu-id="1f15a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f15a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f15a-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f15a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f15a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f15a-122">INPUTS</span></span>

### <span data-ttu-id="1f15a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1f15a-123">System.String</span></span>

## <span data-ttu-id="1f15a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f15a-124">OUTPUTS</span></span>

### <span data-ttu-id="1f15a-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="1f15a-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="1f15a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f15a-126">NOTES</span></span>

## <span data-ttu-id="1f15a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f15a-127">RELATED LINKS</span></span>

[<span data-ttu-id="1f15a-128">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="1f15a-128">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


