---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405236"
---
# <span data-ttu-id="b3b37-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="b3b37-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="b3b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3b37-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b37-103">Возвращает параметры пропускной способности, соответствующие контейнеру Sql Container в ПараметрахDb.</span><span class="sxs-lookup"><span data-stu-id="b3b37-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="b3b37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3b37-104">SYNTAX</span></span>

### <span data-ttu-id="b3b37-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3b37-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b37-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b37-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3b37-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3b37-107">DESCRIPTION</span></span>
<span data-ttu-id="b3b37-108">Для этого с помощью cmdlet **get-AzCosmosDBSqlContainerThroughput** задаются параметры пропускной способности, соответствующие Sql Container для AzsDB.</span><span class="sxs-lookup"><span data-stu-id="b3b37-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="b3b37-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3b37-109">EXAMPLES</span></span>

### <span data-ttu-id="b3b37-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3b37-110">Example 1</span></span>
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

## <span data-ttu-id="b3b37-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3b37-111">PARAMETERS</span></span>

### <span data-ttu-id="b3b37-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3b37-112">-AccountName</span></span>
<span data-ttu-id="b3b37-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="b3b37-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b3b37-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3b37-114">-DatabaseName</span></span>
<span data-ttu-id="b3b37-115">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b3b37-115">Database name.</span></span>

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

### <span data-ttu-id="b3b37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b37-116">-DefaultProfile</span></span>
<span data-ttu-id="b3b37-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3b37-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3b37-118">-InputObject</span></span>
<span data-ttu-id="b3b37-119">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="b3b37-119">Sql Container object.</span></span>

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

### <span data-ttu-id="b3b37-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b3b37-120">-Name</span></span>
<span data-ttu-id="b3b37-121">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="b3b37-121">Container name.</span></span>

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

### <span data-ttu-id="b3b37-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b37-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3b37-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b3b37-123">Name of resource group.</span></span>

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

### <span data-ttu-id="b3b37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b37-124">CommonParameters</span></span>
<span data-ttu-id="b3b37-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b37-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3b37-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b37-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3b37-127">INPUTS</span></span>

### <span data-ttu-id="b3b37-128">Нет</span><span class="sxs-lookup"><span data-stu-id="b3b37-128">None</span></span>

## <span data-ttu-id="b3b37-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3b37-129">OUTPUTS</span></span>

### <span data-ttu-id="b3b37-130">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b3b37-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b3b37-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3b37-131">NOTES</span></span>

## <span data-ttu-id="b3b37-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3b37-132">RELATED LINKS</span></span>
