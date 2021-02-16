---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230817"
---
# <span data-ttu-id="bbdcd-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="bbdcd-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="bbdcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbdcd-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdcd-103">Обновляет значение пропускной способности коллекции ВайсDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="bbdcd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bbdcd-104">SYNTAX</span></span>

### <span data-ttu-id="bbdcd-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bbdcd-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbdcd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbdcd-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbdcd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbdcd-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbdcd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbdcd-108">DESCRIPTION</span></span>
<span data-ttu-id="bbdcd-109">Обновляет значение пропускной способности коллекции ВайсDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="bbdcd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bbdcd-110">EXAMPLES</span></span>

### <span data-ttu-id="bbdcd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbdcd-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="bbdcd-112">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="bbdcd-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="bbdcd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbdcd-113">PARAMETERS</span></span>

### <span data-ttu-id="bbdcd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bbdcd-114">-AccountName</span></span>
<span data-ttu-id="bbdcd-115">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="bbdcd-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bbdcd-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="bbdcd-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="bbdcd-117">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="bbdcd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbdcd-118">-Confirm</span></span>
<span data-ttu-id="bbdcd-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbdcd-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bbdcd-120">-DatabaseName</span></span>
<span data-ttu-id="bbdcd-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-121">Database name.</span></span>

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

### <span data-ttu-id="bbdcd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdcd-122">-DefaultProfile</span></span>
<span data-ttu-id="bbdcd-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbdcd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbdcd-124">-InputObject</span></span>
<span data-ttu-id="bbdcd-125">Объект базы данных Пнго.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="bbdcd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bbdcd-126">-Name</span></span>
<span data-ttu-id="bbdcd-127">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-127">Collection name.</span></span>

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

### <span data-ttu-id="bbdcd-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bbdcd-128">-ParentObject</span></span>
<span data-ttu-id="bbdcd-129">Объект базы данных Пнго.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="bbdcd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdcd-130">-ResourceGroupName</span></span>
<span data-ttu-id="bbdcd-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-131">Name of resource group.</span></span>

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

### <span data-ttu-id="bbdcd-132">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="bbdcd-132">-Throughput</span></span>
<span data-ttu-id="bbdcd-133">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="bbdcd-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="bbdcd-134">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-134">Default value is 400.</span></span>

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

### <span data-ttu-id="bbdcd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbdcd-135">-WhatIf</span></span>
<span data-ttu-id="bbdcd-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbdcd-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbdcd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdcd-138">CommonParameters</span></span>
<span data-ttu-id="bbdcd-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbdcd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdcd-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbdcd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdcd-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbdcd-141">INPUTS</span></span>

### <span data-ttu-id="bbdcd-142">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bbdcd-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="bbdcd-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bbdcd-143">OUTPUTS</span></span>

### <span data-ttu-id="bbdcd-144">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bbdcd-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bbdcd-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bbdcd-145">NOTES</span></span>

## <span data-ttu-id="bbdcd-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbdcd-146">RELATED LINKS</span></span>
