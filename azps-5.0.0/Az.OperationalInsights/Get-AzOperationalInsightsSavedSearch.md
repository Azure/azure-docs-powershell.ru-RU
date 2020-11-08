---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246882"
---
# <span data-ttu-id="e7cc1-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="e7cc1-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="e7cc1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="e7cc1-103">Возвращает все сохраненные результаты поиска для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e7cc1-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="e7cc1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7cc1-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7cc1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="e7cc1-106">Командлет **Get-AzOperationalInsightsSavedSearch** возвращает все сохраненные результаты поиска для указанной рабочей области в указанной группе ресурсов, если не указать сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="e7cc1-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="e7cc1-107">Если вы укажете сохраненный идентификатор поиска, возвращается сохраненный поиск, соответствующий этому ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="e7cc1-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="e7cc1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7cc1-108">EXAMPLES</span></span>

### <span data-ttu-id="e7cc1-109">Пример 1: получение всех сохраненных поисков для рабочей области</span><span class="sxs-lookup"><span data-stu-id="e7cc1-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="e7cc1-110">Эта команда получает все сохраненные ресурсы, связанные с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="e7cc1-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="e7cc1-111">Пример 2: получение конкретного сохраненного поиска по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="e7cc1-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="e7cc1-112">Эта команда возвращает определенный сохраненный поиск по его ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="e7cc1-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="e7cc1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7cc1-113">PARAMETERS</span></span>

### <span data-ttu-id="e7cc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7cc1-114">-DefaultProfile</span></span>
<span data-ttu-id="e7cc1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e7cc1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7cc1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7cc1-116">-ResourceGroupName</span></span>
<span data-ttu-id="e7cc1-117">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="e7cc1-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="e7cc1-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="e7cc1-118">-SavedSearchId</span></span>
<span data-ttu-id="e7cc1-119">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="e7cc1-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="e7cc1-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e7cc1-120">-WorkspaceName</span></span>
<span data-ttu-id="e7cc1-121">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e7cc1-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="e7cc1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7cc1-122">CommonParameters</span></span>
<span data-ttu-id="e7cc1-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7cc1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7cc1-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7cc1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7cc1-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7cc1-125">INPUTS</span></span>

### <span data-ttu-id="e7cc1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e7cc1-126">System.String</span></span>

## <span data-ttu-id="e7cc1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7cc1-127">OUTPUTS</span></span>

### <span data-ttu-id="e7cc1-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="e7cc1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="e7cc1-129">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="e7cc1-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="e7cc1-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7cc1-130">NOTES</span></span>

## <span data-ttu-id="e7cc1-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7cc1-131">RELATED LINKS</span></span>

[<span data-ttu-id="e7cc1-132">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="e7cc1-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


