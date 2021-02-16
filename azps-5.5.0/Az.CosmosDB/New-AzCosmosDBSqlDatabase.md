---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 2953da3747404c0b6b98992cc8a8b80573da5129
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243928"
---
# <span data-ttu-id="0f817-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0f817-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="0f817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f817-102">SYNOPSIS</span></span>
<span data-ttu-id="0f817-103">Создает новую базу данных SQLDb.</span><span class="sxs-lookup"><span data-stu-id="0f817-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="0f817-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0f817-104">SYNTAX</span></span>

### <span data-ttu-id="0f817-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f817-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f817-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f817-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f817-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f817-107">DESCRIPTION</span></span>
<span data-ttu-id="0f817-108">Создает новую базу данных SQLDb.</span><span class="sxs-lookup"><span data-stu-id="0f817-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="0f817-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0f817-109">EXAMPLES</span></span>

### <span data-ttu-id="0f817-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f817-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="0f817-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f817-111">PARAMETERS</span></span>

### <span data-ttu-id="0f817-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0f817-112">-AccountName</span></span>
<span data-ttu-id="0f817-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="0f817-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0f817-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0f817-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0f817-115">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="0f817-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0f817-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f817-116">-Confirm</span></span>
<span data-ttu-id="0f817-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f817-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f817-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f817-118">-DefaultProfile</span></span>
<span data-ttu-id="0f817-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f817-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f817-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0f817-120">-Name</span></span>
<span data-ttu-id="0f817-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="0f817-121">Database name.</span></span>

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

### <span data-ttu-id="0f817-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0f817-122">-ParentObject</span></span>
<span data-ttu-id="0f817-123">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="0f817-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0f817-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f817-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f817-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f817-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0f817-126">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="0f817-126">-Throughput</span></span>
<span data-ttu-id="0f817-127">Пропускная способность SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="0f817-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="0f817-128">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="0f817-128">Default value is 400.</span></span>

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

### <span data-ttu-id="0f817-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f817-129">-WhatIf</span></span>
<span data-ttu-id="0f817-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f817-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f817-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0f817-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f817-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f817-132">CommonParameters</span></span>
<span data-ttu-id="0f817-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f817-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f817-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f817-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f817-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f817-135">INPUTS</span></span>

### <span data-ttu-id="0f817-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0f817-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0f817-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0f817-137">OUTPUTS</span></span>

### <span data-ttu-id="0f817-138">Microsoft.Azure.Commands.GetsDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0f817-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="0f817-139">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="0f817-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="0f817-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0f817-140">NOTES</span></span>

## <span data-ttu-id="0f817-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f817-141">RELATED LINKS</span></span>
