---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: d90df542fd2acc925531f4bf9da7244ea1831a63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066652"
---
# <span data-ttu-id="26e9a-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="26e9a-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="26e9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="26e9a-103">Обновляет значение пропускной способности CosmosDB базы данных MongoDB.</span><span class="sxs-lookup"><span data-stu-id="26e9a-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="26e9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26e9a-104">SYNTAX</span></span>

### <span data-ttu-id="26e9a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26e9a-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e9a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e9a-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26e9a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e9a-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26e9a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26e9a-108">EXAMPLES</span></span>

### <span data-ttu-id="26e9a-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26e9a-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="26e9a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26e9a-110">PARAMETERS</span></span>

### <span data-ttu-id="26e9a-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="26e9a-111">-AccountName</span></span>
<span data-ttu-id="26e9a-112">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="26e9a-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26e9a-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26e9a-113">-Confirm</span></span>
<span data-ttu-id="26e9a-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26e9a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e9a-115">-DefaultProfile</span></span>
<span data-ttu-id="26e9a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26e9a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e9a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26e9a-117">-InputObject</span></span>
<span data-ttu-id="26e9a-118">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="26e9a-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="26e9a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26e9a-119">-Name</span></span>
<span data-ttu-id="26e9a-120">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="26e9a-120">Database name.</span></span>

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

### <span data-ttu-id="26e9a-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="26e9a-121">-ParentObject</span></span>
<span data-ttu-id="26e9a-122">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="26e9a-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e9a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e9a-123">-ResourceGroupName</span></span>
<span data-ttu-id="26e9a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26e9a-124">Name of resource group.</span></span>

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

### <span data-ttu-id="26e9a-125">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="26e9a-125">-Throughput</span></span>
<span data-ttu-id="26e9a-126">Пропускная способность Mongo базы данных (RU/s).</span><span class="sxs-lookup"><span data-stu-id="26e9a-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="26e9a-127">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="26e9a-127">Default value is 400.</span></span>

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

### <span data-ttu-id="26e9a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e9a-128">-WhatIf</span></span>
<span data-ttu-id="26e9a-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26e9a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e9a-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26e9a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e9a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e9a-131">CommonParameters</span></span>
<span data-ttu-id="26e9a-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26e9a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e9a-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26e9a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e9a-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26e9a-134">INPUTS</span></span>

### <span data-ttu-id="26e9a-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="26e9a-135">None</span></span>

## <span data-ttu-id="26e9a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26e9a-136">OUTPUTS</span></span>

### <span data-ttu-id="26e9a-137">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="26e9a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="26e9a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="26e9a-138">NOTES</span></span>

## <span data-ttu-id="26e9a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26e9a-139">RELATED LINKS</span></span>
