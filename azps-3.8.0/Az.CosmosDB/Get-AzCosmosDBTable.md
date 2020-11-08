---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074882"
---
# <span data-ttu-id="55c87-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="55c87-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="55c87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55c87-102">SYNOPSIS</span></span>
<span data-ttu-id="55c87-103">Возвращает таблицу CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="55c87-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="55c87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55c87-104">SYNTAX</span></span>

### <span data-ttu-id="55c87-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55c87-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55c87-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55c87-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55c87-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55c87-107">DESCRIPTION</span></span>
<span data-ttu-id="55c87-108">Командлет **Get-AzCosmosDBTable** получает существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="55c87-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="55c87-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55c87-109">EXAMPLES</span></span>

### <span data-ttu-id="55c87-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55c87-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="55c87-111">Объект Resource (ресурс), содержащий _rid, _ts, _ свойства ETag таблицы.</span><span class="sxs-lookup"><span data-stu-id="55c87-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="55c87-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55c87-112">PARAMETERS</span></span>

### <span data-ttu-id="55c87-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="55c87-113">-AccountName</span></span>
<span data-ttu-id="55c87-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="55c87-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="55c87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c87-115">-DefaultProfile</span></span>
<span data-ttu-id="55c87-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55c87-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55c87-117">-Подробно</span><span class="sxs-lookup"><span data-stu-id="55c87-117">-Detailed</span></span>
<span data-ttu-id="55c87-118">Если он указан, командлет возвращает таблицу с соответствующим значением пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="55c87-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c87-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55c87-119">-InputObject</span></span>
<span data-ttu-id="55c87-120">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="55c87-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c87-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55c87-121">-Name</span></span>
<span data-ttu-id="55c87-122">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="55c87-122">Name of the Table.</span></span>

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

### <span data-ttu-id="55c87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c87-123">-ResourceGroupName</span></span>
<span data-ttu-id="55c87-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55c87-124">Name of resource group.</span></span>

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

### <span data-ttu-id="55c87-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c87-125">CommonParameters</span></span>
<span data-ttu-id="55c87-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55c87-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c87-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55c87-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c87-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55c87-128">INPUTS</span></span>

### <span data-ttu-id="55c87-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="55c87-129">None</span></span>

## <span data-ttu-id="55c87-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55c87-130">OUTPUTS</span></span>

### <span data-ttu-id="55c87-131">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="55c87-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="55c87-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="55c87-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="55c87-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="55c87-133">NOTES</span></span>

## <span data-ttu-id="55c87-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55c87-134">RELATED LINKS</span></span>
