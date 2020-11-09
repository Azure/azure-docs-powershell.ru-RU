---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315059"
---
# <span data-ttu-id="54729-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="54729-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="54729-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54729-102">SYNOPSIS</span></span>
<span data-ttu-id="54729-103">Возвращает базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="54729-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="54729-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54729-104">SYNTAX</span></span>

### <span data-ttu-id="54729-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54729-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54729-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54729-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54729-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54729-107">DESCRIPTION</span></span>
<span data-ttu-id="54729-108">Командлет **Get-AzCosmosDBGremlinDatabase** получает базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="54729-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="54729-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54729-109">EXAMPLES</span></span>

### <span data-ttu-id="54729-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54729-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="54729-111">Объект Resource (ресурс) включает _rid, _ts _etag.</span><span class="sxs-lookup"><span data-stu-id="54729-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="54729-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54729-112">PARAMETERS</span></span>

### <span data-ttu-id="54729-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="54729-113">-AccountName</span></span>
<span data-ttu-id="54729-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="54729-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="54729-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54729-115">-DefaultProfile</span></span>
<span data-ttu-id="54729-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54729-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54729-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54729-117">-Name</span></span>
<span data-ttu-id="54729-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="54729-118">Database name.</span></span>

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

### <span data-ttu-id="54729-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="54729-119">-ParentObject</span></span>
<span data-ttu-id="54729-120">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="54729-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54729-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54729-121">-ResourceGroupName</span></span>
<span data-ttu-id="54729-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54729-122">Name of resource group.</span></span>

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

### <span data-ttu-id="54729-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54729-123">CommonParameters</span></span>
<span data-ttu-id="54729-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54729-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54729-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54729-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54729-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54729-126">INPUTS</span></span>

### <span data-ttu-id="54729-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="54729-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="54729-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54729-128">OUTPUTS</span></span>

### <span data-ttu-id="54729-129">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="54729-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="54729-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="54729-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="54729-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="54729-131">NOTES</span></span>

## <span data-ttu-id="54729-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54729-132">RELATED LINKS</span></span>
