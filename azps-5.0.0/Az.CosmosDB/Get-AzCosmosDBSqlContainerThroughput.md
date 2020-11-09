---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315005"
---
# <span data-ttu-id="36714-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="36714-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="36714-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36714-102">SYNOPSIS</span></span>
<span data-ttu-id="36714-103">Получает параметры пропускной способности, соответствующие контейнеру SQL для CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="36714-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="36714-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36714-104">SYNTAX</span></span>

### <span data-ttu-id="36714-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36714-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36714-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36714-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36714-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36714-107">DESCRIPTION</span></span>
<span data-ttu-id="36714-108">Командлет **Get-AzCosmosDBSqlContainerThroughput** получает параметры пропускной способности, соответствующие контейнеру SQL для CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="36714-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="36714-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36714-109">EXAMPLES</span></span>

### <span data-ttu-id="36714-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36714-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="36714-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36714-111">PARAMETERS</span></span>

### <span data-ttu-id="36714-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="36714-112">-AccountName</span></span>
<span data-ttu-id="36714-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="36714-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="36714-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36714-114">-DatabaseName</span></span>
<span data-ttu-id="36714-115">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="36714-115">Database name.</span></span>

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

### <span data-ttu-id="36714-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36714-116">-DefaultProfile</span></span>
<span data-ttu-id="36714-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36714-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36714-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36714-118">-InputObject</span></span>
<span data-ttu-id="36714-119">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="36714-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36714-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36714-120">-Name</span></span>
<span data-ttu-id="36714-121">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="36714-121">Container name.</span></span>

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

### <span data-ttu-id="36714-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36714-122">-ResourceGroupName</span></span>
<span data-ttu-id="36714-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36714-123">Name of resource group.</span></span>

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

### <span data-ttu-id="36714-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36714-124">CommonParameters</span></span>
<span data-ttu-id="36714-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36714-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36714-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36714-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36714-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36714-127">INPUTS</span></span>

### <span data-ttu-id="36714-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="36714-128">None</span></span>

## <span data-ttu-id="36714-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36714-129">OUTPUTS</span></span>

### <span data-ttu-id="36714-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="36714-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="36714-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="36714-131">NOTES</span></span>

## <span data-ttu-id="36714-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36714-132">RELATED LINKS</span></span>
