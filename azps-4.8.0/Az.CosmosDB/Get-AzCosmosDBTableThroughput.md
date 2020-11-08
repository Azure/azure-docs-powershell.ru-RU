---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236866"
---
# <span data-ttu-id="baa76-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="baa76-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="baa76-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="baa76-102">SYNOPSIS</span></span>
<span data-ttu-id="baa76-103">Возвращает пропускную способность таблицы CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="baa76-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="baa76-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="baa76-104">SYNTAX</span></span>

### <span data-ttu-id="baa76-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="baa76-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baa76-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="baa76-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baa76-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baa76-107">DESCRIPTION</span></span>
<span data-ttu-id="baa76-108">Командлет **Get-AzCosmosDBTableThroughput** возвращает пропускную способность таблицы CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="baa76-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="baa76-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="baa76-109">EXAMPLES</span></span>

### <span data-ttu-id="baa76-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="baa76-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="baa76-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="baa76-111">PARAMETERS</span></span>

### <span data-ttu-id="baa76-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="baa76-112">-AccountName</span></span>
<span data-ttu-id="baa76-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="baa76-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="baa76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa76-114">-DefaultProfile</span></span>
<span data-ttu-id="baa76-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baa76-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baa76-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baa76-116">-InputObject</span></span>
<span data-ttu-id="baa76-117">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="baa76-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="baa76-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="baa76-118">-Name</span></span>
<span data-ttu-id="baa76-119">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="baa76-119">Name of the Table.</span></span>

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

### <span data-ttu-id="baa76-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa76-120">-ResourceGroupName</span></span>
<span data-ttu-id="baa76-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="baa76-121">Name of resource group.</span></span>

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

### <span data-ttu-id="baa76-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa76-122">CommonParameters</span></span>
<span data-ttu-id="baa76-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="baa76-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa76-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baa76-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa76-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="baa76-125">INPUTS</span></span>

### <span data-ttu-id="baa76-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="baa76-126">None</span></span>

## <span data-ttu-id="baa76-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="baa76-127">OUTPUTS</span></span>

### <span data-ttu-id="baa76-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="baa76-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="baa76-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="baa76-129">NOTES</span></span>

## <span data-ttu-id="baa76-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baa76-130">RELATED LINKS</span></span>