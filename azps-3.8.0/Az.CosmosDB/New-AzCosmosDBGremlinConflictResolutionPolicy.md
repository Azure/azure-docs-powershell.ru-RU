---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066556"
---
# <span data-ttu-id="d6477-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6477-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="d6477-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6477-102">SYNOPSIS</span></span>
<span data-ttu-id="d6477-103">Создает новый объект типа PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d6477-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="d6477-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="d6477-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="d6477-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6477-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6477-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6477-106">DESCRIPTION</span></span>
<span data-ttu-id="d6477-107">Объект, соответствующий ConflictResolutionPolicy API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d6477-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="d6477-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6477-108">EXAMPLES</span></span>

### <span data-ttu-id="d6477-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6477-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="d6477-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6477-110">PARAMETERS</span></span>

### <span data-ttu-id="d6477-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="d6477-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="d6477-112">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="d6477-112">To be provided when the type is custom.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6477-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6477-113">-DefaultProfile</span></span>
<span data-ttu-id="d6477-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6477-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6477-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d6477-115">-Path</span></span>
<span data-ttu-id="d6477-116">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="d6477-116">To be provided when the type is LastWriterWins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6477-117">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="d6477-117">-Type</span></span>
<span data-ttu-id="d6477-118">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="d6477-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6477-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6477-119">CommonParameters</span></span>
<span data-ttu-id="d6477-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6477-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6477-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6477-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6477-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6477-122">INPUTS</span></span>

### <span data-ttu-id="d6477-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="d6477-123">None</span></span>

## <span data-ttu-id="d6477-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6477-124">OUTPUTS</span></span>

### <span data-ttu-id="d6477-125">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6477-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="d6477-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6477-126">NOTES</span></span>

## <span data-ttu-id="d6477-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6477-127">RELATED LINKS</span></span>
