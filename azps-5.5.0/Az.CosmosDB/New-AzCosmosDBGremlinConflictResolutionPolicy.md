---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233033"
---
# <span data-ttu-id="25bcd-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="25bcd-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="25bcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="25bcd-103">Создание объекта типа PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="25bcd-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="25bcd-104">Его можно передать в качестве значения параметра set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="25bcd-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="25bcd-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="25bcd-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25bcd-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25bcd-106">DESCRIPTION</span></span>
<span data-ttu-id="25bcd-107">Объект, соответствующий API Гремлина ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="25bcd-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="25bcd-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="25bcd-108">EXAMPLES</span></span>

### <span data-ttu-id="25bcd-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="25bcd-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="25bcd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25bcd-110">PARAMETERS</span></span>

### <span data-ttu-id="25bcd-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="25bcd-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="25bcd-112">Предоставляется при пользовательском типе.</span><span class="sxs-lookup"><span data-stu-id="25bcd-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="25bcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bcd-113">-DefaultProfile</span></span>
<span data-ttu-id="25bcd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25bcd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25bcd-115">-Path</span><span class="sxs-lookup"><span data-stu-id="25bcd-115">-Path</span></span>
<span data-ttu-id="25bcd-116">Должен предоставляться при типе LastWins.</span><span class="sxs-lookup"><span data-stu-id="25bcd-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="25bcd-117">-Type</span><span class="sxs-lookup"><span data-stu-id="25bcd-117">-Type</span></span>
<span data-ttu-id="25bcd-118">Могут иметь значения: LastWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="25bcd-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="25bcd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bcd-119">CommonParameters</span></span>
<span data-ttu-id="25bcd-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25bcd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bcd-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25bcd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bcd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25bcd-122">INPUTS</span></span>

### <span data-ttu-id="25bcd-123">Нет</span><span class="sxs-lookup"><span data-stu-id="25bcd-123">None</span></span>

## <span data-ttu-id="25bcd-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25bcd-124">OUTPUTS</span></span>

### <span data-ttu-id="25bcd-125">Microsoft.Azure.Commands.АsDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="25bcd-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="25bcd-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="25bcd-126">NOTES</span></span>

## <span data-ttu-id="25bcd-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25bcd-127">RELATED LINKS</span></span>
