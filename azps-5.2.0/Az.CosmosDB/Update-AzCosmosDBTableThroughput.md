---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418143"
---
# <span data-ttu-id="9e370-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="9e370-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="9e370-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e370-102">SYNOPSIS</span></span>
<span data-ttu-id="9e370-103">Обновляет значение пропускной способности таблицы ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="9e370-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="9e370-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e370-104">SYNTAX</span></span>

### <span data-ttu-id="9e370-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e370-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e370-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e370-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e370-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e370-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e370-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e370-108">DESCRIPTION</span></span>
<span data-ttu-id="9e370-109">Обновляет значение пропускной способности таблицы ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="9e370-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="9e370-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e370-110">EXAMPLES</span></span>

### <span data-ttu-id="9e370-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e370-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="9e370-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e370-112">PARAMETERS</span></span>

### <span data-ttu-id="9e370-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9e370-113">-AccountName</span></span>
<span data-ttu-id="9e370-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="9e370-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9e370-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9e370-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9e370-116">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="9e370-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9e370-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e370-117">-Confirm</span></span>
<span data-ttu-id="9e370-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9e370-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e370-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e370-119">-DefaultProfile</span></span>
<span data-ttu-id="9e370-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e370-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e370-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e370-121">-InputObject</span></span>
<span data-ttu-id="9e370-122">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="9e370-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9e370-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9e370-123">-Name</span></span>
<span data-ttu-id="9e370-124">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e370-124">Name of the Table.</span></span>

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

### <span data-ttu-id="9e370-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9e370-125">-ParentObject</span></span>
<span data-ttu-id="9e370-126">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="9e370-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9e370-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e370-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e370-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e370-128">Name of resource group.</span></span>

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

### <span data-ttu-id="9e370-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="9e370-129">-Throughput</span></span>
<span data-ttu-id="9e370-130">Пропускная способность таблицы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9e370-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="9e370-131">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="9e370-131">Default value is 400.</span></span>

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

### <span data-ttu-id="9e370-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e370-132">-WhatIf</span></span>
<span data-ttu-id="9e370-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e370-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e370-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9e370-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e370-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e370-135">CommonParameters</span></span>
<span data-ttu-id="9e370-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e370-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e370-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e370-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e370-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e370-138">INPUTS</span></span>

### <span data-ttu-id="9e370-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9e370-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9e370-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e370-140">OUTPUTS</span></span>

### <span data-ttu-id="9e370-141">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9e370-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9e370-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e370-142">NOTES</span></span>

## <span data-ttu-id="9e370-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e370-143">RELATED LINKS</span></span>
