---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 478e1458f68a0f7c385d24e3cd1cfc6f149dbfc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314522"
---
# <span data-ttu-id="772a5-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="772a5-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="772a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="772a5-102">SYNOPSIS</span></span>
<span data-ttu-id="772a5-103">Обновляет значение пропускной способности контейнера CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="772a5-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="772a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="772a5-104">SYNTAX</span></span>

### <span data-ttu-id="772a5-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="772a5-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="772a5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="772a5-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="772a5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="772a5-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="772a5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="772a5-108">DESCRIPTION</span></span>
<span data-ttu-id="772a5-109">Обновляет значение пропускной способности контейнера CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="772a5-109">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="772a5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="772a5-110">EXAMPLES</span></span>

### <span data-ttu-id="772a5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="772a5-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

### <span data-ttu-id="772a5-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="772a5-112">Example 2</span></span>

<span data-ttu-id="772a5-113">Обновляет значение пропускной способности контейнера CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="772a5-113">Updates the throughput value of a CosmosDB Sql Container.</span></span> <span data-ttu-id="772a5-114">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="772a5-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
Update-AzCosmosDBSqlContainerThroughput -AccountName myAccountName -AutoscaleMaxThroughput <Int32> -DatabaseName myDatabaseName -Name dbname -ResourceGroupName rg1
```

## <span data-ttu-id="772a5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="772a5-115">PARAMETERS</span></span>

### <span data-ttu-id="772a5-116">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="772a5-116">-AccountName</span></span>
<span data-ttu-id="772a5-117">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="772a5-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="772a5-118">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="772a5-118">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="772a5-119">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="772a5-119">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="772a5-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="772a5-120">-Confirm</span></span>
<span data-ttu-id="772a5-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="772a5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="772a5-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="772a5-122">-DatabaseName</span></span>
<span data-ttu-id="772a5-123">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="772a5-123">Database name.</span></span>

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

### <span data-ttu-id="772a5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772a5-124">-DefaultProfile</span></span>
<span data-ttu-id="772a5-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="772a5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="772a5-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="772a5-126">-InputObject</span></span>
<span data-ttu-id="772a5-127">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="772a5-127">Sql Database object.</span></span>

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

### <span data-ttu-id="772a5-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="772a5-128">-Name</span></span>
<span data-ttu-id="772a5-129">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="772a5-129">Container name.</span></span>

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

### <span data-ttu-id="772a5-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="772a5-130">-ParentObject</span></span>
<span data-ttu-id="772a5-131">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="772a5-131">Sql Database object.</span></span>

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

### <span data-ttu-id="772a5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="772a5-132">-ResourceGroupName</span></span>
<span data-ttu-id="772a5-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="772a5-133">Name of resource group.</span></span>

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

### <span data-ttu-id="772a5-134">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="772a5-134">-Throughput</span></span>
<span data-ttu-id="772a5-135">Пропускная способность контейнера SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="772a5-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="772a5-136">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="772a5-136">Default value is 400.</span></span>

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

### <span data-ttu-id="772a5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="772a5-137">-WhatIf</span></span>
<span data-ttu-id="772a5-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="772a5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="772a5-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="772a5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="772a5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772a5-140">CommonParameters</span></span>
<span data-ttu-id="772a5-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="772a5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772a5-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="772a5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772a5-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="772a5-143">INPUTS</span></span>

### <span data-ttu-id="772a5-144">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="772a5-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="772a5-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="772a5-145">OUTPUTS</span></span>

### <span data-ttu-id="772a5-146">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="772a5-146">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="772a5-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="772a5-147">NOTES</span></span>

## <span data-ttu-id="772a5-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="772a5-148">RELATED LINKS</span></span>