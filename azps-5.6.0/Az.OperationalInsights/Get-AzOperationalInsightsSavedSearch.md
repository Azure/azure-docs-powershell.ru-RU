---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: fe0d1e13b276f3282feaef2cf4eb5a9c687bb3b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958099"
---
# <span data-ttu-id="9e946-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="9e946-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="9e946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e946-102">SYNOPSIS</span></span>
<span data-ttu-id="9e946-103">Возвращает все сохраненные поисковые запросы для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9e946-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="9e946-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e946-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e946-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e946-105">DESCRIPTION</span></span>
<span data-ttu-id="9e946-106">При **этом** все сохраненные поисковые запросы для определенной рабочей области в группе ресурсов, заданной без указания сохраненного ИД поиска, возвращаются с его рабочая область.</span><span class="sxs-lookup"><span data-stu-id="9e946-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="9e946-107">Если указать сохраненный ИД поиска, будет возвращен сохраненный поиск, соответствующий ему.</span><span class="sxs-lookup"><span data-stu-id="9e946-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="9e946-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e946-108">EXAMPLES</span></span>

### <span data-ttu-id="9e946-109">Пример 1. Все сохраненные поисковые запросы для рабочей области</span><span class="sxs-lookup"><span data-stu-id="9e946-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="9e946-110">Эта команда возвращает все сохраненные ресурсы, связанные с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="9e946-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="9e946-111">Пример 2. Получить определенный сохраненный поиск по ИД</span><span class="sxs-lookup"><span data-stu-id="9e946-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="9e946-112">Эта команда получает определенный сохраненный поиск по его ИД.</span><span class="sxs-lookup"><span data-stu-id="9e946-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="9e946-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e946-113">PARAMETERS</span></span>

### <span data-ttu-id="9e946-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e946-114">-DefaultProfile</span></span>
<span data-ttu-id="9e946-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9e946-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e946-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e946-116">-ResourceGroupName</span></span>
<span data-ttu-id="9e946-117">Указывает имя группы ресурсов Azure, которая содержит рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="9e946-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="9e946-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="9e946-118">-SavedSearchId</span></span>
<span data-ttu-id="9e946-119">Определяет сохраненный ИД поиска.</span><span class="sxs-lookup"><span data-stu-id="9e946-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="9e946-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e946-120">-WorkspaceName</span></span>
<span data-ttu-id="9e946-121">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9e946-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="9e946-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e946-122">CommonParameters</span></span>
<span data-ttu-id="9e946-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e946-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e946-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e946-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e946-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e946-125">INPUTS</span></span>

### <span data-ttu-id="9e946-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9e946-126">System.String</span></span>

## <span data-ttu-id="9e946-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e946-127">OUTPUTS</span></span>

### <span data-ttu-id="9e946-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="9e946-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="9e946-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="9e946-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="9e946-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e946-130">NOTES</span></span>

## <span data-ttu-id="9e946-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e946-131">RELATED LINKS</span></span>

[<span data-ttu-id="9e946-132">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9e946-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


