---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: dbffec52b5c1b30f6b00febbc2e6c952beda669e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977288"
---
# <span data-ttu-id="c5939-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="c5939-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="c5939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5939-102">SYNOPSIS</span></span>
<span data-ttu-id="c5939-103">Обновляет базу данных "ЕгосDB MongoDB".</span><span class="sxs-lookup"><span data-stu-id="c5939-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="c5939-104">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="c5939-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="c5939-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5939-105">SYNTAX</span></span>

### <span data-ttu-id="c5939-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5939-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5939-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5939-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5939-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5939-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5939-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5939-109">DESCRIPTION</span></span>
<span data-ttu-id="c5939-110">Обновляет базу данных "ЕгосDB MongoDB".</span><span class="sxs-lookup"><span data-stu-id="c5939-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="c5939-111">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="c5939-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="c5939-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5939-112">EXAMPLES</span></span>

### <span data-ttu-id="c5939-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c5939-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="c5939-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5939-114">PARAMETERS</span></span>

### <span data-ttu-id="c5939-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c5939-115">-AccountName</span></span>
<span data-ttu-id="c5939-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="c5939-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c5939-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c5939-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c5939-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="c5939-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c5939-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5939-119">-Confirm</span></span>
<span data-ttu-id="c5939-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5939-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5939-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5939-121">-DefaultProfile</span></span>
<span data-ttu-id="c5939-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5939-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5939-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5939-123">-InputObject</span></span>
<span data-ttu-id="c5939-124">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="c5939-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5939-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c5939-125">-Name</span></span>
<span data-ttu-id="c5939-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c5939-126">Database name.</span></span>

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

### <span data-ttu-id="c5939-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c5939-127">-ParentObject</span></span>
<span data-ttu-id="c5939-128">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="c5939-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c5939-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5939-129">-ResourceGroupName</span></span>
<span data-ttu-id="c5939-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5939-130">Name of resource group.</span></span>

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

### <span data-ttu-id="c5939-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="c5939-131">-Throughput</span></span>
<span data-ttu-id="c5939-132">Пропускная способность базы данных Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c5939-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="c5939-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="c5939-133">Default value is 400.</span></span>

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

### <span data-ttu-id="c5939-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5939-134">-WhatIf</span></span>
<span data-ttu-id="c5939-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5939-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5939-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c5939-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5939-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5939-137">CommonParameters</span></span>
<span data-ttu-id="c5939-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5939-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5939-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5939-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5939-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5939-140">INPUTS</span></span>

### <span data-ttu-id="c5939-141">Нет</span><span class="sxs-lookup"><span data-stu-id="c5939-141">None</span></span>

## <span data-ttu-id="c5939-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5939-142">OUTPUTS</span></span>

### <span data-ttu-id="c5939-143">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c5939-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="c5939-144">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c5939-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="c5939-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5939-145">NOTES</span></span>

## <span data-ttu-id="c5939-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5939-146">RELATED LINKS</span></span>
