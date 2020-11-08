---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 2ee1f932e1829e6c1d9d35ccd2cf67473a851414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074435"
---
# <span data-ttu-id="3ed6a-101">Set-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="3ed6a-101">Set-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="3ed6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ed6a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed6a-103">Задает базу данных CosmosDB MongoDB</span><span class="sxs-lookup"><span data-stu-id="3ed6a-103">Sets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="3ed6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ed6a-104">SYNTAX</span></span>

### <span data-ttu-id="3ed6a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ed6a-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed6a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ed6a-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ed6a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ed6a-107">DESCRIPTION</span></span>
<span data-ttu-id="3ed6a-108">Командлет **Set-AzCosmosDBMongoDBDatabase** получает базу данных CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-108">The **Set-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="3ed6a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ed6a-109">EXAMPLES</span></span>

### <span data-ttu-id="3ed6a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ed6a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="3ed6a-111">Объект Resource (ресурс): _rid, _ts _etag свойств.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="3ed6a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ed6a-112">PARAMETERS</span></span>

### <span data-ttu-id="3ed6a-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="3ed6a-113">-AccountName</span></span>
<span data-ttu-id="3ed6a-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3ed6a-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ed6a-115">-Confirm</span></span>
<span data-ttu-id="3ed6a-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ed6a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed6a-117">-DefaultProfile</span></span>
<span data-ttu-id="3ed6a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ed6a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ed6a-119">-InputObject</span></span>
<span data-ttu-id="3ed6a-120">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="3ed6a-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed6a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ed6a-121">-Name</span></span>
<span data-ttu-id="3ed6a-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-122">Database name.</span></span>

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

### <span data-ttu-id="3ed6a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed6a-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ed6a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-124">Name of resource group.</span></span>

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

### <span data-ttu-id="3ed6a-125">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="3ed6a-125">-Throughput</span></span>
<span data-ttu-id="3ed6a-126">Пропускная способность Mongo базы данных (RU/s).</span><span class="sxs-lookup"><span data-stu-id="3ed6a-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="3ed6a-127">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-127">Default value is 400.</span></span>

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

### <span data-ttu-id="3ed6a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed6a-128">-WhatIf</span></span>
<span data-ttu-id="3ed6a-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ed6a-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ed6a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed6a-131">CommonParameters</span></span>
<span data-ttu-id="3ed6a-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ed6a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed6a-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ed6a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed6a-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ed6a-134">INPUTS</span></span>

### <span data-ttu-id="3ed6a-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="3ed6a-135">None</span></span>

## <span data-ttu-id="3ed6a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ed6a-136">OUTPUTS</span></span>

### <span data-ttu-id="3ed6a-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3ed6a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="3ed6a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ed6a-138">NOTES</span></span>

## <span data-ttu-id="3ed6a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ed6a-139">RELATED LINKS</span></span>
