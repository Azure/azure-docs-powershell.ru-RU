---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 23e4ed96f464d29e95bacd04b93326cb5ce8e3da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977176"
---
# <span data-ttu-id="ddfa1-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ddfa1-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="ddfa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddfa1-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfa1-103">Обновляет значение пропускной способности базы данных SqlDb.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ddfa1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ddfa1-104">SYNTAX</span></span>

### <span data-ttu-id="ddfa1-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ddfa1-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddfa1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddfa1-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddfa1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddfa1-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddfa1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddfa1-108">DESCRIPTION</span></span>
<span data-ttu-id="ddfa1-109">Обновляет значение пропускной способности базы данных SqlDb.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ddfa1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ddfa1-110">EXAMPLES</span></span>

### <span data-ttu-id="ddfa1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ddfa1-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ddfa1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddfa1-112">PARAMETERS</span></span>

### <span data-ttu-id="ddfa1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ddfa1-113">-AccountName</span></span>
<span data-ttu-id="ddfa1-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="ddfa1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ddfa1-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ddfa1-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ddfa1-116">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ddfa1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddfa1-117">-Confirm</span></span>
<span data-ttu-id="ddfa1-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddfa1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfa1-119">-DefaultProfile</span></span>
<span data-ttu-id="ddfa1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddfa1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddfa1-121">-InputObject</span></span>
<span data-ttu-id="ddfa1-122">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="ddfa1-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ddfa1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ddfa1-123">-Name</span></span>
<span data-ttu-id="ddfa1-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-124">Database name.</span></span>

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

### <span data-ttu-id="ddfa1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ddfa1-125">-ParentObject</span></span>
<span data-ttu-id="ddfa1-126">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="ddfa1-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ddfa1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddfa1-127">-ResourceGroupName</span></span>
<span data-ttu-id="ddfa1-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ddfa1-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="ddfa1-129">-Throughput</span></span>
<span data-ttu-id="ddfa1-130">Пропускная способность SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ddfa1-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="ddfa1-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-131">Default value is 400.</span></span>

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

### <span data-ttu-id="ddfa1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddfa1-132">-WhatIf</span></span>
<span data-ttu-id="ddfa1-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddfa1-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddfa1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfa1-135">CommonParameters</span></span>
<span data-ttu-id="ddfa1-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddfa1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfa1-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddfa1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfa1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddfa1-138">INPUTS</span></span>

### <span data-ttu-id="ddfa1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ddfa1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ddfa1-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ddfa1-140">OUTPUTS</span></span>

### <span data-ttu-id="ddfa1-141">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ddfa1-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ddfa1-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ddfa1-142">NOTES</span></span>

## <span data-ttu-id="ddfa1-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddfa1-143">RELATED LINKS</span></span>
