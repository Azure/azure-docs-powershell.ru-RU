---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244198"
---
# <span data-ttu-id="62e91-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62e91-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="62e91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62e91-102">SYNOPSIS</span></span>
<span data-ttu-id="62e91-103">Возвращает базу данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="62e91-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="62e91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62e91-104">SYNTAX</span></span>

### <span data-ttu-id="62e91-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62e91-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62e91-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62e91-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62e91-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62e91-107">DESCRIPTION</span></span>
<span data-ttu-id="62e91-108">Командлет **Get-AzCosmosDBSqlDatabase** получает список всех существующих баз данных SQL CosmosDB для данного ResourceGroupName, AccountName и получает одну CosmosDB базу данных SQL для указанных ResourceGroupName, имя_учетной_записи, DatabaseName и ContainerName.</span><span class="sxs-lookup"><span data-stu-id="62e91-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="62e91-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62e91-109">EXAMPLES</span></span>

### <span data-ttu-id="62e91-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62e91-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="62e91-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62e91-111">PARAMETERS</span></span>

### <span data-ttu-id="62e91-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="62e91-112">-AccountName</span></span>
<span data-ttu-id="62e91-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="62e91-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="62e91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e91-114">-DefaultProfile</span></span>
<span data-ttu-id="62e91-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62e91-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e91-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62e91-116">-Name</span></span>
<span data-ttu-id="62e91-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="62e91-117">Database name.</span></span>

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

### <span data-ttu-id="62e91-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="62e91-118">-ParentObject</span></span>
<span data-ttu-id="62e91-119">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="62e91-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="62e91-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e91-120">-ResourceGroupName</span></span>
<span data-ttu-id="62e91-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62e91-121">Name of resource group.</span></span>

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

### <span data-ttu-id="62e91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e91-122">CommonParameters</span></span>
<span data-ttu-id="62e91-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62e91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e91-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62e91-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e91-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62e91-125">INPUTS</span></span>

### <span data-ttu-id="62e91-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="62e91-126">None</span></span>

## <span data-ttu-id="62e91-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62e91-127">OUTPUTS</span></span>

### <span data-ttu-id="62e91-128">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="62e91-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="62e91-129">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="62e91-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="62e91-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="62e91-130">NOTES</span></span>

## <span data-ttu-id="62e91-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62e91-131">RELATED LINKS</span></span>
