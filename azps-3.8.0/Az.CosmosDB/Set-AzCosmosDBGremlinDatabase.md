---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 18c1c215daa499514cf671f0c33956757dd56611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074436"
---
# <span data-ttu-id="e90ed-101">Set-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="e90ed-101">Set-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="e90ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e90ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e90ed-103">Задает базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e90ed-103">Sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e90ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e90ed-104">SYNTAX</span></span>

### <span data-ttu-id="e90ed-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e90ed-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e90ed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e90ed-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e90ed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e90ed-107">DESCRIPTION</span></span>
<span data-ttu-id="e90ed-108">Командлет **Set-AzCosmosDBGremlinDatabase** задает базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e90ed-108">The **Set-AzCosmosDBGremlinDatabase** cmdlet sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e90ed-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e90ed-109">EXAMPLES</span></span>

### <span data-ttu-id="e90ed-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e90ed-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="e90ed-111">Объект Resource (ресурс) включает _rid, _ts _etag.</span><span class="sxs-lookup"><span data-stu-id="e90ed-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="e90ed-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e90ed-112">PARAMETERS</span></span>

### <span data-ttu-id="e90ed-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e90ed-113">-AccountName</span></span>
<span data-ttu-id="e90ed-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e90ed-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e90ed-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e90ed-115">-Confirm</span></span>
<span data-ttu-id="e90ed-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e90ed-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e90ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90ed-117">-DefaultProfile</span></span>
<span data-ttu-id="e90ed-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e90ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e90ed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e90ed-119">-InputObject</span></span>
<span data-ttu-id="e90ed-120">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e90ed-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e90ed-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e90ed-121">-Name</span></span>
<span data-ttu-id="e90ed-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e90ed-122">Database name.</span></span>

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

### <span data-ttu-id="e90ed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e90ed-123">-ResourceGroupName</span></span>
<span data-ttu-id="e90ed-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e90ed-124">Name of resource group.</span></span>

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

### <span data-ttu-id="e90ed-125">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="e90ed-125">-Throughput</span></span>
<span data-ttu-id="e90ed-126">Пропускная способность Gremlin базы данных (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e90ed-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="e90ed-127">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="e90ed-127">Default value is 400.</span></span>

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

### <span data-ttu-id="e90ed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e90ed-128">-WhatIf</span></span>
<span data-ttu-id="e90ed-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e90ed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e90ed-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e90ed-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e90ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90ed-131">CommonParameters</span></span>
<span data-ttu-id="e90ed-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e90ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90ed-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e90ed-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90ed-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e90ed-134">INPUTS</span></span>

### <span data-ttu-id="e90ed-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e90ed-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e90ed-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e90ed-136">OUTPUTS</span></span>

### <span data-ttu-id="e90ed-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e90ed-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="e90ed-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e90ed-138">NOTES</span></span>

## <span data-ttu-id="e90ed-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e90ed-139">RELATED LINKS</span></span>
