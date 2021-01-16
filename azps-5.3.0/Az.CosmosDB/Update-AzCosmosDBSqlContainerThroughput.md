---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 478e1458f68a0f7c385d24e3cd1cfc6f149dbfc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508713"
---
# <span data-ttu-id="943e9-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="943e9-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="943e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="943e9-102">SYNOPSIS</span></span>
<span data-ttu-id="943e9-103">Обновляет значение пропускной способности контейнера Sql Container для БазсDB.</span><span class="sxs-lookup"><span data-stu-id="943e9-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="943e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="943e9-104">SYNTAX</span></span>

### <span data-ttu-id="943e9-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="943e9-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="943e9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="943e9-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="943e9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="943e9-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="943e9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="943e9-108">DESCRIPTION</span></span>
<span data-ttu-id="943e9-109">Обновляет значение пропускной способности контейнера Sql Container для БазсDB.</span><span class="sxs-lookup"><span data-stu-id="943e9-109">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="943e9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="943e9-110">EXAMPLES</span></span>

### <span data-ttu-id="943e9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="943e9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

### <span data-ttu-id="943e9-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="943e9-112">Example 2</span></span>

<span data-ttu-id="943e9-113">Обновляет значение пропускной способности контейнера Sql Container для БазсDB.</span><span class="sxs-lookup"><span data-stu-id="943e9-113">Updates the throughput value of a CosmosDB Sql Container.</span></span> <span data-ttu-id="943e9-114">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="943e9-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
Update-AzCosmosDBSqlContainerThroughput -AccountName myAccountName -AutoscaleMaxThroughput <Int32> -DatabaseName myDatabaseName -Name dbname -ResourceGroupName rg1
```

## <span data-ttu-id="943e9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="943e9-115">PARAMETERS</span></span>

### <span data-ttu-id="943e9-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="943e9-116">-AccountName</span></span>
<span data-ttu-id="943e9-117">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="943e9-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="943e9-118">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="943e9-118">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="943e9-119">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="943e9-119">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="943e9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="943e9-120">-Confirm</span></span>
<span data-ttu-id="943e9-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="943e9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="943e9-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="943e9-122">-DatabaseName</span></span>
<span data-ttu-id="943e9-123">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="943e9-123">Database name.</span></span>

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

### <span data-ttu-id="943e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="943e9-124">-DefaultProfile</span></span>
<span data-ttu-id="943e9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="943e9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="943e9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="943e9-126">-InputObject</span></span>
<span data-ttu-id="943e9-127">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="943e9-127">Sql Database object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="943e9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="943e9-128">-Name</span></span>
<span data-ttu-id="943e9-129">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="943e9-129">Container name.</span></span>

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

### <span data-ttu-id="943e9-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="943e9-130">-ParentObject</span></span>
<span data-ttu-id="943e9-131">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="943e9-131">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="943e9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="943e9-132">-ResourceGroupName</span></span>
<span data-ttu-id="943e9-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="943e9-133">Name of resource group.</span></span>

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

### <span data-ttu-id="943e9-134">-Throughput</span><span class="sxs-lookup"><span data-stu-id="943e9-134">-Throughput</span></span>
<span data-ttu-id="943e9-135">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="943e9-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="943e9-136">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="943e9-136">Default value is 400.</span></span>

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

### <span data-ttu-id="943e9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="943e9-137">-WhatIf</span></span>
<span data-ttu-id="943e9-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="943e9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="943e9-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="943e9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="943e9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943e9-140">CommonParameters</span></span>
<span data-ttu-id="943e9-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="943e9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943e9-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="943e9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943e9-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="943e9-143">INPUTS</span></span>

### <span data-ttu-id="943e9-144">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="943e9-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="943e9-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="943e9-145">OUTPUTS</span></span>

### <span data-ttu-id="943e9-146">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="943e9-146">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="943e9-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="943e9-147">NOTES</span></span>

## <span data-ttu-id="943e9-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="943e9-148">RELATED LINKS</span></span>