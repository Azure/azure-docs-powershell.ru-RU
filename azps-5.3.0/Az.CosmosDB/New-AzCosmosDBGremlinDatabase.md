---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508826"
---
# <span data-ttu-id="5c995-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="5c995-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="5c995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c995-102">SYNOPSIS</span></span>
<span data-ttu-id="5c995-103">Создает новую базу данных «ПеретассDB Гремлин».</span><span class="sxs-lookup"><span data-stu-id="5c995-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="5c995-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c995-104">SYNTAX</span></span>

### <span data-ttu-id="5c995-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c995-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c995-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c995-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c995-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c995-107">DESCRIPTION</span></span>
<span data-ttu-id="5c995-108">Создает новую базу данных «ПеретассDB Гремлин».</span><span class="sxs-lookup"><span data-stu-id="5c995-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="5c995-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c995-109">EXAMPLES</span></span>

### <span data-ttu-id="5c995-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5c995-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="5c995-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c995-111">PARAMETERS</span></span>

### <span data-ttu-id="5c995-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5c995-112">-AccountName</span></span>
<span data-ttu-id="5c995-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="5c995-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5c995-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5c995-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5c995-115">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="5c995-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5c995-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c995-116">-Confirm</span></span>
<span data-ttu-id="5c995-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c995-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c995-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c995-118">-DefaultProfile</span></span>
<span data-ttu-id="5c995-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c995-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c995-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5c995-120">-Name</span></span>
<span data-ttu-id="5c995-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5c995-121">Database name.</span></span>

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

### <span data-ttu-id="5c995-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5c995-122">-ParentObject</span></span>
<span data-ttu-id="5c995-123">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="5c995-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5c995-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c995-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c995-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c995-125">Name of resource group.</span></span>

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

### <span data-ttu-id="5c995-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="5c995-126">-Throughput</span></span>
<span data-ttu-id="5c995-127">Пропускная способность базы данных Гремлин (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5c995-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="5c995-128">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="5c995-128">Default value is 400.</span></span>

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

### <span data-ttu-id="5c995-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c995-129">-WhatIf</span></span>
<span data-ttu-id="5c995-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c995-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c995-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5c995-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c995-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c995-132">CommonParameters</span></span>
<span data-ttu-id="5c995-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c995-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c995-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c995-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c995-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c995-135">INPUTS</span></span>

### <span data-ttu-id="5c995-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5c995-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5c995-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c995-137">OUTPUTS</span></span>

### <span data-ttu-id="5c995-138">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5c995-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="5c995-139">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="5c995-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5c995-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c995-140">NOTES</span></span>

## <span data-ttu-id="5c995-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c995-141">RELATED LINKS</span></span>