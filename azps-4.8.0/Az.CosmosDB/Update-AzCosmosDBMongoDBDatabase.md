---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242854"
---
# <span data-ttu-id="db657-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="db657-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="db657-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db657-102">SYNOPSIS</span></span>
<span data-ttu-id="db657-103">Обновляет базу данных CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="db657-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="db657-104">Выполняет операцию исправления на стороне клиента, считывая существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="db657-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="db657-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db657-105">SYNTAX</span></span>

### <span data-ttu-id="db657-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db657-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db657-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db657-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db657-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db657-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db657-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db657-109">DESCRIPTION</span></span>
<span data-ttu-id="db657-110">Обновляет базу данных CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="db657-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="db657-111">Выполняет операцию исправления на стороне клиента, считывая существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="db657-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="db657-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db657-112">EXAMPLES</span></span>

### <span data-ttu-id="db657-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db657-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="db657-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db657-114">PARAMETERS</span></span>

### <span data-ttu-id="db657-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="db657-115">-AccountName</span></span>
<span data-ttu-id="db657-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="db657-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="db657-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="db657-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="db657-118">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="db657-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="db657-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db657-119">-Confirm</span></span>
<span data-ttu-id="db657-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db657-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db657-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db657-121">-DefaultProfile</span></span>
<span data-ttu-id="db657-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db657-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db657-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db657-123">-InputObject</span></span>
<span data-ttu-id="db657-124">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="db657-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="db657-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db657-125">-Name</span></span>
<span data-ttu-id="db657-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="db657-126">Database name.</span></span>

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

### <span data-ttu-id="db657-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="db657-127">-ParentObject</span></span>
<span data-ttu-id="db657-128">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="db657-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="db657-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db657-129">-ResourceGroupName</span></span>
<span data-ttu-id="db657-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db657-130">Name of resource group.</span></span>

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

### <span data-ttu-id="db657-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="db657-131">-Throughput</span></span>
<span data-ttu-id="db657-132">Пропускная способность Mongo базы данных (RU/s).</span><span class="sxs-lookup"><span data-stu-id="db657-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="db657-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="db657-133">Default value is 400.</span></span>

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

### <span data-ttu-id="db657-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db657-134">-WhatIf</span></span>
<span data-ttu-id="db657-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db657-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db657-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db657-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db657-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db657-137">CommonParameters</span></span>
<span data-ttu-id="db657-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db657-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db657-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db657-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db657-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db657-140">INPUTS</span></span>

### <span data-ttu-id="db657-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="db657-141">None</span></span>

## <span data-ttu-id="db657-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db657-142">OUTPUTS</span></span>

### <span data-ttu-id="db657-143">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="db657-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="db657-144">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="db657-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="db657-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="db657-145">NOTES</span></span>

## <span data-ttu-id="db657-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db657-146">RELATED LINKS</span></span>
