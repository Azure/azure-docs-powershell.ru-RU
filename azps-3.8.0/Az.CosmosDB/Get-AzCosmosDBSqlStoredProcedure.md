---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: a9a81336ab921ebd63b8a969be5fbf65f4b7fa14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065031"
---
# <span data-ttu-id="bbc88-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="bbc88-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="bbc88-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbc88-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc88-103">Возвращает CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="bbc88-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="bbc88-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbc88-104">SYNTAX</span></span>

### <span data-ttu-id="bbc88-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbc88-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbc88-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbc88-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbc88-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbc88-107">DESCRIPTION</span></span>
<span data-ttu-id="bbc88-108">Командлет **Get-AzCosmosDBSqlStoredProcedure** получает список всех существующих CosmosDB SQL StoredProcedures для заданных ResourceGroupName, AccountName, DatabaseName и ContainerName и возвращает один CosmosDB SQL StoredProcedure для указанных ResourceGroupName, имя_учетной_записи, DatabaseName, ContainerName и StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="bbc88-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="bbc88-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbc88-109">EXAMPLES</span></span>

### <span data-ttu-id="bbc88-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbc88-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="bbc88-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbc88-111">PARAMETERS</span></span>

### <span data-ttu-id="bbc88-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="bbc88-112">-AccountName</span></span>
<span data-ttu-id="bbc88-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="bbc88-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bbc88-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bbc88-114">-ContainerName</span></span>
<span data-ttu-id="bbc88-115">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="bbc88-115">Container name.</span></span>

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

### <span data-ttu-id="bbc88-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bbc88-116">-DatabaseName</span></span>
<span data-ttu-id="bbc88-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="bbc88-117">Database name.</span></span>

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

### <span data-ttu-id="bbc88-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc88-118">-DefaultProfile</span></span>
<span data-ttu-id="bbc88-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc88-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbc88-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbc88-120">-InputObject</span></span>
<span data-ttu-id="bbc88-121">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="bbc88-121">Sql Container object.</span></span>

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

### <span data-ttu-id="bbc88-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bbc88-122">-Name</span></span>
<span data-ttu-id="bbc88-123">Имя сохраненного Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="bbc88-123">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="bbc88-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbc88-124">-ResourceGroupName</span></span>
<span data-ttu-id="bbc88-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bbc88-125">Name of resource group.</span></span>

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

### <span data-ttu-id="bbc88-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc88-126">CommonParameters</span></span>
<span data-ttu-id="bbc88-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbc88-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc88-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbc88-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc88-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbc88-129">INPUTS</span></span>

### <span data-ttu-id="bbc88-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="bbc88-130">None</span></span>

## <span data-ttu-id="bbc88-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbc88-131">OUTPUTS</span></span>

### <span data-ttu-id="bbc88-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="bbc88-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="bbc88-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbc88-133">NOTES</span></span>

## <span data-ttu-id="bbc88-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbc88-134">RELATED LINKS</span></span>
