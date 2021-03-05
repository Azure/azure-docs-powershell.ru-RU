---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 0dfcffe55eb3214f4be9d6ccfb34231d1c9ea50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994468"
---
# <span data-ttu-id="b4a4c-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="b4a4c-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="b4a4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a4c-103">Получает базу данных "ГрадыDB " MongoDB"</span><span class="sxs-lookup"><span data-stu-id="b4a4c-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="b4a4c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4a4c-104">SYNTAX</span></span>

### <span data-ttu-id="b4a4c-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4a4c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4a4c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4a4c-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4a4c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4a4c-107">DESCRIPTION</span></span>
<span data-ttu-id="b4a4c-108">Cmdlet **Get-AzCosmosDBMongoDBDatabase** получает базу данныхЦыDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="b4a4c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4a4c-109">EXAMPLES</span></span>

### <span data-ttu-id="b4a4c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4a4c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="b4a4c-111">Объект ресурсов содержит свойства _rid, _ts, _etag ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="b4a4c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4a4c-112">PARAMETERS</span></span>

### <span data-ttu-id="b4a4c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4a4c-113">-AccountName</span></span>
<span data-ttu-id="b4a4c-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="b4a4c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b4a4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a4c-115">-DefaultProfile</span></span>
<span data-ttu-id="b4a4c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4a4c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b4a4c-117">-Name</span></span>
<span data-ttu-id="b4a4c-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-118">Database name.</span></span>

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

### <span data-ttu-id="b4a4c-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4a4c-119">-ParentObject</span></span>
<span data-ttu-id="b4a4c-120">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="b4a4c-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a4c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a4c-121">-ResourceGroupName</span></span>
<span data-ttu-id="b4a4c-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-122">Name of resource group.</span></span>

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

### <span data-ttu-id="b4a4c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a4c-123">CommonParameters</span></span>
<span data-ttu-id="b4a4c-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a4c-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4a4c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a4c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4a4c-126">INPUTS</span></span>

### <span data-ttu-id="b4a4c-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b4a4c-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b4a4c-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4a4c-128">OUTPUTS</span></span>

### <span data-ttu-id="b4a4c-129">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b4a4c-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="b4a4c-130">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b4a4c-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b4a4c-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4a4c-131">NOTES</span></span>

## <span data-ttu-id="b4a4c-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4a4c-132">RELATED LINKS</span></span>
