---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 9b43e0aab99db7be236a6ffae32997f37de40807
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077228"
---
# <span data-ttu-id="8a0be-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="8a0be-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="8a0be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a0be-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0be-103">Возвращает все сохраненные результаты поиска для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8a0be-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="8a0be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a0be-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a0be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a0be-105">DESCRIPTION</span></span>
<span data-ttu-id="8a0be-106">Командлет **Get-AzOperationalInsightsSavedSearch** возвращает все сохраненные результаты поиска для указанной рабочей области в указанной группе ресурсов, если не указать сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="8a0be-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="8a0be-107">Если вы укажете сохраненный идентификатор поиска, возвращается сохраненный поиск, соответствующий этому ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="8a0be-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="8a0be-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a0be-108">EXAMPLES</span></span>

### <span data-ttu-id="8a0be-109">Пример 1: получение всех сохраненных поисков для рабочей области</span><span class="sxs-lookup"><span data-stu-id="8a0be-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="8a0be-110">Эта команда получает все сохраненные ресурсы, связанные с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="8a0be-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="8a0be-111">Пример 2: получение конкретного сохраненного поиска по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="8a0be-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="8a0be-112">Эта команда возвращает определенный сохраненный поиск по его ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="8a0be-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="8a0be-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a0be-113">PARAMETERS</span></span>

### <span data-ttu-id="8a0be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a0be-114">-DefaultProfile</span></span>
<span data-ttu-id="8a0be-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8a0be-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a0be-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0be-116">-ResourceGroupName</span></span>
<span data-ttu-id="8a0be-117">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="8a0be-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="8a0be-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="8a0be-118">-SavedSearchId</span></span>
<span data-ttu-id="8a0be-119">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="8a0be-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="8a0be-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8a0be-120">-WorkspaceName</span></span>
<span data-ttu-id="8a0be-121">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8a0be-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="8a0be-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0be-122">CommonParameters</span></span>
<span data-ttu-id="8a0be-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a0be-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0be-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a0be-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0be-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a0be-125">INPUTS</span></span>

### <span data-ttu-id="8a0be-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8a0be-126">System.String</span></span>

## <span data-ttu-id="8a0be-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a0be-127">OUTPUTS</span></span>

### <span data-ttu-id="8a0be-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="8a0be-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="8a0be-129">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="8a0be-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="8a0be-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a0be-130">NOTES</span></span>

## <span data-ttu-id="8a0be-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a0be-131">RELATED LINKS</span></span>

[<span data-ttu-id="8a0be-132">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="8a0be-132">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


