---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315011"
---
# <span data-ttu-id="e18d1-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="e18d1-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="e18d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e18d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e18d1-103">Получает контейнер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e18d1-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e18d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e18d1-104">SYNTAX</span></span>

### <span data-ttu-id="e18d1-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e18d1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="e18d1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e18d1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e18d1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e18d1-107">DESCRIPTION</span></span>
<span data-ttu-id="e18d1-108">Командлет **Get-AzCosmosDBSqlContainer** получает список всех существующих контейнеров SQL CosmosDB для данного ResourceGroupName, AccountName и DatabaseName и получает один CosmosDB контейнер SQL для указанных ResourceGroupName, AccountName, DatabaseName и ContainerName.</span><span class="sxs-lookup"><span data-stu-id="e18d1-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="e18d1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e18d1-109">EXAMPLES</span></span>

### <span data-ttu-id="e18d1-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e18d1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="e18d1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e18d1-111">PARAMETERS</span></span>

### <span data-ttu-id="e18d1-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e18d1-112">-AccountName</span></span>
<span data-ttu-id="e18d1-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e18d1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e18d1-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e18d1-114">-DatabaseName</span></span>
<span data-ttu-id="e18d1-115">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e18d1-115">Database name.</span></span>

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

### <span data-ttu-id="e18d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18d1-116">-DefaultProfile</span></span>
<span data-ttu-id="e18d1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e18d1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e18d1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e18d1-118">-Name</span></span>
<span data-ttu-id="e18d1-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="e18d1-119">Container name.</span></span>

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

### <span data-ttu-id="e18d1-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e18d1-120">-ParentObject</span></span>
<span data-ttu-id="e18d1-121">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e18d1-121">Sql Database object.</span></span>

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

### <span data-ttu-id="e18d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e18d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="e18d1-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e18d1-123">Name of resource group.</span></span>

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

### <span data-ttu-id="e18d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18d1-124">CommonParameters</span></span>
<span data-ttu-id="e18d1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e18d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18d1-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e18d1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18d1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e18d1-127">INPUTS</span></span>

### <span data-ttu-id="e18d1-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="e18d1-128">None</span></span>

## <span data-ttu-id="e18d1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e18d1-129">OUTPUTS</span></span>

### <span data-ttu-id="e18d1-130">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e18d1-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="e18d1-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e18d1-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e18d1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e18d1-132">NOTES</span></span>

## <span data-ttu-id="e18d1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e18d1-133">RELATED LINKS</span></span>
