---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418140"
---
# <span data-ttu-id="60bb3-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="60bb3-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="60bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="60bb3-103">Обновляет таблицу "Приобр".</span><span class="sxs-lookup"><span data-stu-id="60bb3-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="60bb3-104">Выполняет клиентскую операцию исправления, читая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="60bb3-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="60bb3-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60bb3-105">SYNTAX</span></span>

### <span data-ttu-id="60bb3-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60bb3-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60bb3-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60bb3-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60bb3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60bb3-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60bb3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60bb3-109">DESCRIPTION</span></span>
<span data-ttu-id="60bb3-110">Обновляет таблицу "Приобр".</span><span class="sxs-lookup"><span data-stu-id="60bb3-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="60bb3-111">Выполняет клиентскую операцию исправления, читая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="60bb3-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="60bb3-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60bb3-112">EXAMPLES</span></span>

### <span data-ttu-id="60bb3-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60bb3-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="60bb3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60bb3-114">PARAMETERS</span></span>

### <span data-ttu-id="60bb3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="60bb3-115">-AccountName</span></span>
<span data-ttu-id="60bb3-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="60bb3-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="60bb3-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="60bb3-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="60bb3-118">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="60bb3-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="60bb3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60bb3-119">-Confirm</span></span>
<span data-ttu-id="60bb3-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60bb3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60bb3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60bb3-121">-DefaultProfile</span></span>
<span data-ttu-id="60bb3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60bb3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60bb3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60bb3-123">-InputObject</span></span>
<span data-ttu-id="60bb3-124">Объект Table.</span><span class="sxs-lookup"><span data-stu-id="60bb3-124">Table Object.</span></span>

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

### <span data-ttu-id="60bb3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="60bb3-125">-Name</span></span>
<span data-ttu-id="60bb3-126">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="60bb3-126">Name of the Table.</span></span>

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

### <span data-ttu-id="60bb3-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="60bb3-127">-ParentObject</span></span>
<span data-ttu-id="60bb3-128">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="60bb3-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="60bb3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60bb3-129">-ResourceGroupName</span></span>
<span data-ttu-id="60bb3-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60bb3-130">Name of resource group.</span></span>

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

### <span data-ttu-id="60bb3-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="60bb3-131">-Throughput</span></span>
<span data-ttu-id="60bb3-132">Пропускная способность таблицы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="60bb3-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="60bb3-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="60bb3-133">Default value is 400.</span></span>

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

### <span data-ttu-id="60bb3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60bb3-134">-WhatIf</span></span>
<span data-ttu-id="60bb3-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60bb3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60bb3-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="60bb3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60bb3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60bb3-137">CommonParameters</span></span>
<span data-ttu-id="60bb3-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60bb3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60bb3-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60bb3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60bb3-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60bb3-140">INPUTS</span></span>

### <span data-ttu-id="60bb3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="60bb3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="60bb3-142">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="60bb3-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="60bb3-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60bb3-143">OUTPUTS</span></span>

### <span data-ttu-id="60bb3-144">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="60bb3-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="60bb3-145">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="60bb3-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="60bb3-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60bb3-146">NOTES</span></span>

## <span data-ttu-id="60bb3-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60bb3-147">RELATED LINKS</span></span>
