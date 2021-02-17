---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232977"
---
# <span data-ttu-id="f51ba-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="f51ba-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="f51ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f51ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f51ba-103">Обновляет базу данных "ЕгосDB MongoDB".</span><span class="sxs-lookup"><span data-stu-id="f51ba-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="f51ba-104">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="f51ba-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="f51ba-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f51ba-105">SYNTAX</span></span>

### <span data-ttu-id="f51ba-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f51ba-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f51ba-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f51ba-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f51ba-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f51ba-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f51ba-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f51ba-109">DESCRIPTION</span></span>
<span data-ttu-id="f51ba-110">Обновляет базу данных "ЕгосDB MongoDB".</span><span class="sxs-lookup"><span data-stu-id="f51ba-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="f51ba-111">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="f51ba-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="f51ba-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f51ba-112">EXAMPLES</span></span>

### <span data-ttu-id="f51ba-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f51ba-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="f51ba-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f51ba-114">PARAMETERS</span></span>

### <span data-ttu-id="f51ba-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f51ba-115">-AccountName</span></span>
<span data-ttu-id="f51ba-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="f51ba-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f51ba-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f51ba-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f51ba-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="f51ba-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f51ba-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f51ba-119">-Confirm</span></span>
<span data-ttu-id="f51ba-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f51ba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f51ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f51ba-121">-DefaultProfile</span></span>
<span data-ttu-id="f51ba-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f51ba-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f51ba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f51ba-123">-InputObject</span></span>
<span data-ttu-id="f51ba-124">Объект базы данных Пнго.</span><span class="sxs-lookup"><span data-stu-id="f51ba-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="f51ba-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f51ba-125">-Name</span></span>
<span data-ttu-id="f51ba-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f51ba-126">Database name.</span></span>

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

### <span data-ttu-id="f51ba-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f51ba-127">-ParentObject</span></span>
<span data-ttu-id="f51ba-128">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="f51ba-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f51ba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f51ba-129">-ResourceGroupName</span></span>
<span data-ttu-id="f51ba-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f51ba-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f51ba-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="f51ba-131">-Throughput</span></span>
<span data-ttu-id="f51ba-132">Пропускная способность базы данных Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f51ba-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="f51ba-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="f51ba-133">Default value is 400.</span></span>

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

### <span data-ttu-id="f51ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f51ba-134">-WhatIf</span></span>
<span data-ttu-id="f51ba-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f51ba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f51ba-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f51ba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f51ba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51ba-137">CommonParameters</span></span>
<span data-ttu-id="f51ba-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f51ba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51ba-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f51ba-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51ba-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f51ba-140">INPUTS</span></span>

### <span data-ttu-id="f51ba-141">Нет</span><span class="sxs-lookup"><span data-stu-id="f51ba-141">None</span></span>

## <span data-ttu-id="f51ba-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f51ba-142">OUTPUTS</span></span>

### <span data-ttu-id="f51ba-143">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f51ba-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="f51ba-144">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f51ba-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f51ba-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f51ba-145">NOTES</span></span>

## <span data-ttu-id="f51ba-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f51ba-146">RELATED LINKS</span></span>
