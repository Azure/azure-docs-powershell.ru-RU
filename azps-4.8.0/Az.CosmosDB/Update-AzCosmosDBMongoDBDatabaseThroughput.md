---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1948bc5b5488c951861509c9b3c9ee7815eddec9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078365"
---
# <span data-ttu-id="dc78a-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="dc78a-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="dc78a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc78a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc78a-103">Обновляет значение пропускной способности CosmosDB базы данных MongoDB.</span><span class="sxs-lookup"><span data-stu-id="dc78a-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="dc78a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc78a-104">SYNTAX</span></span>

### <span data-ttu-id="dc78a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc78a-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc78a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc78a-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc78a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc78a-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc78a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc78a-108">DESCRIPTION</span></span>
<span data-ttu-id="dc78a-109">Обновляет значение пропускной способности CosmosDB базы данных MongoDB.</span><span class="sxs-lookup"><span data-stu-id="dc78a-109">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="dc78a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc78a-110">EXAMPLES</span></span>

### <span data-ttu-id="dc78a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc78a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="dc78a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc78a-112">PARAMETERS</span></span>

### <span data-ttu-id="dc78a-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="dc78a-113">-AccountName</span></span>
<span data-ttu-id="dc78a-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="dc78a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dc78a-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="dc78a-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="dc78a-116">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="dc78a-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="dc78a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc78a-117">-Confirm</span></span>
<span data-ttu-id="dc78a-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc78a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc78a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc78a-119">-DefaultProfile</span></span>
<span data-ttu-id="dc78a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc78a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc78a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc78a-121">-InputObject</span></span>
<span data-ttu-id="dc78a-122">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="dc78a-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="dc78a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc78a-123">-Name</span></span>
<span data-ttu-id="dc78a-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="dc78a-124">Database name.</span></span>

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

### <span data-ttu-id="dc78a-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dc78a-125">-ParentObject</span></span>
<span data-ttu-id="dc78a-126">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="dc78a-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="dc78a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc78a-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc78a-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc78a-128">Name of resource group.</span></span>

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

### <span data-ttu-id="dc78a-129">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="dc78a-129">-Throughput</span></span>
<span data-ttu-id="dc78a-130">Пропускная способность Mongo базы данных (RU/s).</span><span class="sxs-lookup"><span data-stu-id="dc78a-130">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="dc78a-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="dc78a-131">Default value is 400.</span></span>

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

### <span data-ttu-id="dc78a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc78a-132">-WhatIf</span></span>
<span data-ttu-id="dc78a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc78a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc78a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc78a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc78a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc78a-135">CommonParameters</span></span>
<span data-ttu-id="dc78a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc78a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc78a-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc78a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc78a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc78a-138">INPUTS</span></span>

### <span data-ttu-id="dc78a-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="dc78a-139">None</span></span>

## <span data-ttu-id="dc78a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc78a-140">OUTPUTS</span></span>

### <span data-ttu-id="dc78a-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dc78a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dc78a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc78a-142">NOTES</span></span>

## <span data-ttu-id="dc78a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc78a-143">RELATED LINKS</span></span>
