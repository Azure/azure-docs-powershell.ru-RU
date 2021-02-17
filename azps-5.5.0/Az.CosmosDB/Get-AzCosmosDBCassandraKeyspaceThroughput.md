---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233132"
---
# <span data-ttu-id="77f34-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="77f34-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="77f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77f34-102">SYNOPSIS</span></span>
<span data-ttu-id="77f34-103">Получает значение пропускной способности клавиши Александры.</span><span class="sxs-lookup"><span data-stu-id="77f34-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="77f34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77f34-104">SYNTAX</span></span>

### <span data-ttu-id="77f34-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77f34-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77f34-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77f34-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77f34-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77f34-107">DESCRIPTION</span></span>
<span data-ttu-id="77f34-108">С **помощью cmdlet get-AzCosmosDBCassandraKeyspaceThroughput** можно получить объект пропускной способности, соответствующий заданной области клавиш.</span><span class="sxs-lookup"><span data-stu-id="77f34-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="77f34-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77f34-109">EXAMPLES</span></span>

### <span data-ttu-id="77f34-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77f34-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="77f34-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77f34-111">PARAMETERS</span></span>

### <span data-ttu-id="77f34-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="77f34-112">-AccountName</span></span>
<span data-ttu-id="77f34-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="77f34-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="77f34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f34-114">-DefaultProfile</span></span>
<span data-ttu-id="77f34-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77f34-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f34-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77f34-116">-InputObject</span></span>
<span data-ttu-id="77f34-117">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="77f34-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="77f34-118">-Name</span><span class="sxs-lookup"><span data-stu-id="77f34-118">-Name</span></span>
<span data-ttu-id="77f34-119">Имя Клавишной области Александры.</span><span class="sxs-lookup"><span data-stu-id="77f34-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="77f34-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f34-120">-ResourceGroupName</span></span>
<span data-ttu-id="77f34-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77f34-121">Name of resource group.</span></span>

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

### <span data-ttu-id="77f34-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f34-122">CommonParameters</span></span>
<span data-ttu-id="77f34-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f34-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f34-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77f34-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f34-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77f34-125">INPUTS</span></span>

### <span data-ttu-id="77f34-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="77f34-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="77f34-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77f34-127">OUTPUTS</span></span>

### <span data-ttu-id="77f34-128">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="77f34-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="77f34-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77f34-129">NOTES</span></span>

## <span data-ttu-id="77f34-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77f34-130">RELATED LINKS</span></span>
