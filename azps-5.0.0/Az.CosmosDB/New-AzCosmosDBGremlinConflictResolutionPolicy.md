---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314858"
---
# <span data-ttu-id="fa45a-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fa45a-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="fa45a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa45a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa45a-103">Создает новый объект типа PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="fa45a-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="fa45a-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="fa45a-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="fa45a-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa45a-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa45a-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa45a-106">DESCRIPTION</span></span>
<span data-ttu-id="fa45a-107">Объект, соответствующий ConflictResolutionPolicy API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="fa45a-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="fa45a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa45a-108">EXAMPLES</span></span>

### <span data-ttu-id="fa45a-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa45a-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="fa45a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa45a-110">PARAMETERS</span></span>

### <span data-ttu-id="fa45a-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="fa45a-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="fa45a-112">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="fa45a-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="fa45a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa45a-113">-DefaultProfile</span></span>
<span data-ttu-id="fa45a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa45a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa45a-115">-Path</span><span class="sxs-lookup"><span data-stu-id="fa45a-115">-Path</span></span>
<span data-ttu-id="fa45a-116">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="fa45a-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="fa45a-117">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="fa45a-117">-Type</span></span>
<span data-ttu-id="fa45a-118">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="fa45a-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="fa45a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa45a-119">CommonParameters</span></span>
<span data-ttu-id="fa45a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa45a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa45a-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa45a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa45a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa45a-122">INPUTS</span></span>

### <span data-ttu-id="fa45a-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="fa45a-123">None</span></span>

## <span data-ttu-id="fa45a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa45a-124">OUTPUTS</span></span>

### <span data-ttu-id="fa45a-125">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fa45a-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="fa45a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa45a-126">NOTES</span></span>

## <span data-ttu-id="fa45a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa45a-127">RELATED LINKS</span></span>
