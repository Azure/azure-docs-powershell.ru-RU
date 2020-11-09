---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314477"
---
# <span data-ttu-id="1fcf7-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="1fcf7-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="1fcf7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fcf7-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcf7-103">Обновляет таблицу CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="1fcf7-104">Выполняет операцию исправления на стороне клиента, считывая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1fcf7-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fcf7-105">SYNTAX</span></span>

### <span data-ttu-id="1fcf7-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fcf7-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fcf7-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fcf7-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fcf7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fcf7-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1fcf7-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fcf7-109">DESCRIPTION</span></span>
<span data-ttu-id="1fcf7-110">Обновляет таблицу CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="1fcf7-111">Выполняет операцию исправления на стороне клиента, считывая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1fcf7-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fcf7-112">EXAMPLES</span></span>

### <span data-ttu-id="1fcf7-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fcf7-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="1fcf7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fcf7-114">PARAMETERS</span></span>

### <span data-ttu-id="1fcf7-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="1fcf7-115">-AccountName</span></span>
<span data-ttu-id="1fcf7-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1fcf7-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1fcf7-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1fcf7-118">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1fcf7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fcf7-119">-Confirm</span></span>
<span data-ttu-id="1fcf7-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fcf7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcf7-121">-DefaultProfile</span></span>
<span data-ttu-id="1fcf7-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fcf7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fcf7-123">-InputObject</span></span>
<span data-ttu-id="1fcf7-124">Объект Table.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-124">Table Object.</span></span>

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

### <span data-ttu-id="1fcf7-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fcf7-125">-Name</span></span>
<span data-ttu-id="1fcf7-126">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-126">Name of the Table.</span></span>

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

### <span data-ttu-id="1fcf7-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1fcf7-127">-ParentObject</span></span>
<span data-ttu-id="1fcf7-128">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1fcf7-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1fcf7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcf7-129">-ResourceGroupName</span></span>
<span data-ttu-id="1fcf7-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-130">Name of resource group.</span></span>

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

### <span data-ttu-id="1fcf7-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="1fcf7-131">-Throughput</span></span>
<span data-ttu-id="1fcf7-132">Пропускная способность таблицы (RU/с).</span><span class="sxs-lookup"><span data-stu-id="1fcf7-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="1fcf7-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-133">Default value is 400.</span></span>

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

### <span data-ttu-id="1fcf7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcf7-134">-WhatIf</span></span>
<span data-ttu-id="1fcf7-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fcf7-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fcf7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcf7-137">CommonParameters</span></span>
<span data-ttu-id="1fcf7-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fcf7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcf7-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fcf7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcf7-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fcf7-140">INPUTS</span></span>

### <span data-ttu-id="1fcf7-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1fcf7-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="1fcf7-142">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1fcf7-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="1fcf7-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fcf7-143">OUTPUTS</span></span>

### <span data-ttu-id="1fcf7-144">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1fcf7-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="1fcf7-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1fcf7-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1fcf7-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fcf7-146">NOTES</span></span>

## <span data-ttu-id="1fcf7-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fcf7-147">RELATED LINKS</span></span>
