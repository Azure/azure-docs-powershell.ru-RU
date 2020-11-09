---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314561"
---
# <span data-ttu-id="8b7e0-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="8b7e0-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="8b7e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7e0-103">Обновляет значение пропускной способности CosmosDB базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="8b7e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b7e0-104">SYNTAX</span></span>

### <span data-ttu-id="8b7e0-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b7e0-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b7e0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b7e0-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b7e0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b7e0-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b7e0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b7e0-108">DESCRIPTION</span></span>
<span data-ttu-id="8b7e0-109">Обновляет значение пропускной способности CosmosDB базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="8b7e0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b7e0-110">EXAMPLES</span></span>

### <span data-ttu-id="8b7e0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b7e0-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="8b7e0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b7e0-112">PARAMETERS</span></span>

### <span data-ttu-id="8b7e0-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="8b7e0-113">-AccountName</span></span>
<span data-ttu-id="8b7e0-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8b7e0-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8b7e0-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8b7e0-116">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8b7e0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b7e0-117">-Confirm</span></span>
<span data-ttu-id="8b7e0-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b7e0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7e0-119">-DefaultProfile</span></span>
<span data-ttu-id="8b7e0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b7e0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b7e0-121">-InputObject</span></span>
<span data-ttu-id="8b7e0-122">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8b7e0-122">CosmosDB Account object</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7e0-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b7e0-123">-Name</span></span>
<span data-ttu-id="8b7e0-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-124">Database name.</span></span>

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

### <span data-ttu-id="8b7e0-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8b7e0-125">-ParentObject</span></span>
<span data-ttu-id="8b7e0-126">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8b7e0-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8b7e0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b7e0-127">-ResourceGroupName</span></span>
<span data-ttu-id="8b7e0-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-128">Name of resource group.</span></span>

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

### <span data-ttu-id="8b7e0-129">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="8b7e0-129">-Throughput</span></span>
<span data-ttu-id="8b7e0-130">Пропускная способность Gremlin базы данных (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8b7e0-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="8b7e0-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-131">Default value is 400.</span></span>

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

### <span data-ttu-id="8b7e0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b7e0-132">-WhatIf</span></span>
<span data-ttu-id="8b7e0-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b7e0-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b7e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7e0-135">CommonParameters</span></span>
<span data-ttu-id="8b7e0-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b7e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7e0-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b7e0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7e0-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b7e0-138">INPUTS</span></span>

### <span data-ttu-id="8b7e0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8b7e0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8b7e0-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b7e0-140">OUTPUTS</span></span>

### <span data-ttu-id="8b7e0-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8b7e0-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8b7e0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b7e0-142">NOTES</span></span>

## <span data-ttu-id="8b7e0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b7e0-143">RELATED LINKS</span></span>
