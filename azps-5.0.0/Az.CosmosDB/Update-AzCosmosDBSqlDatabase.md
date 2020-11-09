---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314513"
---
# <span data-ttu-id="f25ac-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f25ac-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="f25ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f25ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f25ac-103">Обновляет базу данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f25ac-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="f25ac-104">Выполняет операцию исправления на стороне клиента, считывая существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="f25ac-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="f25ac-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f25ac-105">SYNTAX</span></span>

### <span data-ttu-id="f25ac-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f25ac-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f25ac-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f25ac-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f25ac-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f25ac-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f25ac-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f25ac-109">DESCRIPTION</span></span>
<span data-ttu-id="f25ac-110">Обновляет базу данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f25ac-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="f25ac-111">Выполняет операцию исправления на стороне клиента, считывая существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="f25ac-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="f25ac-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f25ac-112">EXAMPLES</span></span>

### <span data-ttu-id="f25ac-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f25ac-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="f25ac-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f25ac-114">PARAMETERS</span></span>

### <span data-ttu-id="f25ac-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f25ac-115">-AccountName</span></span>
<span data-ttu-id="f25ac-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f25ac-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f25ac-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f25ac-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f25ac-118">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="f25ac-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f25ac-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f25ac-119">-Confirm</span></span>
<span data-ttu-id="f25ac-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f25ac-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f25ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25ac-121">-DefaultProfile</span></span>
<span data-ttu-id="f25ac-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f25ac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f25ac-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f25ac-123">-InputObject</span></span>
<span data-ttu-id="f25ac-124">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f25ac-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f25ac-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f25ac-125">-Name</span></span>
<span data-ttu-id="f25ac-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f25ac-126">Database name.</span></span>

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

### <span data-ttu-id="f25ac-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f25ac-127">-ParentObject</span></span>
<span data-ttu-id="f25ac-128">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f25ac-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f25ac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f25ac-129">-ResourceGroupName</span></span>
<span data-ttu-id="f25ac-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f25ac-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f25ac-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="f25ac-131">-Throughput</span></span>
<span data-ttu-id="f25ac-132">Пропускная способность базы данных SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f25ac-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="f25ac-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="f25ac-133">Default value is 400.</span></span>

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

### <span data-ttu-id="f25ac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f25ac-134">-WhatIf</span></span>
<span data-ttu-id="f25ac-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f25ac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f25ac-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f25ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f25ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25ac-137">CommonParameters</span></span>
<span data-ttu-id="f25ac-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f25ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25ac-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f25ac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25ac-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f25ac-140">INPUTS</span></span>

### <span data-ttu-id="f25ac-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f25ac-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="f25ac-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f25ac-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="f25ac-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f25ac-143">OUTPUTS</span></span>

### <span data-ttu-id="f25ac-144">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f25ac-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="f25ac-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f25ac-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f25ac-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="f25ac-146">NOTES</span></span>

## <span data-ttu-id="f25ac-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f25ac-147">RELATED LINKS</span></span>
