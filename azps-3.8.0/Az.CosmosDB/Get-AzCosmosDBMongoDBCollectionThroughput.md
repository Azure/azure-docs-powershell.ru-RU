---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074119"
---
# <span data-ttu-id="16538-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="16538-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="16538-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16538-102">SYNOPSIS</span></span>
<span data-ttu-id="16538-103">Возвращает свойства пропускной способности CosmosDB коллекции MongoDB.</span><span class="sxs-lookup"><span data-stu-id="16538-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="16538-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16538-104">SYNTAX</span></span>

### <span data-ttu-id="16538-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16538-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16538-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16538-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16538-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16538-107">DESCRIPTION</span></span>
<span data-ttu-id="16538-108">Командлет **Get-AzCosmosDBMongoDBCollectionThroughput** получает свойства пропускной способности коллекции MongoDB.</span><span class="sxs-lookup"><span data-stu-id="16538-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="16538-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16538-109">EXAMPLES</span></span>

### <span data-ttu-id="16538-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16538-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="16538-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16538-111">PARAMETERS</span></span>

### <span data-ttu-id="16538-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="16538-112">-AccountName</span></span>
<span data-ttu-id="16538-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="16538-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="16538-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16538-114">-Confirm</span></span>
<span data-ttu-id="16538-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16538-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16538-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16538-116">-DatabaseName</span></span>
<span data-ttu-id="16538-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="16538-117">Database name.</span></span>

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

### <span data-ttu-id="16538-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16538-118">-DefaultProfile</span></span>
<span data-ttu-id="16538-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16538-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16538-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16538-120">-InputObject</span></span>
<span data-ttu-id="16538-121">Если он указан, командлет возвращает коллекцию с соответствующим значением пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="16538-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16538-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16538-122">-Name</span></span>
<span data-ttu-id="16538-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="16538-123">Collection name.</span></span>

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

### <span data-ttu-id="16538-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16538-124">-ResourceGroupName</span></span>
<span data-ttu-id="16538-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16538-125">Name of resource group.</span></span>

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

### <span data-ttu-id="16538-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16538-126">-WhatIf</span></span>
<span data-ttu-id="16538-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16538-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16538-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16538-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16538-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16538-129">CommonParameters</span></span>
<span data-ttu-id="16538-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16538-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16538-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16538-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16538-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16538-132">INPUTS</span></span>

### <span data-ttu-id="16538-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="16538-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="16538-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16538-134">OUTPUTS</span></span>

### <span data-ttu-id="16538-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="16538-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="16538-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="16538-136">NOTES</span></span>

## <span data-ttu-id="16538-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16538-137">RELATED LINKS</span></span>
