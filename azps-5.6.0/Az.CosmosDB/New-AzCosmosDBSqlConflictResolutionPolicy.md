---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: e5742cde3a39cb2bf7dc96b952b3129d353235f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985200"
---
# <span data-ttu-id="5219f-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5219f-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="5219f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5219f-102">SYNOPSIS</span></span>
<span data-ttu-id="5219f-103">Создание объекта типа PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="5219f-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="5219f-104">Его можно передать в качестве значения параметра для Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="5219f-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="5219f-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5219f-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5219f-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5219f-106">DESCRIPTION</span></span>
<span data-ttu-id="5219f-107">Объект, соответствующий SQL API ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="5219f-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="5219f-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5219f-108">EXAMPLES</span></span>

### <span data-ttu-id="5219f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5219f-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="5219f-110">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="5219f-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="5219f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5219f-111">PARAMETERS</span></span>

### <span data-ttu-id="5219f-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="5219f-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="5219f-113">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="5219f-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="5219f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5219f-114">-DefaultProfile</span></span>
<span data-ttu-id="5219f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5219f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5219f-116">-Path</span><span class="sxs-lookup"><span data-stu-id="5219f-116">-Path</span></span>
<span data-ttu-id="5219f-117">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="5219f-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="5219f-118">-Type</span><span class="sxs-lookup"><span data-stu-id="5219f-118">-Type</span></span>
<span data-ttu-id="5219f-119">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="5219f-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="5219f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5219f-120">CommonParameters</span></span>
<span data-ttu-id="5219f-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5219f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5219f-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5219f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5219f-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5219f-123">INPUTS</span></span>

### <span data-ttu-id="5219f-124">Нет</span><span class="sxs-lookup"><span data-stu-id="5219f-124">None</span></span>

## <span data-ttu-id="5219f-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5219f-125">OUTPUTS</span></span>

### <span data-ttu-id="5219f-126">Microsoft.Azure.Commands.АsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5219f-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="5219f-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5219f-127">NOTES</span></span>

## <span data-ttu-id="5219f-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5219f-128">RELATED LINKS</span></span>
