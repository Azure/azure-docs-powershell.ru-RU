---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1bfb0ec8392c0ddcce20db839f1817688e8feb7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977203"
---
# <span data-ttu-id="d4218-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4218-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="d4218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4218-102">SYNOPSIS</span></span>
<span data-ttu-id="d4218-103">Обновляет базу данных SQLDb.</span><span class="sxs-lookup"><span data-stu-id="d4218-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="d4218-104">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="d4218-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d4218-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4218-105">SYNTAX</span></span>

### <span data-ttu-id="d4218-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4218-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4218-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4218-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4218-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4218-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4218-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4218-109">DESCRIPTION</span></span>
<span data-ttu-id="d4218-110">Обновляет базу данных SQLDb.</span><span class="sxs-lookup"><span data-stu-id="d4218-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="d4218-111">Выполняет обновление на стороне клиента, считыв существующую базу данных.</span><span class="sxs-lookup"><span data-stu-id="d4218-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d4218-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4218-112">EXAMPLES</span></span>

### <span data-ttu-id="d4218-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4218-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="d4218-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4218-114">PARAMETERS</span></span>

### <span data-ttu-id="d4218-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d4218-115">-AccountName</span></span>
<span data-ttu-id="d4218-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="d4218-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d4218-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d4218-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d4218-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="d4218-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d4218-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4218-119">-Confirm</span></span>
<span data-ttu-id="d4218-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4218-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4218-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4218-121">-DefaultProfile</span></span>
<span data-ttu-id="d4218-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4218-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4218-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4218-123">-InputObject</span></span>
<span data-ttu-id="d4218-124">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="d4218-124">Sql Database object.</span></span>

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

### <span data-ttu-id="d4218-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d4218-125">-Name</span></span>
<span data-ttu-id="d4218-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d4218-126">Database name.</span></span>

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

### <span data-ttu-id="d4218-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d4218-127">-ParentObject</span></span>
<span data-ttu-id="d4218-128">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="d4218-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d4218-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4218-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4218-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4218-130">Name of resource group.</span></span>

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

### <span data-ttu-id="d4218-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="d4218-131">-Throughput</span></span>
<span data-ttu-id="d4218-132">Пропускная способность SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d4218-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="d4218-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="d4218-133">Default value is 400.</span></span>

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

### <span data-ttu-id="d4218-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4218-134">-WhatIf</span></span>
<span data-ttu-id="d4218-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4218-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4218-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d4218-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4218-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4218-137">CommonParameters</span></span>
<span data-ttu-id="d4218-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4218-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4218-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4218-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4218-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4218-140">INPUTS</span></span>

### <span data-ttu-id="d4218-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d4218-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="d4218-142">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d4218-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="d4218-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4218-143">OUTPUTS</span></span>

### <span data-ttu-id="d4218-144">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d4218-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d4218-145">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d4218-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d4218-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4218-146">NOTES</span></span>

## <span data-ttu-id="d4218-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4218-147">RELATED LINKS</span></span>
