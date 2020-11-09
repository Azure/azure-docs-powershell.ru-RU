---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314972"
---
# <span data-ttu-id="6fb5b-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="6fb5b-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="6fb5b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6fb5b-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb5b-103">Возвращает таблицу CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6fb5b-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="6fb5b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6fb5b-104">SYNTAX</span></span>

### <span data-ttu-id="6fb5b-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6fb5b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb5b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fb5b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fb5b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fb5b-107">DESCRIPTION</span></span>
<span data-ttu-id="6fb5b-108">Командлет **Get-AzCosmosDBTable** получает существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="6fb5b-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="6fb5b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6fb5b-109">EXAMPLES</span></span>

### <span data-ttu-id="6fb5b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6fb5b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="6fb5b-111">Объект Resource (ресурс), содержащий _rid, _ts, _ свойства ETag таблицы.</span><span class="sxs-lookup"><span data-stu-id="6fb5b-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="6fb5b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6fb5b-112">PARAMETERS</span></span>

### <span data-ttu-id="6fb5b-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="6fb5b-113">-AccountName</span></span>
<span data-ttu-id="6fb5b-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6fb5b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6fb5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb5b-115">-DefaultProfile</span></span>
<span data-ttu-id="6fb5b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb5b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb5b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6fb5b-117">-Name</span></span>
<span data-ttu-id="6fb5b-118">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="6fb5b-118">Name of the Table.</span></span>

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

### <span data-ttu-id="6fb5b-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6fb5b-119">-ParentObject</span></span>
<span data-ttu-id="6fb5b-120">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6fb5b-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb5b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb5b-121">-ResourceGroupName</span></span>
<span data-ttu-id="6fb5b-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fb5b-122">Name of resource group.</span></span>

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

### <span data-ttu-id="6fb5b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb5b-123">CommonParameters</span></span>
<span data-ttu-id="6fb5b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6fb5b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb5b-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fb5b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb5b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6fb5b-126">INPUTS</span></span>

### <span data-ttu-id="6fb5b-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="6fb5b-127">None</span></span>

## <span data-ttu-id="6fb5b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fb5b-128">OUTPUTS</span></span>

### <span data-ttu-id="6fb5b-129">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="6fb5b-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="6fb5b-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6fb5b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6fb5b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6fb5b-131">NOTES</span></span>

## <span data-ttu-id="6fb5b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fb5b-132">RELATED LINKS</span></span>