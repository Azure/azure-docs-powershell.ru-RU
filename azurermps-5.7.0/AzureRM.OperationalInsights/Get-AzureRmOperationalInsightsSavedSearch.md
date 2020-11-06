---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7022c7b2fcc9fb0f11ded4034a0c78c4faa65237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561648"
---
# <span data-ttu-id="e25a8-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="e25a8-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="e25a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e25a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e25a8-103">Возвращает все сохраненные результаты поиска для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e25a8-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e25a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e25a8-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e25a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e25a8-105">DESCRIPTION</span></span>
<span data-ttu-id="e25a8-106">Командлет **Get-AzureRmOperationalInsightsSavedSearch** возвращает все сохраненные результаты поиска для указанной рабочей области в указанной группе ресурсов, если не указать сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="e25a8-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="e25a8-107">Если вы укажете сохраненный идентификатор поиска, возвращается сохраненный поиск, соответствующий этому ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="e25a8-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="e25a8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e25a8-108">EXAMPLES</span></span>

### <span data-ttu-id="e25a8-109">Пример 1: получение всех сохраненных поисков для рабочей области</span><span class="sxs-lookup"><span data-stu-id="e25a8-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="e25a8-110">Эта команда получает все сохраненные ресурсы, связанные с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="e25a8-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="e25a8-111">Пример 2: получение конкретного сохраненного поиска по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="e25a8-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="e25a8-112">Эта команда возвращает определенный сохраненный поиск по его ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="e25a8-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="e25a8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e25a8-113">PARAMETERS</span></span>

### <span data-ttu-id="e25a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25a8-114">-DefaultProfile</span></span>
<span data-ttu-id="e25a8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e25a8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e25a8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25a8-116">-ResourceGroupName</span></span>
<span data-ttu-id="e25a8-117">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="e25a8-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="e25a8-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="e25a8-118">-SavedSearchId</span></span>
<span data-ttu-id="e25a8-119">Указывает сохраненный идентификатор поиска.</span><span class="sxs-lookup"><span data-stu-id="e25a8-119">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e25a8-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e25a8-120">-WorkspaceName</span></span>
<span data-ttu-id="e25a8-121">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e25a8-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="e25a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25a8-122">CommonParameters</span></span>
<span data-ttu-id="e25a8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e25a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25a8-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25a8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25a8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e25a8-125">INPUTS</span></span>

### <span data-ttu-id="e25a8-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="e25a8-126">None</span></span>
<span data-ttu-id="e25a8-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e25a8-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e25a8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e25a8-128">OUTPUTS</span></span>

### <span data-ttu-id="e25a8-129">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="e25a8-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="e25a8-130">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="e25a8-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="e25a8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e25a8-131">NOTES</span></span>

## <span data-ttu-id="e25a8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e25a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="e25a8-133">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="e25a8-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


