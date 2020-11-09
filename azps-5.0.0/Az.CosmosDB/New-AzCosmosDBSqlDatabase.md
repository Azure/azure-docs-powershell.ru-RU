---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 2953da3747404c0b6b98992cc8a8b80573da5129
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314762"
---
# <span data-ttu-id="95839-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="95839-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="95839-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95839-102">SYNOPSIS</span></span>
<span data-ttu-id="95839-103">Создает новую базу данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="95839-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="95839-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95839-104">SYNTAX</span></span>

### <span data-ttu-id="95839-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95839-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95839-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95839-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95839-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95839-107">DESCRIPTION</span></span>
<span data-ttu-id="95839-108">Создает новую базу данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="95839-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="95839-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95839-109">EXAMPLES</span></span>

### <span data-ttu-id="95839-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95839-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="95839-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95839-111">PARAMETERS</span></span>

### <span data-ttu-id="95839-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="95839-112">-AccountName</span></span>
<span data-ttu-id="95839-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="95839-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="95839-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="95839-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="95839-115">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="95839-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="95839-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95839-116">-Confirm</span></span>
<span data-ttu-id="95839-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95839-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95839-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95839-118">-DefaultProfile</span></span>
<span data-ttu-id="95839-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95839-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95839-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95839-120">-Name</span></span>
<span data-ttu-id="95839-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="95839-121">Database name.</span></span>

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

### <span data-ttu-id="95839-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="95839-122">-ParentObject</span></span>
<span data-ttu-id="95839-123">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="95839-123">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95839-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95839-124">-ResourceGroupName</span></span>
<span data-ttu-id="95839-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95839-125">Name of resource group.</span></span>

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

### <span data-ttu-id="95839-126">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="95839-126">-Throughput</span></span>
<span data-ttu-id="95839-127">Пропускная способность базы данных SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="95839-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="95839-128">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="95839-128">Default value is 400.</span></span>

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

### <span data-ttu-id="95839-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95839-129">-WhatIf</span></span>
<span data-ttu-id="95839-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95839-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95839-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95839-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95839-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95839-132">CommonParameters</span></span>
<span data-ttu-id="95839-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95839-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95839-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95839-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95839-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95839-135">INPUTS</span></span>

### <span data-ttu-id="95839-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="95839-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="95839-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95839-137">OUTPUTS</span></span>

### <span data-ttu-id="95839-138">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="95839-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="95839-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="95839-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="95839-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="95839-140">NOTES</span></span>

## <span data-ttu-id="95839-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95839-141">RELATED LINKS</span></span>
