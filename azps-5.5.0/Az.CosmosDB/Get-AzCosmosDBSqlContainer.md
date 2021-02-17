---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238546"
---
# <span data-ttu-id="1386f-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="1386f-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="1386f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1386f-102">SYNOPSIS</span></span>
<span data-ttu-id="1386f-103">Получает контейнер SQLDb.</span><span class="sxs-lookup"><span data-stu-id="1386f-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="1386f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1386f-104">SYNTAX</span></span>

### <span data-ttu-id="1386f-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1386f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="1386f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1386f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1386f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1386f-107">DESCRIPTION</span></span>
<span data-ttu-id="1386f-108">С  его учетной записью можно получить список всех существующих контейнеров Sql Для Пользователя ResourceGroupName, AccountName и DatabaseName, а также один контейнер SqlБDb для заданной группы ресурсов ResourceGroupName, AccountName, DatabaseName и ContainerName.</span><span class="sxs-lookup"><span data-stu-id="1386f-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="1386f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1386f-109">EXAMPLES</span></span>

### <span data-ttu-id="1386f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1386f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="1386f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1386f-111">PARAMETERS</span></span>

### <span data-ttu-id="1386f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1386f-112">-AccountName</span></span>
<span data-ttu-id="1386f-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="1386f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1386f-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1386f-114">-DatabaseName</span></span>
<span data-ttu-id="1386f-115">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="1386f-115">Database name.</span></span>

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

### <span data-ttu-id="1386f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1386f-116">-DefaultProfile</span></span>
<span data-ttu-id="1386f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1386f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1386f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1386f-118">-Name</span></span>
<span data-ttu-id="1386f-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="1386f-119">Container name.</span></span>

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

### <span data-ttu-id="1386f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1386f-120">-ParentObject</span></span>
<span data-ttu-id="1386f-121">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="1386f-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1386f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1386f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1386f-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1386f-123">Name of resource group.</span></span>

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

### <span data-ttu-id="1386f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1386f-124">CommonParameters</span></span>
<span data-ttu-id="1386f-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1386f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1386f-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1386f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1386f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1386f-127">INPUTS</span></span>

### <span data-ttu-id="1386f-128">Нет</span><span class="sxs-lookup"><span data-stu-id="1386f-128">None</span></span>

## <span data-ttu-id="1386f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1386f-129">OUTPUTS</span></span>

### <span data-ttu-id="1386f-130">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="1386f-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="1386f-131">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1386f-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1386f-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1386f-132">NOTES</span></span>

## <span data-ttu-id="1386f-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1386f-133">RELATED LINKS</span></span>
