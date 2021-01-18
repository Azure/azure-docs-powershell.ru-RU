---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519333"
---
# <span data-ttu-id="ee2a2-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="ee2a2-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="ee2a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2a2-103">Получает пропускную способность таблицы "Приобр".</span><span class="sxs-lookup"><span data-stu-id="ee2a2-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="ee2a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee2a2-104">SYNTAX</span></span>

### <span data-ttu-id="ee2a2-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee2a2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee2a2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2a2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee2a2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee2a2-107">DESCRIPTION</span></span>
<span data-ttu-id="ee2a2-108">С **помощью cmdlet get-AzCosmosDBTableThroughput** можно получить пропускную способность таблицы Вадима Зуева.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="ee2a2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee2a2-109">EXAMPLES</span></span>

### <span data-ttu-id="ee2a2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee2a2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="ee2a2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee2a2-111">PARAMETERS</span></span>

### <span data-ttu-id="ee2a2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ee2a2-112">-AccountName</span></span>
<span data-ttu-id="ee2a2-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="ee2a2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ee2a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2a2-114">-DefaultProfile</span></span>
<span data-ttu-id="ee2a2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee2a2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee2a2-116">-InputObject</span></span>
<span data-ttu-id="ee2a2-117">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="ee2a2-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ee2a2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ee2a2-118">-Name</span></span>
<span data-ttu-id="ee2a2-119">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-119">Name of the Table.</span></span>

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

### <span data-ttu-id="ee2a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee2a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee2a2-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-121">Name of resource group.</span></span>

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

### <span data-ttu-id="ee2a2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2a2-122">CommonParameters</span></span>
<span data-ttu-id="ee2a2-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2a2-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee2a2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2a2-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee2a2-125">INPUTS</span></span>

### <span data-ttu-id="ee2a2-126">Нет</span><span class="sxs-lookup"><span data-stu-id="ee2a2-126">None</span></span>

## <span data-ttu-id="ee2a2-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee2a2-127">OUTPUTS</span></span>

### <span data-ttu-id="ee2a2-128">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ee2a2-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ee2a2-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee2a2-129">NOTES</span></span>

## <span data-ttu-id="ee2a2-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee2a2-130">RELATED LINKS</span></span>
