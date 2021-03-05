---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8195179599d98fbc3fd8954361ba142706460886
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012248"
---
# <span data-ttu-id="d0bd2-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d0bd2-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="d0bd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="d0bd2-103">Создает новую базу данных SQLDb.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d0bd2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d0bd2-104">SYNTAX</span></span>

### <span data-ttu-id="d0bd2-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0bd2-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0bd2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bd2-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0bd2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0bd2-107">DESCRIPTION</span></span>
<span data-ttu-id="d0bd2-108">Создает новую базу данных SQLDb.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d0bd2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d0bd2-109">EXAMPLES</span></span>

### <span data-ttu-id="d0bd2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d0bd2-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="d0bd2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0bd2-111">PARAMETERS</span></span>

### <span data-ttu-id="d0bd2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d0bd2-112">-AccountName</span></span>
<span data-ttu-id="d0bd2-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="d0bd2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d0bd2-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d0bd2-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d0bd2-115">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d0bd2-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0bd2-116">-Confirm</span></span>
<span data-ttu-id="d0bd2-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0bd2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0bd2-118">-DefaultProfile</span></span>
<span data-ttu-id="d0bd2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0bd2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d0bd2-120">-Name</span></span>
<span data-ttu-id="d0bd2-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0bd2-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0bd2-122">-ParentObject</span></span>
<span data-ttu-id="d0bd2-123">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="d0bd2-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d0bd2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0bd2-124">-ResourceGroupName</span></span>
<span data-ttu-id="d0bd2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-125">Name of resource group.</span></span>

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

### <span data-ttu-id="d0bd2-126">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="d0bd2-126">-Throughput</span></span>
<span data-ttu-id="d0bd2-127">Пропускная способность SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d0bd2-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="d0bd2-128">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-128">Default value is 400.</span></span>

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

### <span data-ttu-id="d0bd2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0bd2-129">-WhatIf</span></span>
<span data-ttu-id="d0bd2-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0bd2-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0bd2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0bd2-132">CommonParameters</span></span>
<span data-ttu-id="d0bd2-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0bd2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0bd2-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0bd2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0bd2-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0bd2-135">INPUTS</span></span>

### <span data-ttu-id="d0bd2-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d0bd2-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d0bd2-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d0bd2-137">OUTPUTS</span></span>

### <span data-ttu-id="d0bd2-138">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d0bd2-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d0bd2-139">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="d0bd2-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="d0bd2-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d0bd2-140">NOTES</span></span>

## <span data-ttu-id="d0bd2-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0bd2-141">RELATED LINKS</span></span>
