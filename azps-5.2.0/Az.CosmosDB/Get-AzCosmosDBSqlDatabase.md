---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393612"
---
# <span data-ttu-id="9f17b-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9f17b-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="9f17b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f17b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f17b-103">Получает базу данных SqlDb.</span><span class="sxs-lookup"><span data-stu-id="9f17b-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9f17b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f17b-104">SYNTAX</span></span>

### <span data-ttu-id="9f17b-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f17b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f17b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f17b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f17b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f17b-107">DESCRIPTION</span></span>
<span data-ttu-id="9f17b-108">Cmdlet **Get-AzCosmosDBSqlDatabase** получает список всех существующих SQL-баз данныхDB для заданной базы данных ResourceGroupName, AccountName и получает одну базу данных Sql "КодБазы" для данного ресурса ResourceGroupName, AccountName, DatabaseName и ContainerName.</span><span class="sxs-lookup"><span data-stu-id="9f17b-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="9f17b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f17b-109">EXAMPLES</span></span>

### <span data-ttu-id="9f17b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f17b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="9f17b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f17b-111">PARAMETERS</span></span>

### <span data-ttu-id="9f17b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9f17b-112">-AccountName</span></span>
<span data-ttu-id="9f17b-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="9f17b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9f17b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f17b-114">-DefaultProfile</span></span>
<span data-ttu-id="9f17b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f17b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f17b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9f17b-116">-Name</span></span>
<span data-ttu-id="9f17b-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f17b-117">Database name.</span></span>

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

### <span data-ttu-id="9f17b-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9f17b-118">-ParentObject</span></span>
<span data-ttu-id="9f17b-119">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="9f17b-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9f17b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f17b-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f17b-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f17b-121">Name of resource group.</span></span>

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

### <span data-ttu-id="9f17b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f17b-122">CommonParameters</span></span>
<span data-ttu-id="9f17b-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f17b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f17b-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f17b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f17b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f17b-125">INPUTS</span></span>

### <span data-ttu-id="9f17b-126">Нет</span><span class="sxs-lookup"><span data-stu-id="9f17b-126">None</span></span>

## <span data-ttu-id="9f17b-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f17b-127">OUTPUTS</span></span>

### <span data-ttu-id="9f17b-128">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9f17b-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="9f17b-129">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9f17b-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9f17b-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f17b-130">NOTES</span></span>

## <span data-ttu-id="9f17b-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f17b-131">RELATED LINKS</span></span>
