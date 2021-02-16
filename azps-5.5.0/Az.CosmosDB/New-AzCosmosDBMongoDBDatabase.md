---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211316"
---
# <span data-ttu-id="58a03-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="58a03-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="58a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58a03-102">SYNOPSIS</span></span>
<span data-ttu-id="58a03-103">Создает базу данных "ДискиDB " MongoDB".</span><span class="sxs-lookup"><span data-stu-id="58a03-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="58a03-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58a03-104">SYNTAX</span></span>

### <span data-ttu-id="58a03-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58a03-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58a03-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a03-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58a03-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58a03-107">DESCRIPTION</span></span>
<span data-ttu-id="58a03-108">Создается новая база данных "ДискиDB " MongoDB.</span><span class="sxs-lookup"><span data-stu-id="58a03-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="58a03-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58a03-109">EXAMPLES</span></span>

### <span data-ttu-id="58a03-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58a03-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="58a03-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58a03-111">PARAMETERS</span></span>

### <span data-ttu-id="58a03-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58a03-112">-AccountName</span></span>
<span data-ttu-id="58a03-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="58a03-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="58a03-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="58a03-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="58a03-115">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="58a03-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="58a03-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58a03-116">-Confirm</span></span>
<span data-ttu-id="58a03-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58a03-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a03-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a03-118">-DefaultProfile</span></span>
<span data-ttu-id="58a03-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58a03-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a03-120">-Name</span><span class="sxs-lookup"><span data-stu-id="58a03-120">-Name</span></span>
<span data-ttu-id="58a03-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="58a03-121">Database name.</span></span>

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

### <span data-ttu-id="58a03-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="58a03-122">-ParentObject</span></span>
<span data-ttu-id="58a03-123">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="58a03-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="58a03-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a03-124">-ResourceGroupName</span></span>
<span data-ttu-id="58a03-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58a03-125">Name of resource group.</span></span>

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

### <span data-ttu-id="58a03-126">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="58a03-126">-Throughput</span></span>
<span data-ttu-id="58a03-127">Пропускная способность базы данных Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="58a03-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="58a03-128">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="58a03-128">Default value is 400.</span></span>

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

### <span data-ttu-id="58a03-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a03-129">-WhatIf</span></span>
<span data-ttu-id="58a03-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58a03-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a03-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="58a03-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a03-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a03-132">CommonParameters</span></span>
<span data-ttu-id="58a03-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a03-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a03-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58a03-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a03-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58a03-135">INPUTS</span></span>

### <span data-ttu-id="58a03-136">Нет</span><span class="sxs-lookup"><span data-stu-id="58a03-136">None</span></span>

## <span data-ttu-id="58a03-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58a03-137">OUTPUTS</span></span>

### <span data-ttu-id="58a03-138">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="58a03-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="58a03-139">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="58a03-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="58a03-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58a03-140">NOTES</span></span>

## <span data-ttu-id="58a03-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58a03-141">RELATED LINKS</span></span>
