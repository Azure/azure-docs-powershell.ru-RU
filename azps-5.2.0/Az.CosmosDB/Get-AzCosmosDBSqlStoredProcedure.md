---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417876"
---
# <span data-ttu-id="52b37-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="52b37-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="52b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52b37-102">SYNOPSIS</span></span>
<span data-ttu-id="52b37-103">Получает ЕлисейСDB Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="52b37-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="52b37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="52b37-104">SYNTAX</span></span>

### <span data-ttu-id="52b37-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="52b37-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52b37-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52b37-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52b37-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52b37-107">DESCRIPTION</span></span>
<span data-ttu-id="52b37-108">Cmdlet **Get-AzCosmosDBSqlStoredProcedure** получает список всех существующих SqsDB Sql StoredProcedures для данной базы данных ResourceGroupName, AccountName, DatabaseName и ContainerName и получает одну Учетную запись Sql StoredProcedure для заданного имени ResourceGroupName, AccountName, DatabaseName, ContainerName и StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="52b37-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="52b37-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="52b37-109">EXAMPLES</span></span>

### <span data-ttu-id="52b37-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52b37-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="52b37-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52b37-111">PARAMETERS</span></span>

### <span data-ttu-id="52b37-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52b37-112">-AccountName</span></span>
<span data-ttu-id="52b37-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="52b37-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="52b37-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="52b37-114">-ContainerName</span></span>
<span data-ttu-id="52b37-115">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="52b37-115">Container name.</span></span>

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

### <span data-ttu-id="52b37-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52b37-116">-DatabaseName</span></span>
<span data-ttu-id="52b37-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="52b37-117">Database name.</span></span>

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

### <span data-ttu-id="52b37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b37-118">-DefaultProfile</span></span>
<span data-ttu-id="52b37-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52b37-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b37-120">-Name</span><span class="sxs-lookup"><span data-stu-id="52b37-120">-Name</span></span>
<span data-ttu-id="52b37-121">Имя хранимой prcodecure.</span><span class="sxs-lookup"><span data-stu-id="52b37-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="52b37-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="52b37-122">-ParentObject</span></span>
<span data-ttu-id="52b37-123">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="52b37-123">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52b37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b37-124">-ResourceGroupName</span></span>
<span data-ttu-id="52b37-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52b37-125">Name of resource group.</span></span>

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

### <span data-ttu-id="52b37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b37-126">CommonParameters</span></span>
<span data-ttu-id="52b37-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b37-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52b37-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b37-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52b37-129">INPUTS</span></span>

### <span data-ttu-id="52b37-130">Нет</span><span class="sxs-lookup"><span data-stu-id="52b37-130">None</span></span>

## <span data-ttu-id="52b37-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52b37-131">OUTPUTS</span></span>

### <span data-ttu-id="52b37-132">Microsoft.Azure.Commands.GetsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="52b37-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="52b37-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="52b37-133">NOTES</span></span>

## <span data-ttu-id="52b37-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52b37-134">RELATED LINKS</span></span>
