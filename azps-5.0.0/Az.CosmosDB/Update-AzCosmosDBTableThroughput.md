---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314474"
---
# <span data-ttu-id="e097e-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="e097e-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="e097e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e097e-102">SYNOPSIS</span></span>
<span data-ttu-id="e097e-103">Обновляет значение пропускной способности таблицы CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e097e-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="e097e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e097e-104">SYNTAX</span></span>

### <span data-ttu-id="e097e-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e097e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e097e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e097e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e097e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e097e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e097e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e097e-108">DESCRIPTION</span></span>
<span data-ttu-id="e097e-109">Обновляет значение пропускной способности таблицы CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e097e-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="e097e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e097e-110">EXAMPLES</span></span>

### <span data-ttu-id="e097e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e097e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="e097e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e097e-112">PARAMETERS</span></span>

### <span data-ttu-id="e097e-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e097e-113">-AccountName</span></span>
<span data-ttu-id="e097e-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e097e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e097e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e097e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e097e-116">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="e097e-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e097e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e097e-117">-Confirm</span></span>
<span data-ttu-id="e097e-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e097e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e097e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e097e-119">-DefaultProfile</span></span>
<span data-ttu-id="e097e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e097e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e097e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e097e-121">-InputObject</span></span>
<span data-ttu-id="e097e-122">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e097e-122">CosmosDB Account object</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e097e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e097e-123">-Name</span></span>
<span data-ttu-id="e097e-124">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="e097e-124">Name of the Table.</span></span>

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

### <span data-ttu-id="e097e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e097e-125">-ParentObject</span></span>
<span data-ttu-id="e097e-126">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e097e-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e097e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e097e-127">-ResourceGroupName</span></span>
<span data-ttu-id="e097e-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e097e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e097e-129">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="e097e-129">-Throughput</span></span>
<span data-ttu-id="e097e-130">Пропускная способность таблицы (RU/с).</span><span class="sxs-lookup"><span data-stu-id="e097e-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="e097e-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="e097e-131">Default value is 400.</span></span>

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

### <span data-ttu-id="e097e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e097e-132">-WhatIf</span></span>
<span data-ttu-id="e097e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e097e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e097e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e097e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e097e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e097e-135">CommonParameters</span></span>
<span data-ttu-id="e097e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e097e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e097e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e097e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e097e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e097e-138">INPUTS</span></span>

### <span data-ttu-id="e097e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e097e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e097e-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e097e-140">OUTPUTS</span></span>

### <span data-ttu-id="e097e-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e097e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e097e-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e097e-142">NOTES</span></span>

## <span data-ttu-id="e097e-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e097e-143">RELATED LINKS</span></span>
