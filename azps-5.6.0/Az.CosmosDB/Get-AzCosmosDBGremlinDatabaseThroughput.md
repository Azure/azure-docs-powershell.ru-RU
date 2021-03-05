---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 4dbfea5106b46bd8d0f1efc1926841dd964b0299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983640"
---
# <span data-ttu-id="9f8fc-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="9f8fc-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="9f8fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8fc-103">Получает пропускную способность базы данных ВайссDB Гремлин.</span><span class="sxs-lookup"><span data-stu-id="9f8fc-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="9f8fc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f8fc-104">SYNTAX</span></span>

### <span data-ttu-id="9f8fc-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f8fc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f8fc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f8fc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f8fc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f8fc-107">DESCRIPTION</span></span>
<span data-ttu-id="9f8fc-108">С **помощью cmdlet get-AzCosmosDBGremlinDatabaseThroughput** можно получить пропускную способность базы данных "ЦыDB Гремлин".</span><span class="sxs-lookup"><span data-stu-id="9f8fc-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="9f8fc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f8fc-109">EXAMPLES</span></span>

### <span data-ttu-id="9f8fc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f8fc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="9f8fc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f8fc-111">PARAMETERS</span></span>

### <span data-ttu-id="9f8fc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9f8fc-112">-AccountName</span></span>
<span data-ttu-id="9f8fc-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="9f8fc-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9f8fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8fc-114">-DefaultProfile</span></span>
<span data-ttu-id="9f8fc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f8fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f8fc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f8fc-116">-InputObject</span></span>
<span data-ttu-id="9f8fc-117">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="9f8fc-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9f8fc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9f8fc-118">-Name</span></span>
<span data-ttu-id="9f8fc-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f8fc-119">Database name.</span></span>

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

### <span data-ttu-id="9f8fc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f8fc-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f8fc-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f8fc-121">Name of resource group.</span></span>

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

### <span data-ttu-id="9f8fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8fc-122">CommonParameters</span></span>
<span data-ttu-id="9f8fc-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f8fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8fc-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f8fc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8fc-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f8fc-125">INPUTS</span></span>

### <span data-ttu-id="9f8fc-126">Нет</span><span class="sxs-lookup"><span data-stu-id="9f8fc-126">None</span></span>

## <span data-ttu-id="9f8fc-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f8fc-127">OUTPUTS</span></span>

### <span data-ttu-id="9f8fc-128">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9f8fc-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9f8fc-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f8fc-129">NOTES</span></span>

## <span data-ttu-id="9f8fc-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f8fc-130">RELATED LINKS</span></span>
