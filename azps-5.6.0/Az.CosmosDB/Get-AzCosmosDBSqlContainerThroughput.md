---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 3ceb7ccbb789c21fc0fdb51244260e6a54b3e900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998864"
---
# <span data-ttu-id="94efc-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="94efc-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="94efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94efc-102">SYNOPSIS</span></span>
<span data-ttu-id="94efc-103">Возвращает параметры пропускной способности, соответствующие контейнеру Sql Container в ПараметрахDb.</span><span class="sxs-lookup"><span data-stu-id="94efc-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="94efc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94efc-104">SYNTAX</span></span>

### <span data-ttu-id="94efc-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94efc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94efc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94efc-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94efc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94efc-107">DESCRIPTION</span></span>
<span data-ttu-id="94efc-108">Для этого с помощью cmdlet **get-AzCosmosDBSqlContainerThroughput** задаются параметры пропускной способности, соответствующие Sql Container для AzsDB.</span><span class="sxs-lookup"><span data-stu-id="94efc-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="94efc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94efc-109">EXAMPLES</span></span>

### <span data-ttu-id="94efc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94efc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="94efc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94efc-111">PARAMETERS</span></span>

### <span data-ttu-id="94efc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="94efc-112">-AccountName</span></span>
<span data-ttu-id="94efc-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="94efc-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="94efc-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="94efc-114">-DatabaseName</span></span>
<span data-ttu-id="94efc-115">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="94efc-115">Database name.</span></span>

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

### <span data-ttu-id="94efc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94efc-116">-DefaultProfile</span></span>
<span data-ttu-id="94efc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94efc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94efc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94efc-118">-InputObject</span></span>
<span data-ttu-id="94efc-119">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="94efc-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94efc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="94efc-120">-Name</span></span>
<span data-ttu-id="94efc-121">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="94efc-121">Container name.</span></span>

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

### <span data-ttu-id="94efc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94efc-122">-ResourceGroupName</span></span>
<span data-ttu-id="94efc-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94efc-123">Name of resource group.</span></span>

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

### <span data-ttu-id="94efc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94efc-124">CommonParameters</span></span>
<span data-ttu-id="94efc-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94efc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94efc-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94efc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94efc-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94efc-127">INPUTS</span></span>

### <span data-ttu-id="94efc-128">Нет</span><span class="sxs-lookup"><span data-stu-id="94efc-128">None</span></span>

## <span data-ttu-id="94efc-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94efc-129">OUTPUTS</span></span>

### <span data-ttu-id="94efc-130">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="94efc-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="94efc-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94efc-131">NOTES</span></span>

## <span data-ttu-id="94efc-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94efc-132">RELATED LINKS</span></span>
