---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244204"
---
# <span data-ttu-id="ec0d9-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ec0d9-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="ec0d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec0d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0d9-103">Возвращает свойства пропускной способности CosmosDB для базы данных MongoDB.</span><span class="sxs-lookup"><span data-stu-id="ec0d9-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="ec0d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec0d9-104">SYNTAX</span></span>

### <span data-ttu-id="ec0d9-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec0d9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec0d9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec0d9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec0d9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec0d9-107">DESCRIPTION</span></span>
<span data-ttu-id="ec0d9-108">Командлет **Get-AzCosmosDBMongoDBDatabaseThroughput** получает свойства пропускной способности базы данных MongoDB.</span><span class="sxs-lookup"><span data-stu-id="ec0d9-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="ec0d9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec0d9-109">EXAMPLES</span></span>

### <span data-ttu-id="ec0d9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec0d9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="ec0d9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec0d9-111">PARAMETERS</span></span>

### <span data-ttu-id="ec0d9-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ec0d9-112">-AccountName</span></span>
<span data-ttu-id="ec0d9-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ec0d9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ec0d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0d9-114">-DefaultProfile</span></span>
<span data-ttu-id="ec0d9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec0d9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec0d9-116">-InputObject</span></span>
<span data-ttu-id="ec0d9-117">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ec0d9-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec0d9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec0d9-118">-Name</span></span>
<span data-ttu-id="ec0d9-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ec0d9-119">Database name.</span></span>

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

### <span data-ttu-id="ec0d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec0d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec0d9-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec0d9-121">Name of resource group.</span></span>

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

### <span data-ttu-id="ec0d9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0d9-122">CommonParameters</span></span>
<span data-ttu-id="ec0d9-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec0d9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0d9-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec0d9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0d9-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec0d9-125">INPUTS</span></span>

### <span data-ttu-id="ec0d9-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="ec0d9-126">None</span></span>

## <span data-ttu-id="ec0d9-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec0d9-127">OUTPUTS</span></span>

### <span data-ttu-id="ec0d9-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ec0d9-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ec0d9-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec0d9-129">NOTES</span></span>

## <span data-ttu-id="ec0d9-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec0d9-130">RELATED LINKS</span></span>
