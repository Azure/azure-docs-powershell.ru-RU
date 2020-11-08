---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066663"
---
# <span data-ttu-id="f94d0-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="f94d0-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="f94d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f94d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f94d0-103">Задает таблицу CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f94d0-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="f94d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f94d0-104">SYNTAX</span></span>

### <span data-ttu-id="f94d0-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f94d0-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f94d0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f94d0-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f94d0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f94d0-107">DESCRIPTION</span></span>
<span data-ttu-id="f94d0-108">Командлет **Set-AzCosmosDBTable** создает новую таблицу или обновляет существующую, полностью заменяя существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="f94d0-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="f94d0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f94d0-109">EXAMPLES</span></span>

### <span data-ttu-id="f94d0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f94d0-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="f94d0-111">Объект Resource (ресурс), содержащий _rid, _ts, _ свойства ETag таблицы.</span><span class="sxs-lookup"><span data-stu-id="f94d0-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="f94d0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f94d0-112">PARAMETERS</span></span>

### <span data-ttu-id="f94d0-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f94d0-113">-AccountName</span></span>
<span data-ttu-id="f94d0-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f94d0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f94d0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f94d0-115">-Confirm</span></span>
<span data-ttu-id="f94d0-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f94d0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f94d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94d0-117">-DefaultProfile</span></span>
<span data-ttu-id="f94d0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f94d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f94d0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f94d0-119">-InputObject</span></span>
<span data-ttu-id="f94d0-120">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f94d0-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f94d0-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f94d0-121">-Name</span></span>
<span data-ttu-id="f94d0-122">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="f94d0-122">Name of the Table.</span></span>

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

### <span data-ttu-id="f94d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="f94d0-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f94d0-124">Name of resource group.</span></span>

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

### <span data-ttu-id="f94d0-125">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="f94d0-125">-Throughput</span></span>
<span data-ttu-id="f94d0-126">Пропускная способность таблицы (RU/с).</span><span class="sxs-lookup"><span data-stu-id="f94d0-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="f94d0-127">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="f94d0-127">Default value is 400.</span></span>

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

### <span data-ttu-id="f94d0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f94d0-128">-WhatIf</span></span>
<span data-ttu-id="f94d0-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f94d0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f94d0-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f94d0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f94d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94d0-131">CommonParameters</span></span>
<span data-ttu-id="f94d0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f94d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94d0-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f94d0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94d0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f94d0-134">INPUTS</span></span>

### <span data-ttu-id="f94d0-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f94d0-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f94d0-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f94d0-136">OUTPUTS</span></span>

### <span data-ttu-id="f94d0-137">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="f94d0-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="f94d0-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f94d0-138">NOTES</span></span>

## <span data-ttu-id="f94d0-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f94d0-139">RELATED LINKS</span></span>
