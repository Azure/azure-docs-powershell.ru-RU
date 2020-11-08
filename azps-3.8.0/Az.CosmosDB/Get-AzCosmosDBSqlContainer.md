---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074108"
---
# <span data-ttu-id="e3259-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="e3259-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="e3259-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3259-102">SYNOPSIS</span></span>
<span data-ttu-id="e3259-103">Получает контейнер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e3259-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e3259-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3259-104">SYNTAX</span></span>

### <span data-ttu-id="e3259-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3259-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="e3259-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3259-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3259-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3259-107">DESCRIPTION</span></span>
<span data-ttu-id="e3259-108">Командлет **Get-AzCosmosDBSqlContainer** получает список всех существующих контейнеров SQL CosmosDB для данного ResourceGroupName, AccountName и DatabaseName и получает один CosmosDB контейнер SQL для указанных ResourceGroupName, AccountName, DatabaseName и ContainerName.</span><span class="sxs-lookup"><span data-stu-id="e3259-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="e3259-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3259-109">EXAMPLES</span></span>

### <span data-ttu-id="e3259-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3259-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="e3259-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3259-111">PARAMETERS</span></span>

### <span data-ttu-id="e3259-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e3259-112">-AccountName</span></span>
<span data-ttu-id="e3259-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e3259-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e3259-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3259-114">-DatabaseName</span></span>
<span data-ttu-id="e3259-115">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e3259-115">Database name.</span></span>

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

### <span data-ttu-id="e3259-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3259-116">-DefaultProfile</span></span>
<span data-ttu-id="e3259-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3259-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3259-118">-Подробно</span><span class="sxs-lookup"><span data-stu-id="e3259-118">-Detailed</span></span>
<span data-ttu-id="e3259-119">Если он указан, командлет возвращает контейнер со значением пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e3259-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="e3259-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3259-120">-InputObject</span></span>
<span data-ttu-id="e3259-121">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e3259-121">Sql Database object.</span></span>

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

### <span data-ttu-id="e3259-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3259-122">-Name</span></span>
<span data-ttu-id="e3259-123">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="e3259-123">Container name.</span></span>

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

### <span data-ttu-id="e3259-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3259-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3259-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3259-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e3259-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3259-126">CommonParameters</span></span>
<span data-ttu-id="e3259-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3259-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3259-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3259-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3259-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3259-129">INPUTS</span></span>

### <span data-ttu-id="e3259-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="e3259-130">None</span></span>

## <span data-ttu-id="e3259-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3259-131">OUTPUTS</span></span>

### <span data-ttu-id="e3259-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e3259-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="e3259-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e3259-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e3259-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3259-134">NOTES</span></span>

## <span data-ttu-id="e3259-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3259-135">RELATED LINKS</span></span>
