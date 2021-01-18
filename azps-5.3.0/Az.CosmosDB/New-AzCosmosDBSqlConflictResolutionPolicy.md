---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519265"
---
# <span data-ttu-id="7be68-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="7be68-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="7be68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7be68-102">SYNOPSIS</span></span>
<span data-ttu-id="7be68-103">Создание объекта типа PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7be68-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="7be68-104">Его можно передать в качестве значения параметра для Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="7be68-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="7be68-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7be68-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7be68-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7be68-106">DESCRIPTION</span></span>
<span data-ttu-id="7be68-107">Объект, соответствующий SQL API ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7be68-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="7be68-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7be68-108">EXAMPLES</span></span>

### <span data-ttu-id="7be68-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7be68-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="7be68-110">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="7be68-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="7be68-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7be68-111">PARAMETERS</span></span>

### <span data-ttu-id="7be68-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="7be68-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="7be68-113">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="7be68-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="7be68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be68-114">-DefaultProfile</span></span>
<span data-ttu-id="7be68-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7be68-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7be68-116">-Path</span><span class="sxs-lookup"><span data-stu-id="7be68-116">-Path</span></span>
<span data-ttu-id="7be68-117">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="7be68-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="7be68-118">-Type</span><span class="sxs-lookup"><span data-stu-id="7be68-118">-Type</span></span>
<span data-ttu-id="7be68-119">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="7be68-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="7be68-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be68-120">CommonParameters</span></span>
<span data-ttu-id="7be68-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7be68-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be68-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7be68-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be68-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7be68-123">INPUTS</span></span>

### <span data-ttu-id="7be68-124">Нет</span><span class="sxs-lookup"><span data-stu-id="7be68-124">None</span></span>

## <span data-ttu-id="7be68-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7be68-125">OUTPUTS</span></span>

### <span data-ttu-id="7be68-126">Microsoft.Azure.Commands.АsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="7be68-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="7be68-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7be68-127">NOTES</span></span>

## <span data-ttu-id="7be68-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7be68-128">RELATED LINKS</span></span>
