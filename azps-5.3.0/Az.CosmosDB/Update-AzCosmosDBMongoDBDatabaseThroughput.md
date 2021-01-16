---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1948bc5b5488c951861509c9b3c9ee7815eddec9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508714"
---
# <span data-ttu-id="6f54e-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="6f54e-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="6f54e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f54e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f54e-103">Обновляет значение пропускной способности базы данных ВайсDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="6f54e-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="6f54e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f54e-104">SYNTAX</span></span>

### <span data-ttu-id="6f54e-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f54e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f54e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f54e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f54e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f54e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f54e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f54e-108">DESCRIPTION</span></span>
<span data-ttu-id="6f54e-109">Обновляет значение пропускной способности базы данных ВайссDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="6f54e-109">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="6f54e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f54e-110">EXAMPLES</span></span>

### <span data-ttu-id="6f54e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f54e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="6f54e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f54e-112">PARAMETERS</span></span>

### <span data-ttu-id="6f54e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6f54e-113">-AccountName</span></span>
<span data-ttu-id="6f54e-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="6f54e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6f54e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="6f54e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6f54e-116">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="6f54e-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="6f54e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f54e-117">-Confirm</span></span>
<span data-ttu-id="6f54e-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f54e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f54e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f54e-119">-DefaultProfile</span></span>
<span data-ttu-id="6f54e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f54e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f54e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f54e-121">-InputObject</span></span>
<span data-ttu-id="6f54e-122">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="6f54e-122">CosmosDB Account object</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f54e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6f54e-123">-Name</span></span>
<span data-ttu-id="6f54e-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="6f54e-124">Database name.</span></span>

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

### <span data-ttu-id="6f54e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6f54e-125">-ParentObject</span></span>
<span data-ttu-id="6f54e-126">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="6f54e-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6f54e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f54e-127">-ResourceGroupName</span></span>
<span data-ttu-id="6f54e-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f54e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="6f54e-129">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="6f54e-129">-Throughput</span></span>
<span data-ttu-id="6f54e-130">Пропускная способность базы данных Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="6f54e-130">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="6f54e-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="6f54e-131">Default value is 400.</span></span>

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

### <span data-ttu-id="6f54e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f54e-132">-WhatIf</span></span>
<span data-ttu-id="6f54e-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f54e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f54e-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6f54e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f54e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f54e-135">CommonParameters</span></span>
<span data-ttu-id="6f54e-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f54e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f54e-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f54e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f54e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f54e-138">INPUTS</span></span>

### <span data-ttu-id="6f54e-139">Нет</span><span class="sxs-lookup"><span data-stu-id="6f54e-139">None</span></span>

## <span data-ttu-id="6f54e-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f54e-140">OUTPUTS</span></span>

### <span data-ttu-id="6f54e-141">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6f54e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6f54e-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f54e-142">NOTES</span></span>

## <span data-ttu-id="6f54e-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f54e-143">RELATED LINKS</span></span>
