---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236847"
---
# <span data-ttu-id="54ae7-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="54ae7-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="54ae7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="54ae7-103">Создает новый объект типа PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="54ae7-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="54ae7-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="54ae7-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="54ae7-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54ae7-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54ae7-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54ae7-106">DESCRIPTION</span></span>
<span data-ttu-id="54ae7-107">Объект, соответствующий ConflictResolutionPolicy API SQL.</span><span class="sxs-lookup"><span data-stu-id="54ae7-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="54ae7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54ae7-108">EXAMPLES</span></span>

### <span data-ttu-id="54ae7-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54ae7-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="54ae7-110">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="54ae7-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="54ae7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54ae7-111">PARAMETERS</span></span>

### <span data-ttu-id="54ae7-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="54ae7-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="54ae7-113">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="54ae7-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="54ae7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ae7-114">-DefaultProfile</span></span>
<span data-ttu-id="54ae7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54ae7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54ae7-116">-Path</span><span class="sxs-lookup"><span data-stu-id="54ae7-116">-Path</span></span>
<span data-ttu-id="54ae7-117">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="54ae7-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="54ae7-118">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="54ae7-118">-Type</span></span>
<span data-ttu-id="54ae7-119">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="54ae7-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="54ae7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ae7-120">CommonParameters</span></span>
<span data-ttu-id="54ae7-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54ae7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ae7-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54ae7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ae7-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54ae7-123">INPUTS</span></span>

### <span data-ttu-id="54ae7-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="54ae7-124">None</span></span>

## <span data-ttu-id="54ae7-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54ae7-125">OUTPUTS</span></span>

### <span data-ttu-id="54ae7-126">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="54ae7-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="54ae7-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="54ae7-127">NOTES</span></span>

## <span data-ttu-id="54ae7-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54ae7-128">RELATED LINKS</span></span>