---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 961ba3375c25098de32bf93b4559d9bfa6b8944d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074124"
---
# <span data-ttu-id="5a813-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="5a813-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="5a813-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a813-102">SYNOPSIS</span></span>
<span data-ttu-id="5a813-103">Возвращает пропускную способность CosmosDB базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5a813-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="5a813-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a813-104">SYNTAX</span></span>

### <span data-ttu-id="5a813-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a813-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a813-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a813-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a813-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a813-107">DESCRIPTION</span></span>
<span data-ttu-id="5a813-108">Командлет **Get-AzCosmosDBGremlinDatabaseThroughput** возвращает пропускную способность базы данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5a813-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="5a813-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a813-109">EXAMPLES</span></span>

### <span data-ttu-id="5a813-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a813-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="5a813-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a813-111">PARAMETERS</span></span>

### <span data-ttu-id="5a813-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5a813-112">-AccountName</span></span>
<span data-ttu-id="5a813-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5a813-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5a813-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a813-114">-DefaultProfile</span></span>
<span data-ttu-id="5a813-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a813-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a813-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a813-116">-InputObject</span></span>
<span data-ttu-id="5a813-117">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5a813-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5a813-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a813-118">-Name</span></span>
<span data-ttu-id="5a813-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5a813-119">Database name.</span></span>

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

### <span data-ttu-id="5a813-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a813-120">-ResourceGroupName</span></span>
<span data-ttu-id="5a813-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a813-121">Name of resource group.</span></span>

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

### <span data-ttu-id="5a813-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a813-122">CommonParameters</span></span>
<span data-ttu-id="5a813-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a813-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a813-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a813-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a813-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a813-125">INPUTS</span></span>

### <span data-ttu-id="5a813-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="5a813-126">None</span></span>

## <span data-ttu-id="5a813-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a813-127">OUTPUTS</span></span>

### <span data-ttu-id="5a813-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5a813-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5a813-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a813-129">NOTES</span></span>

## <span data-ttu-id="5a813-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a813-130">RELATED LINKS</span></span>
