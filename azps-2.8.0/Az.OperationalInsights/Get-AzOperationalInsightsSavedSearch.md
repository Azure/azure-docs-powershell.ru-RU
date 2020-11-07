---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 6a330541d72dd2672eea829fdc5bdcc160f10606
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913114"
---
# <span data-ttu-id="7de99-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="7de99-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="7de99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7de99-102">SYNOPSIS</span></span>
<span data-ttu-id="7de99-103">Возвращает все сохраненные результаты поиска для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7de99-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="7de99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7de99-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7de99-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7de99-105">DESCRIPTION</span></span>
<span data-ttu-id="7de99-106">Командлет **Get-AzOperationalInsightsSavedSearch** возвращает все сохраненные результаты поиска для указанной рабочей области в указанной группе ресурсов, если не указать сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="7de99-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="7de99-107">Если вы укажете сохраненный идентификатор поиска, возвращается сохраненный поиск, соответствующий этому ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="7de99-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="7de99-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7de99-108">EXAMPLES</span></span>

### <span data-ttu-id="7de99-109">Пример 1: получение всех сохраненных поисков для рабочей области</span><span class="sxs-lookup"><span data-stu-id="7de99-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="7de99-110">Эта команда получает все сохраненные ресурсы, связанные с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="7de99-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="7de99-111">Пример 2: получение конкретного сохраненного поиска по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="7de99-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="7de99-112">Эта команда возвращает определенный сохраненный поиск по его ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="7de99-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="7de99-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7de99-113">PARAMETERS</span></span>

### <span data-ttu-id="7de99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de99-114">-DefaultProfile</span></span>
<span data-ttu-id="7de99-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7de99-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7de99-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de99-116">-ResourceGroupName</span></span>
<span data-ttu-id="7de99-117">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="7de99-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="7de99-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="7de99-118">-SavedSearchId</span></span>
<span data-ttu-id="7de99-119">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="7de99-119">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de99-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7de99-120">-WorkspaceName</span></span>
<span data-ttu-id="7de99-121">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7de99-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="7de99-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de99-122">CommonParameters</span></span>
<span data-ttu-id="7de99-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7de99-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de99-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de99-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de99-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7de99-125">INPUTS</span></span>

### <span data-ttu-id="7de99-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7de99-126">System.String</span></span>

## <span data-ttu-id="7de99-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7de99-127">OUTPUTS</span></span>

### <span data-ttu-id="7de99-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="7de99-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="7de99-129">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="7de99-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="7de99-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7de99-130">NOTES</span></span>

## <span data-ttu-id="7de99-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7de99-131">RELATED LINKS</span></span>

[<span data-ttu-id="7de99-132">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="7de99-132">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


