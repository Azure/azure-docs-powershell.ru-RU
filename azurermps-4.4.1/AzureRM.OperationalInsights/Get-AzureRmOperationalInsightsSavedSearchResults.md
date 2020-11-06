---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 88adac87543c0a51542cc0f79f2f1eb10ca8184b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567551"
---
# <span data-ttu-id="bd649-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="bd649-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="bd649-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd649-102">SYNOPSIS</span></span>
<span data-ttu-id="bd649-103">Возвращает результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="bd649-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd649-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd649-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd649-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd649-105">DESCRIPTION</span></span>
<span data-ttu-id="bd649-106">Командлет **Get-AzureRmOperationalInsightsSavedSearchResults** возвращает результаты запроса, указанного идентификатором поиска.</span><span class="sxs-lookup"><span data-stu-id="bd649-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="bd649-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd649-107">EXAMPLES</span></span>

### <span data-ttu-id="bd649-108">Пример 1: получение всех результатов поиска для сохраненного поиска</span><span class="sxs-lookup"><span data-stu-id="bd649-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="bd649-109">Эта команда возвращает все результаты поиска для сохраненного поиска.</span><span class="sxs-lookup"><span data-stu-id="bd649-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="bd649-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd649-110">PARAMETERS</span></span>

### <span data-ttu-id="bd649-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd649-111">-ResourceGroupName</span></span>
<span data-ttu-id="bd649-112">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="bd649-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="bd649-113">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="bd649-113">-SavedSearchId</span></span>
<span data-ttu-id="bd649-114">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="bd649-114">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="bd649-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bd649-115">-WorkspaceName</span></span>
<span data-ttu-id="bd649-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="bd649-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="bd649-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd649-117">-DefaultProfile</span></span>
<span data-ttu-id="bd649-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd649-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd649-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd649-119">CommonParameters</span></span>
<span data-ttu-id="bd649-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd649-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd649-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd649-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd649-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd649-122">INPUTS</span></span>

## <span data-ttu-id="bd649-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd649-123">OUTPUTS</span></span>

### <span data-ttu-id="bd649-124">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="bd649-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="bd649-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd649-125">NOTES</span></span>

## <span data-ttu-id="bd649-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd649-126">RELATED LINKS</span></span>

[<span data-ttu-id="bd649-127">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="bd649-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


