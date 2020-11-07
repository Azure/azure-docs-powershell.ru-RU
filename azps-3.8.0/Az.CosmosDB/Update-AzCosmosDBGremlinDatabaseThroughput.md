---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 75ea7849424d8587f4eb4151bde63f31ea35676f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913040"
---
# <span data-ttu-id="ee775-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ee775-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="ee775-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee775-102">SYNOPSIS</span></span>
<span data-ttu-id="ee775-103">Обновляет значение пропускной способности CosmosDB базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ee775-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="ee775-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee775-104">SYNTAX</span></span>

### <span data-ttu-id="ee775-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee775-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee775-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee775-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee775-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee775-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee775-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee775-108">EXAMPLES</span></span>

### <span data-ttu-id="ee775-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee775-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ee775-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee775-110">PARAMETERS</span></span>

### <span data-ttu-id="ee775-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ee775-111">-AccountName</span></span>
<span data-ttu-id="ee775-112">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ee775-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ee775-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee775-113">-Confirm</span></span>
<span data-ttu-id="ee775-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee775-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee775-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee775-115">-DefaultProfile</span></span>
<span data-ttu-id="ee775-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee775-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee775-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee775-117">-InputObject</span></span>
<span data-ttu-id="ee775-118">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ee775-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ee775-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee775-119">-Name</span></span>
<span data-ttu-id="ee775-120">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ee775-120">Database name.</span></span>

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

### <span data-ttu-id="ee775-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ee775-121">-ParentObject</span></span>
<span data-ttu-id="ee775-122">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ee775-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee775-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee775-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee775-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee775-124">Name of resource group.</span></span>

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

### <span data-ttu-id="ee775-125">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="ee775-125">-Throughput</span></span>
<span data-ttu-id="ee775-126">Пропускная способность Gremlin базы данных (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ee775-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="ee775-127">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="ee775-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee775-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee775-128">-WhatIf</span></span>
<span data-ttu-id="ee775-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee775-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee775-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee775-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee775-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee775-131">CommonParameters</span></span>
<span data-ttu-id="ee775-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee775-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee775-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee775-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee775-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee775-134">INPUTS</span></span>

### <span data-ttu-id="ee775-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ee775-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ee775-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee775-136">OUTPUTS</span></span>

### <span data-ttu-id="ee775-137">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ee775-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ee775-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee775-138">NOTES</span></span>

## <span data-ttu-id="ee775-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee775-139">RELATED LINKS</span></span>
