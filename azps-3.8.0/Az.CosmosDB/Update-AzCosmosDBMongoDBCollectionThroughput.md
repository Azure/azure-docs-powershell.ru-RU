---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 605998d6bc5ae8b647b3644dc71b8063f0881910
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066654"
---
# <span data-ttu-id="fc50d-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="fc50d-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="fc50d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc50d-102">SYNOPSIS</span></span>
<span data-ttu-id="fc50d-103">Обновляет значение пропускной способности семейства CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="fc50d-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="fc50d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc50d-104">SYNTAX</span></span>

### <span data-ttu-id="fc50d-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc50d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc50d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc50d-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc50d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc50d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc50d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc50d-108">EXAMPLES</span></span>

### <span data-ttu-id="fc50d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc50d-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="fc50d-110">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="fc50d-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="fc50d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc50d-111">PARAMETERS</span></span>

### <span data-ttu-id="fc50d-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="fc50d-112">-AccountName</span></span>
<span data-ttu-id="fc50d-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="fc50d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fc50d-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc50d-114">-Confirm</span></span>
<span data-ttu-id="fc50d-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc50d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc50d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc50d-116">-DatabaseName</span></span>
<span data-ttu-id="fc50d-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="fc50d-117">Database name.</span></span>

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

### <span data-ttu-id="fc50d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc50d-118">-DefaultProfile</span></span>
<span data-ttu-id="fc50d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc50d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc50d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc50d-120">-InputObject</span></span>
<span data-ttu-id="fc50d-121">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="fc50d-121">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc50d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc50d-122">-Name</span></span>
<span data-ttu-id="fc50d-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="fc50d-123">Collection name.</span></span>

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

### <span data-ttu-id="fc50d-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fc50d-124">-ParentObject</span></span>
<span data-ttu-id="fc50d-125">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="fc50d-125">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc50d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc50d-126">-ResourceGroupName</span></span>
<span data-ttu-id="fc50d-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc50d-127">Name of resource group.</span></span>

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

### <span data-ttu-id="fc50d-128">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="fc50d-128">-Throughput</span></span>
<span data-ttu-id="fc50d-129">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="fc50d-129">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="fc50d-130">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="fc50d-130">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc50d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc50d-131">-WhatIf</span></span>
<span data-ttu-id="fc50d-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc50d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc50d-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc50d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc50d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc50d-134">CommonParameters</span></span>
<span data-ttu-id="fc50d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc50d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc50d-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc50d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc50d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc50d-137">INPUTS</span></span>

### <span data-ttu-id="fc50d-138">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fc50d-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="fc50d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc50d-139">OUTPUTS</span></span>

### <span data-ttu-id="fc50d-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fc50d-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fc50d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc50d-141">NOTES</span></span>

## <span data-ttu-id="fc50d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc50d-142">RELATED LINKS</span></span>
