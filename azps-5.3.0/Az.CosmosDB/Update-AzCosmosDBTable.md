---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508701"
---
# <span data-ttu-id="b5fb2-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="b5fb2-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="b5fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fb2-103">Обновляет таблицу "Приобр".</span><span class="sxs-lookup"><span data-stu-id="b5fb2-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="b5fb2-104">Выполняет клиентскую операцию исправления на стороне клиента, читая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="b5fb2-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b5fb2-105">SYNTAX</span></span>

### <span data-ttu-id="b5fb2-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5fb2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5fb2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5fb2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5fb2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5fb2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5fb2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5fb2-109">DESCRIPTION</span></span>
<span data-ttu-id="b5fb2-110">Обновляет таблицу "Приобр".</span><span class="sxs-lookup"><span data-stu-id="b5fb2-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="b5fb2-111">Выполняет клиентскую операцию исправления на стороне клиента, читая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="b5fb2-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b5fb2-112">EXAMPLES</span></span>

### <span data-ttu-id="b5fb2-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5fb2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="b5fb2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5fb2-114">PARAMETERS</span></span>

### <span data-ttu-id="b5fb2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b5fb2-115">-AccountName</span></span>
<span data-ttu-id="b5fb2-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="b5fb2-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b5fb2-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b5fb2-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b5fb2-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b5fb2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5fb2-119">-Confirm</span></span>
<span data-ttu-id="b5fb2-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5fb2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fb2-121">-DefaultProfile</span></span>
<span data-ttu-id="b5fb2-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5fb2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5fb2-123">-InputObject</span></span>
<span data-ttu-id="b5fb2-124">Объект Table.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-124">Table Object.</span></span>

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

### <span data-ttu-id="b5fb2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b5fb2-125">-Name</span></span>
<span data-ttu-id="b5fb2-126">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-126">Name of the Table.</span></span>

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

### <span data-ttu-id="b5fb2-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b5fb2-127">-ParentObject</span></span>
<span data-ttu-id="b5fb2-128">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="b5fb2-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b5fb2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5fb2-129">-ResourceGroupName</span></span>
<span data-ttu-id="b5fb2-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b5fb2-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="b5fb2-131">-Throughput</span></span>
<span data-ttu-id="b5fb2-132">Пропускная способность таблицы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b5fb2-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="b5fb2-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-133">Default value is 400.</span></span>

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

### <span data-ttu-id="b5fb2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5fb2-134">-WhatIf</span></span>
<span data-ttu-id="b5fb2-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5fb2-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5fb2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fb2-137">CommonParameters</span></span>
<span data-ttu-id="b5fb2-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5fb2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fb2-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5fb2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fb2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5fb2-140">INPUTS</span></span>

### <span data-ttu-id="b5fb2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b5fb2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="b5fb2-142">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="b5fb2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="b5fb2-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5fb2-143">OUTPUTS</span></span>

### <span data-ttu-id="b5fb2-144">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="b5fb2-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="b5fb2-145">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b5fb2-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b5fb2-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b5fb2-146">NOTES</span></span>

## <span data-ttu-id="b5fb2-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5fb2-147">RELATED LINKS</span></span>
