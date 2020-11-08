---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244628"
---
# <span data-ttu-id="b147a-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="b147a-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="b147a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b147a-102">SYNOPSIS</span></span>
<span data-ttu-id="b147a-103">Создание новой базы данных CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="b147a-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="b147a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b147a-104">SYNTAX</span></span>

### <span data-ttu-id="b147a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b147a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b147a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b147a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b147a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b147a-107">DESCRIPTION</span></span>
<span data-ttu-id="b147a-108">Создание новой базы данных CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="b147a-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="b147a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b147a-109">EXAMPLES</span></span>

### <span data-ttu-id="b147a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b147a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="b147a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b147a-111">PARAMETERS</span></span>

### <span data-ttu-id="b147a-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b147a-112">-AccountName</span></span>
<span data-ttu-id="b147a-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b147a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b147a-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b147a-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b147a-115">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="b147a-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b147a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b147a-116">-Confirm</span></span>
<span data-ttu-id="b147a-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b147a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b147a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b147a-118">-DefaultProfile</span></span>
<span data-ttu-id="b147a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b147a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b147a-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b147a-120">-Name</span></span>
<span data-ttu-id="b147a-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b147a-121">Database name.</span></span>

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

### <span data-ttu-id="b147a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b147a-122">-ParentObject</span></span>
<span data-ttu-id="b147a-123">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b147a-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b147a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b147a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b147a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b147a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b147a-126">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="b147a-126">-Throughput</span></span>
<span data-ttu-id="b147a-127">Пропускная способность Mongo базы данных (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b147a-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="b147a-128">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="b147a-128">Default value is 400.</span></span>

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

### <span data-ttu-id="b147a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b147a-129">-WhatIf</span></span>
<span data-ttu-id="b147a-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b147a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b147a-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b147a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b147a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b147a-132">CommonParameters</span></span>
<span data-ttu-id="b147a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b147a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b147a-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b147a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b147a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b147a-135">INPUTS</span></span>

### <span data-ttu-id="b147a-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="b147a-136">None</span></span>

## <span data-ttu-id="b147a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b147a-137">OUTPUTS</span></span>

### <span data-ttu-id="b147a-138">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b147a-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="b147a-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="b147a-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="b147a-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b147a-140">NOTES</span></span>

## <span data-ttu-id="b147a-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b147a-141">RELATED LINKS</span></span>
