---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 9ba9c092f021041f1a56626a79e07b369b694d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065032"
---
# <span data-ttu-id="858b1-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="858b1-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="858b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="858b1-102">SYNOPSIS</span></span>
<span data-ttu-id="858b1-103">Получает параметры пропускной способности, соответствующие базе данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="858b1-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="858b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="858b1-104">SYNTAX</span></span>

### <span data-ttu-id="858b1-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="858b1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="858b1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="858b1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="858b1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="858b1-107">DESCRIPTION</span></span>
<span data-ttu-id="858b1-108">Командлет **Get-AzCosmosDBSqlDatabaseThroughput** получает параметры пропускной способности, соответствующие базе данных CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="858b1-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="858b1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="858b1-109">EXAMPLES</span></span>

### <span data-ttu-id="858b1-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="858b1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="858b1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="858b1-111">PARAMETERS</span></span>

### <span data-ttu-id="858b1-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="858b1-112">-AccountName</span></span>
<span data-ttu-id="858b1-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="858b1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="858b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858b1-114">-DefaultProfile</span></span>
<span data-ttu-id="858b1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="858b1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="858b1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="858b1-116">-InputObject</span></span>
<span data-ttu-id="858b1-117">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="858b1-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="858b1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="858b1-118">-Name</span></span>
<span data-ttu-id="858b1-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="858b1-119">Database name.</span></span>

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

### <span data-ttu-id="858b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="858b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="858b1-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="858b1-121">Name of resource group.</span></span>

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

### <span data-ttu-id="858b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858b1-122">CommonParameters</span></span>
<span data-ttu-id="858b1-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="858b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858b1-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="858b1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858b1-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="858b1-125">INPUTS</span></span>

### <span data-ttu-id="858b1-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="858b1-126">None</span></span>

## <span data-ttu-id="858b1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="858b1-127">OUTPUTS</span></span>

### <span data-ttu-id="858b1-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="858b1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="858b1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="858b1-129">NOTES</span></span>

## <span data-ttu-id="858b1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="858b1-130">RELATED LINKS</span></span>
