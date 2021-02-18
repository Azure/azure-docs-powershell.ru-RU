---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215460"
---
# <span data-ttu-id="da37a-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="da37a-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="da37a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da37a-102">SYNOPSIS</span></span>
<span data-ttu-id="da37a-103">Получает базу данных "ВайсDB МонгоDB"</span><span class="sxs-lookup"><span data-stu-id="da37a-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="da37a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da37a-104">SYNTAX</span></span>

### <span data-ttu-id="da37a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da37a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da37a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da37a-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da37a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da37a-107">DESCRIPTION</span></span>
<span data-ttu-id="da37a-108">Cmdlet **Get-AzCosmosDBMongoDBDatabase** получает базу данныхЦыDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="da37a-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="da37a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da37a-109">EXAMPLES</span></span>

### <span data-ttu-id="da37a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da37a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="da37a-111">Объект ресурсов содержит свойства _rid, _ts, _etag ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da37a-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="da37a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da37a-112">PARAMETERS</span></span>

### <span data-ttu-id="da37a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="da37a-113">-AccountName</span></span>
<span data-ttu-id="da37a-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="da37a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="da37a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da37a-115">-DefaultProfile</span></span>
<span data-ttu-id="da37a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da37a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da37a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da37a-117">-Name</span></span>
<span data-ttu-id="da37a-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="da37a-118">Database name.</span></span>

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

### <span data-ttu-id="da37a-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="da37a-119">-ParentObject</span></span>
<span data-ttu-id="da37a-120">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="da37a-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="da37a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da37a-121">-ResourceGroupName</span></span>
<span data-ttu-id="da37a-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da37a-122">Name of resource group.</span></span>

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

### <span data-ttu-id="da37a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da37a-123">CommonParameters</span></span>
<span data-ttu-id="da37a-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da37a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da37a-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da37a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da37a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da37a-126">INPUTS</span></span>

### <span data-ttu-id="da37a-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="da37a-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="da37a-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da37a-128">OUTPUTS</span></span>

### <span data-ttu-id="da37a-129">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="da37a-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="da37a-130">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="da37a-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="da37a-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da37a-131">NOTES</span></span>

## <span data-ttu-id="da37a-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da37a-132">RELATED LINKS</span></span>
