---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245075"
---
# <span data-ttu-id="7f632-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="7f632-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="7f632-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f632-102">SYNOPSIS</span></span>
<span data-ttu-id="7f632-103">Обновляет значение пропускной способности семейства CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="7f632-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7f632-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f632-104">SYNTAX</span></span>

### <span data-ttu-id="7f632-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f632-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f632-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f632-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f632-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f632-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f632-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f632-108">DESCRIPTION</span></span>
<span data-ttu-id="7f632-109">Обновляет значение пропускной способности семейства CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="7f632-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7f632-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f632-110">EXAMPLES</span></span>

### <span data-ttu-id="7f632-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f632-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="7f632-112">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="7f632-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="7f632-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f632-113">PARAMETERS</span></span>

### <span data-ttu-id="7f632-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="7f632-114">-AccountName</span></span>
<span data-ttu-id="7f632-115">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7f632-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7f632-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7f632-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7f632-117">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="7f632-117">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f632-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f632-118">-Confirm</span></span>
<span data-ttu-id="7f632-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7f632-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f632-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f632-120">-DatabaseName</span></span>
<span data-ttu-id="7f632-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="7f632-121">Database name.</span></span>

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

### <span data-ttu-id="7f632-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f632-122">-DefaultProfile</span></span>
<span data-ttu-id="7f632-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f632-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f632-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f632-124">-InputObject</span></span>
<span data-ttu-id="7f632-125">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="7f632-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="7f632-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f632-126">-Name</span></span>
<span data-ttu-id="7f632-127">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="7f632-127">Collection name.</span></span>

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

### <span data-ttu-id="7f632-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7f632-128">-ParentObject</span></span>
<span data-ttu-id="7f632-129">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="7f632-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="7f632-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f632-130">-ResourceGroupName</span></span>
<span data-ttu-id="7f632-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7f632-131">Name of resource group.</span></span>

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

### <span data-ttu-id="7f632-132">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="7f632-132">-Throughput</span></span>
<span data-ttu-id="7f632-133">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="7f632-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="7f632-134">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="7f632-134">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f632-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f632-135">-WhatIf</span></span>
<span data-ttu-id="7f632-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7f632-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f632-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7f632-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f632-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f632-138">CommonParameters</span></span>
<span data-ttu-id="7f632-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f632-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f632-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f632-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f632-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f632-141">INPUTS</span></span>

### <span data-ttu-id="7f632-142">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7f632-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="7f632-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f632-143">OUTPUTS</span></span>

### <span data-ttu-id="7f632-144">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7f632-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7f632-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f632-145">NOTES</span></span>

## <span data-ttu-id="7f632-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f632-146">RELATED LINKS</span></span>
