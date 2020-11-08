---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236850"
---
# <span data-ttu-id="0f5b1-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0f5b1-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="0f5b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5b1-103">Создает новый объект типа PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="0f5b1-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="0f5b1-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="0f5b1-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="0f5b1-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f5b1-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f5b1-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f5b1-106">DESCRIPTION</span></span>
<span data-ttu-id="0f5b1-107">Объект, соответствующий ConflictResolutionPolicy API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="0f5b1-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="0f5b1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f5b1-108">EXAMPLES</span></span>

### <span data-ttu-id="0f5b1-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f5b1-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="0f5b1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f5b1-110">PARAMETERS</span></span>

### <span data-ttu-id="0f5b1-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="0f5b1-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="0f5b1-112">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="0f5b1-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="0f5b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5b1-113">-DefaultProfile</span></span>
<span data-ttu-id="0f5b1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f5b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f5b1-115">-Path</span><span class="sxs-lookup"><span data-stu-id="0f5b1-115">-Path</span></span>
<span data-ttu-id="0f5b1-116">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="0f5b1-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="0f5b1-117">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="0f5b1-117">-Type</span></span>
<span data-ttu-id="0f5b1-118">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="0f5b1-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="0f5b1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5b1-119">CommonParameters</span></span>
<span data-ttu-id="0f5b1-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f5b1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5b1-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f5b1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5b1-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f5b1-122">INPUTS</span></span>

### <span data-ttu-id="0f5b1-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="0f5b1-123">None</span></span>

## <span data-ttu-id="0f5b1-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f5b1-124">OUTPUTS</span></span>

### <span data-ttu-id="0f5b1-125">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0f5b1-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="0f5b1-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f5b1-126">NOTES</span></span>

## <span data-ttu-id="0f5b1-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f5b1-127">RELATED LINKS</span></span>
