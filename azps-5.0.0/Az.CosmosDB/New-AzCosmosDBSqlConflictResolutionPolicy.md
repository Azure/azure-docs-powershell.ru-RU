---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314777"
---
# <span data-ttu-id="af4ad-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="af4ad-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="af4ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="af4ad-103">Создает новый объект типа PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="af4ad-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="af4ad-104">Она может быть передана в качестве значения параметра Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="af4ad-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="af4ad-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af4ad-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af4ad-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af4ad-106">DESCRIPTION</span></span>
<span data-ttu-id="af4ad-107">Объект, соответствующий ConflictResolutionPolicy API SQL.</span><span class="sxs-lookup"><span data-stu-id="af4ad-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="af4ad-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af4ad-108">EXAMPLES</span></span>

### <span data-ttu-id="af4ad-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af4ad-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="af4ad-110">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="af4ad-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="af4ad-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af4ad-111">PARAMETERS</span></span>

### <span data-ttu-id="af4ad-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="af4ad-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="af4ad-113">Указывается, если тип является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="af4ad-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="af4ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4ad-114">-DefaultProfile</span></span>
<span data-ttu-id="af4ad-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af4ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af4ad-116">-Path</span><span class="sxs-lookup"><span data-stu-id="af4ad-116">-Path</span></span>
<span data-ttu-id="af4ad-117">Должен быть указан, если тип — LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="af4ad-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="af4ad-118">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="af4ad-118">-Type</span></span>
<span data-ttu-id="af4ad-119">Может иметь значения: LastWriterWins, Custom, руководство.</span><span class="sxs-lookup"><span data-stu-id="af4ad-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="af4ad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4ad-120">CommonParameters</span></span>
<span data-ttu-id="af4ad-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af4ad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4ad-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af4ad-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4ad-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af4ad-123">INPUTS</span></span>

### <span data-ttu-id="af4ad-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="af4ad-124">None</span></span>

## <span data-ttu-id="af4ad-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af4ad-125">OUTPUTS</span></span>

### <span data-ttu-id="af4ad-126">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="af4ad-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="af4ad-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="af4ad-127">NOTES</span></span>

## <span data-ttu-id="af4ad-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af4ad-128">RELATED LINKS</span></span>
