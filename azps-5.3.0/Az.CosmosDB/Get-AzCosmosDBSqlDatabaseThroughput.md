---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508873"
---
# <span data-ttu-id="75cb0-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="75cb0-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="75cb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="75cb0-103">Возвращает параметры пропускной способности, соответствующие базе данных SQLБББББ.</span><span class="sxs-lookup"><span data-stu-id="75cb0-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="75cb0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75cb0-104">SYNTAX</span></span>

### <span data-ttu-id="75cb0-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75cb0-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75cb0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75cb0-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75cb0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75cb0-107">DESCRIPTION</span></span>
<span data-ttu-id="75cb0-108">Для этого с помощью cmdlet **get-AzCosmosDBSqlDatabaseThroughput** можно получить параметры пропускной способности, соответствующие базе данных Sql "Базой данных Sql".</span><span class="sxs-lookup"><span data-stu-id="75cb0-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="75cb0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75cb0-109">EXAMPLES</span></span>

### <span data-ttu-id="75cb0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75cb0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="75cb0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75cb0-111">PARAMETERS</span></span>

### <span data-ttu-id="75cb0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75cb0-112">-AccountName</span></span>
<span data-ttu-id="75cb0-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="75cb0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="75cb0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cb0-114">-DefaultProfile</span></span>
<span data-ttu-id="75cb0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75cb0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75cb0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75cb0-116">-InputObject</span></span>
<span data-ttu-id="75cb0-117">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="75cb0-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="75cb0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="75cb0-118">-Name</span></span>
<span data-ttu-id="75cb0-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="75cb0-119">Database name.</span></span>

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

### <span data-ttu-id="75cb0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75cb0-120">-ResourceGroupName</span></span>
<span data-ttu-id="75cb0-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75cb0-121">Name of resource group.</span></span>

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

### <span data-ttu-id="75cb0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cb0-122">CommonParameters</span></span>
<span data-ttu-id="75cb0-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cb0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cb0-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75cb0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cb0-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75cb0-125">INPUTS</span></span>

### <span data-ttu-id="75cb0-126">Нет</span><span class="sxs-lookup"><span data-stu-id="75cb0-126">None</span></span>

## <span data-ttu-id="75cb0-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75cb0-127">OUTPUTS</span></span>

### <span data-ttu-id="75cb0-128">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="75cb0-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="75cb0-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75cb0-129">NOTES</span></span>

## <span data-ttu-id="75cb0-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75cb0-130">RELATED LINKS</span></span>
