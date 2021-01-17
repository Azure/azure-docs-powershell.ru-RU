---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 324350329b166ab3a41f7e2bd8b59af1b9efdcb7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418180"
---
# <span data-ttu-id="ba951-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ba951-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="ba951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba951-102">SYNOPSIS</span></span>
<span data-ttu-id="ba951-103">Обновляет значение пропускной способности для базы данных SqlDb.</span><span class="sxs-lookup"><span data-stu-id="ba951-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ba951-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba951-104">SYNTAX</span></span>

### <span data-ttu-id="ba951-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba951-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba951-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba951-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba951-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba951-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba951-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba951-108">DESCRIPTION</span></span>
<span data-ttu-id="ba951-109">Обновляет значение пропускной способности для базы данных SqlDb.</span><span class="sxs-lookup"><span data-stu-id="ba951-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ba951-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba951-110">EXAMPLES</span></span>

### <span data-ttu-id="ba951-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba951-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ba951-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba951-112">PARAMETERS</span></span>

### <span data-ttu-id="ba951-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ba951-113">-AccountName</span></span>
<span data-ttu-id="ba951-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="ba951-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ba951-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ba951-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ba951-116">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="ba951-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ba951-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba951-117">-Confirm</span></span>
<span data-ttu-id="ba951-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba951-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba951-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba951-119">-DefaultProfile</span></span>
<span data-ttu-id="ba951-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba951-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba951-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba951-121">-InputObject</span></span>
<span data-ttu-id="ba951-122">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="ba951-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ba951-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ba951-123">-Name</span></span>
<span data-ttu-id="ba951-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ba951-124">Database name.</span></span>

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

### <span data-ttu-id="ba951-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ba951-125">-ParentObject</span></span>
<span data-ttu-id="ba951-126">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="ba951-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ba951-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba951-127">-ResourceGroupName</span></span>
<span data-ttu-id="ba951-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba951-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ba951-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="ba951-129">-Throughput</span></span>
<span data-ttu-id="ba951-130">Пропускная способность SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ba951-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="ba951-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="ba951-131">Default value is 400.</span></span>

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

### <span data-ttu-id="ba951-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba951-132">-WhatIf</span></span>
<span data-ttu-id="ba951-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba951-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba951-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ba951-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba951-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba951-135">CommonParameters</span></span>
<span data-ttu-id="ba951-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba951-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba951-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba951-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba951-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba951-138">INPUTS</span></span>

### <span data-ttu-id="ba951-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ba951-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ba951-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba951-140">OUTPUTS</span></span>

### <span data-ttu-id="ba951-141">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ba951-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ba951-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba951-142">NOTES</span></span>

## <span data-ttu-id="ba951-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba951-143">RELATED LINKS</span></span>
