---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506832"
---
# <span data-ttu-id="13efa-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="13efa-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="13efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13efa-102">SYNOPSIS</span></span>
<span data-ttu-id="13efa-103">Возвращает все сохраненные поисковые запросы для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="13efa-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="13efa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="13efa-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13efa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13efa-105">DESCRIPTION</span></span>
<span data-ttu-id="13efa-106">При **этом** все сохраненные поисковые запросы для определенной рабочей области в группе ресурсов, заданной без указания сохраненного ИД поиска, возвращаются с его рабочая область.</span><span class="sxs-lookup"><span data-stu-id="13efa-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="13efa-107">Если указать сохраненный ИД поиска, будет возвращен сохраненный поиск, соответствующий ему.</span><span class="sxs-lookup"><span data-stu-id="13efa-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="13efa-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="13efa-108">EXAMPLES</span></span>

### <span data-ttu-id="13efa-109">Пример 1. Все сохраненные поисковые запросы для рабочей области</span><span class="sxs-lookup"><span data-stu-id="13efa-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="13efa-110">Эта команда возвращает все сохраненные ресурсы, связанные с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="13efa-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="13efa-111">Пример 2. Получить определенный сохраненный поиск по ИД</span><span class="sxs-lookup"><span data-stu-id="13efa-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="13efa-112">Эта команда получает определенный сохраненный поиск по его ИД.</span><span class="sxs-lookup"><span data-stu-id="13efa-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="13efa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13efa-113">PARAMETERS</span></span>

### <span data-ttu-id="13efa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13efa-114">-DefaultProfile</span></span>
<span data-ttu-id="13efa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="13efa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13efa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13efa-116">-ResourceGroupName</span></span>
<span data-ttu-id="13efa-117">Имя группы ресурсов Azure, которая содержит рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="13efa-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="13efa-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="13efa-118">-SavedSearchId</span></span>
<span data-ttu-id="13efa-119">Определяет сохраненный ИД поиска.</span><span class="sxs-lookup"><span data-stu-id="13efa-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="13efa-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="13efa-120">-WorkspaceName</span></span>
<span data-ttu-id="13efa-121">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="13efa-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="13efa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13efa-122">CommonParameters</span></span>
<span data-ttu-id="13efa-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13efa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13efa-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13efa-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13efa-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13efa-125">INPUTS</span></span>

### <span data-ttu-id="13efa-126">System.String</span><span class="sxs-lookup"><span data-stu-id="13efa-126">System.String</span></span>

## <span data-ttu-id="13efa-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="13efa-127">OUTPUTS</span></span>

### <span data-ttu-id="13efa-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="13efa-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="13efa-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="13efa-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="13efa-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="13efa-130">NOTES</span></span>

## <span data-ttu-id="13efa-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13efa-131">RELATED LINKS</span></span>

[<span data-ttu-id="13efa-132">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="13efa-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


