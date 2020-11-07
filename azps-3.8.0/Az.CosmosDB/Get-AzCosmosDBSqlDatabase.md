---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 5efdbc3f1f8172ba59a78d4ec462f57a527faf07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912895"
---
# <span data-ttu-id="09dad-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09dad-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="09dad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09dad-102">SYNOPSIS</span></span>
<span data-ttu-id="09dad-103">Возвращает базу данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="09dad-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="09dad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09dad-104">SYNTAX</span></span>

### <span data-ttu-id="09dad-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09dad-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09dad-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09dad-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09dad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09dad-107">DESCRIPTION</span></span>
<span data-ttu-id="09dad-108">Командлет **Get-AzCosmosDBSqlDatabase** получает список всех существующих баз данных SQL CosmosDB для данного ResourceGroupName, AccountName и получает одну CosmosDB базу данных SQL для указанных ResourceGroupName, имя_учетной_записи, DatabaseName и ContainerName.</span><span class="sxs-lookup"><span data-stu-id="09dad-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="09dad-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09dad-109">EXAMPLES</span></span>

### <span data-ttu-id="09dad-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="09dad-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="09dad-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09dad-111">PARAMETERS</span></span>

### <span data-ttu-id="09dad-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="09dad-112">-AccountName</span></span>
<span data-ttu-id="09dad-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="09dad-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09dad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09dad-114">-DefaultProfile</span></span>
<span data-ttu-id="09dad-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09dad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09dad-116">-Подробно</span><span class="sxs-lookup"><span data-stu-id="09dad-116">-Detailed</span></span>
<span data-ttu-id="09dad-117">Если он указан, командлет возвращает контейнер со значением пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="09dad-117">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="09dad-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09dad-118">-InputObject</span></span>
<span data-ttu-id="09dad-119">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="09dad-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09dad-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09dad-120">-Name</span></span>
<span data-ttu-id="09dad-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="09dad-121">Database name.</span></span>

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

### <span data-ttu-id="09dad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09dad-122">-ResourceGroupName</span></span>
<span data-ttu-id="09dad-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09dad-123">Name of resource group.</span></span>

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

### <span data-ttu-id="09dad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09dad-124">CommonParameters</span></span>
<span data-ttu-id="09dad-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09dad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09dad-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09dad-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09dad-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09dad-127">INPUTS</span></span>

### <span data-ttu-id="09dad-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="09dad-128">None</span></span>

## <span data-ttu-id="09dad-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09dad-129">OUTPUTS</span></span>

### <span data-ttu-id="09dad-130">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="09dad-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="09dad-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="09dad-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="09dad-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="09dad-132">NOTES</span></span>

## <span data-ttu-id="09dad-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09dad-133">RELATED LINKS</span></span>
