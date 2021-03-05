---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: c67627068ef2fc90f8322b2e8b63dd6cd68acbe3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007971"
---
# <span data-ttu-id="ff234-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff234-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="ff234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff234-102">SYNOPSIS</span></span>
<span data-ttu-id="ff234-103">Создание объекта типа PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ff234-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="ff234-104">Его можно передать в качестве значения параметра set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="ff234-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="ff234-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff234-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff234-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff234-106">DESCRIPTION</span></span>
<span data-ttu-id="ff234-107">Объект, соответствующий API Гремлина ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ff234-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="ff234-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff234-108">EXAMPLES</span></span>

### <span data-ttu-id="ff234-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff234-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="ff234-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff234-110">PARAMETERS</span></span>

### <span data-ttu-id="ff234-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="ff234-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="ff234-112">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="ff234-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="ff234-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff234-113">-DefaultProfile</span></span>
<span data-ttu-id="ff234-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff234-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff234-115">-Path</span><span class="sxs-lookup"><span data-stu-id="ff234-115">-Path</span></span>
<span data-ttu-id="ff234-116">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="ff234-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="ff234-117">-Type</span><span class="sxs-lookup"><span data-stu-id="ff234-117">-Type</span></span>
<span data-ttu-id="ff234-118">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="ff234-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="ff234-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff234-119">CommonParameters</span></span>
<span data-ttu-id="ff234-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff234-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff234-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff234-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff234-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff234-122">INPUTS</span></span>

### <span data-ttu-id="ff234-123">Нет</span><span class="sxs-lookup"><span data-stu-id="ff234-123">None</span></span>

## <span data-ttu-id="ff234-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff234-124">OUTPUTS</span></span>

### <span data-ttu-id="ff234-125">Microsoft.Azure.Commands.АsDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff234-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="ff234-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff234-126">NOTES</span></span>

## <span data-ttu-id="ff234-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff234-127">RELATED LINKS</span></span>
