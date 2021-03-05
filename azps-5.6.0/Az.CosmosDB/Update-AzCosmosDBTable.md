---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: 3463a07219375db06495bd5d50a2fe3b5916e173
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009683"
---
# <span data-ttu-id="826d7-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="826d7-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="826d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="826d7-102">SYNOPSIS</span></span>
<span data-ttu-id="826d7-103">Обновляет таблицу "Приобр".</span><span class="sxs-lookup"><span data-stu-id="826d7-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="826d7-104">Выполняет клиентскую операцию исправления, читая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="826d7-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="826d7-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="826d7-105">SYNTAX</span></span>

### <span data-ttu-id="826d7-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="826d7-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="826d7-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="826d7-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="826d7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="826d7-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="826d7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="826d7-109">DESCRIPTION</span></span>
<span data-ttu-id="826d7-110">Обновляет таблицу "Приобр".</span><span class="sxs-lookup"><span data-stu-id="826d7-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="826d7-111">Выполняет клиентскую операцию исправления, читая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="826d7-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="826d7-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="826d7-112">EXAMPLES</span></span>

### <span data-ttu-id="826d7-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="826d7-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="826d7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="826d7-114">PARAMETERS</span></span>

### <span data-ttu-id="826d7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="826d7-115">-AccountName</span></span>
<span data-ttu-id="826d7-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="826d7-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="826d7-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="826d7-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="826d7-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="826d7-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="826d7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="826d7-119">-Confirm</span></span>
<span data-ttu-id="826d7-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="826d7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="826d7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="826d7-121">-DefaultProfile</span></span>
<span data-ttu-id="826d7-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="826d7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="826d7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="826d7-123">-InputObject</span></span>
<span data-ttu-id="826d7-124">Объект Table.</span><span class="sxs-lookup"><span data-stu-id="826d7-124">Table Object.</span></span>

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

### <span data-ttu-id="826d7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="826d7-125">-Name</span></span>
<span data-ttu-id="826d7-126">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="826d7-126">Name of the Table.</span></span>

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

### <span data-ttu-id="826d7-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="826d7-127">-ParentObject</span></span>
<span data-ttu-id="826d7-128">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="826d7-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="826d7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="826d7-129">-ResourceGroupName</span></span>
<span data-ttu-id="826d7-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="826d7-130">Name of resource group.</span></span>

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

### <span data-ttu-id="826d7-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="826d7-131">-Throughput</span></span>
<span data-ttu-id="826d7-132">Пропускная способность таблицы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="826d7-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="826d7-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="826d7-133">Default value is 400.</span></span>

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

### <span data-ttu-id="826d7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="826d7-134">-WhatIf</span></span>
<span data-ttu-id="826d7-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="826d7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="826d7-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="826d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="826d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="826d7-137">CommonParameters</span></span>
<span data-ttu-id="826d7-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="826d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="826d7-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="826d7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="826d7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="826d7-140">INPUTS</span></span>

### <span data-ttu-id="826d7-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="826d7-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="826d7-142">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="826d7-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="826d7-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="826d7-143">OUTPUTS</span></span>

### <span data-ttu-id="826d7-144">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="826d7-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="826d7-145">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="826d7-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="826d7-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="826d7-146">NOTES</span></span>

## <span data-ttu-id="826d7-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="826d7-147">RELATED LINKS</span></span>
