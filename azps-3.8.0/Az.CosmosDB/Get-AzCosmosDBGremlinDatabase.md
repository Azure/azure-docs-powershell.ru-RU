---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074125"
---
# <span data-ttu-id="7f68d-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="7f68d-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="7f68d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f68d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f68d-103">Возвращает базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="7f68d-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="7f68d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f68d-104">SYNTAX</span></span>

### <span data-ttu-id="7f68d-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f68d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f68d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f68d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f68d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f68d-107">DESCRIPTION</span></span>
<span data-ttu-id="7f68d-108">Командлет **Get-AzCosmosDBGremlinDatabase** получает базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="7f68d-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="7f68d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f68d-109">EXAMPLES</span></span>

### <span data-ttu-id="7f68d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f68d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="7f68d-111">Объект Resource (ресурс) включает _rid, _ts _etag.</span><span class="sxs-lookup"><span data-stu-id="7f68d-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="7f68d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f68d-112">PARAMETERS</span></span>

### <span data-ttu-id="7f68d-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="7f68d-113">-AccountName</span></span>
<span data-ttu-id="7f68d-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7f68d-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f68d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f68d-115">-DefaultProfile</span></span>
<span data-ttu-id="7f68d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f68d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f68d-117">-Подробно</span><span class="sxs-lookup"><span data-stu-id="7f68d-117">-Detailed</span></span>
<span data-ttu-id="7f68d-118">Если он указан, командлет возвращает базу данных с соответствующим значением пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="7f68d-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f68d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f68d-119">-InputObject</span></span>
<span data-ttu-id="7f68d-120">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="7f68d-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f68d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f68d-121">-Name</span></span>
<span data-ttu-id="7f68d-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="7f68d-122">Database name.</span></span>

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

### <span data-ttu-id="7f68d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f68d-123">-ResourceGroupName</span></span>
<span data-ttu-id="7f68d-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7f68d-124">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f68d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f68d-125">CommonParameters</span></span>
<span data-ttu-id="7f68d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f68d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f68d-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f68d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f68d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f68d-128">INPUTS</span></span>

### <span data-ttu-id="7f68d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7f68d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7f68d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f68d-130">OUTPUTS</span></span>

### <span data-ttu-id="7f68d-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7f68d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="7f68d-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7f68d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7f68d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f68d-133">NOTES</span></span>

## <span data-ttu-id="7f68d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f68d-134">RELATED LINKS</span></span>
