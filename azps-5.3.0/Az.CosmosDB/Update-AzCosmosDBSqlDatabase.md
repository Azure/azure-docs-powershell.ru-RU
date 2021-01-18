---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519173"
---
# <span data-ttu-id="d8135-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d8135-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="d8135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8135-102">SYNOPSIS</span></span>
<span data-ttu-id="d8135-103">Обновляет базу данных SQLDb.</span><span class="sxs-lookup"><span data-stu-id="d8135-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="d8135-104">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="d8135-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d8135-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8135-105">SYNTAX</span></span>

### <span data-ttu-id="d8135-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8135-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8135-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8135-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8135-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8135-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8135-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8135-109">DESCRIPTION</span></span>
<span data-ttu-id="d8135-110">Обновляет базу данных SQLDb.</span><span class="sxs-lookup"><span data-stu-id="d8135-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="d8135-111">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="d8135-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d8135-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8135-112">EXAMPLES</span></span>

### <span data-ttu-id="d8135-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8135-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="d8135-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8135-114">PARAMETERS</span></span>

### <span data-ttu-id="d8135-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d8135-115">-AccountName</span></span>
<span data-ttu-id="d8135-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="d8135-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d8135-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d8135-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d8135-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="d8135-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d8135-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8135-119">-Confirm</span></span>
<span data-ttu-id="d8135-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d8135-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8135-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8135-121">-DefaultProfile</span></span>
<span data-ttu-id="d8135-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8135-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8135-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8135-123">-InputObject</span></span>
<span data-ttu-id="d8135-124">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="d8135-124">Sql Database object.</span></span>

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

### <span data-ttu-id="d8135-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d8135-125">-Name</span></span>
<span data-ttu-id="d8135-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d8135-126">Database name.</span></span>

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

### <span data-ttu-id="d8135-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d8135-127">-ParentObject</span></span>
<span data-ttu-id="d8135-128">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="d8135-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d8135-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8135-129">-ResourceGroupName</span></span>
<span data-ttu-id="d8135-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8135-130">Name of resource group.</span></span>

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

### <span data-ttu-id="d8135-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="d8135-131">-Throughput</span></span>
<span data-ttu-id="d8135-132">Пропускная способность SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d8135-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="d8135-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="d8135-133">Default value is 400.</span></span>

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

### <span data-ttu-id="d8135-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8135-134">-WhatIf</span></span>
<span data-ttu-id="d8135-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8135-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8135-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d8135-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8135-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8135-137">CommonParameters</span></span>
<span data-ttu-id="d8135-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8135-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8135-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8135-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8135-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8135-140">INPUTS</span></span>

### <span data-ttu-id="d8135-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d8135-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="d8135-142">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d8135-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="d8135-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8135-143">OUTPUTS</span></span>

### <span data-ttu-id="d8135-144">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d8135-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d8135-145">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d8135-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d8135-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8135-146">NOTES</span></span>

## <span data-ttu-id="d8135-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8135-147">RELATED LINKS</span></span>
