---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: e38e10765bc9a9768efaf1598a1865ec985b376c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066655"
---
# <span data-ttu-id="63943-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="63943-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="63943-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63943-102">SYNOPSIS</span></span>
<span data-ttu-id="63943-103">Обновляет значение пропускной способности контейнера CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="63943-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="63943-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63943-104">SYNTAX</span></span>

### <span data-ttu-id="63943-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63943-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63943-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63943-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63943-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63943-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63943-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63943-108">EXAMPLES</span></span>

### <span data-ttu-id="63943-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63943-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="63943-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63943-110">PARAMETERS</span></span>

### <span data-ttu-id="63943-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="63943-111">-AccountName</span></span>
<span data-ttu-id="63943-112">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="63943-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="63943-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63943-113">-Confirm</span></span>
<span data-ttu-id="63943-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63943-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63943-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63943-115">-DatabaseName</span></span>
<span data-ttu-id="63943-116">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="63943-116">Database name.</span></span>

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

### <span data-ttu-id="63943-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63943-117">-DefaultProfile</span></span>
<span data-ttu-id="63943-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63943-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63943-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63943-119">-InputObject</span></span>
<span data-ttu-id="63943-120">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="63943-120">Sql Database object.</span></span>

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

### <span data-ttu-id="63943-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63943-121">-Name</span></span>
<span data-ttu-id="63943-122">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="63943-122">Container name.</span></span>

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

### <span data-ttu-id="63943-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="63943-123">-ParentObject</span></span>
<span data-ttu-id="63943-124">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="63943-124">Sql Database object.</span></span>

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

### <span data-ttu-id="63943-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63943-125">-ResourceGroupName</span></span>
<span data-ttu-id="63943-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63943-126">Name of resource group.</span></span>

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

### <span data-ttu-id="63943-127">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="63943-127">-Throughput</span></span>
<span data-ttu-id="63943-128">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="63943-128">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="63943-129">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="63943-129">Default value is 400.</span></span>

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

### <span data-ttu-id="63943-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63943-130">-WhatIf</span></span>
<span data-ttu-id="63943-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63943-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63943-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63943-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63943-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63943-133">CommonParameters</span></span>
<span data-ttu-id="63943-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63943-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63943-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63943-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63943-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63943-136">INPUTS</span></span>

### <span data-ttu-id="63943-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="63943-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="63943-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63943-138">OUTPUTS</span></span>

### <span data-ttu-id="63943-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="63943-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="63943-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="63943-140">NOTES</span></span>

## <span data-ttu-id="63943-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63943-141">RELATED LINKS</span></span>
