---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215457"
---
# <span data-ttu-id="9c232-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="9c232-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="9c232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c232-102">SYNOPSIS</span></span>
<span data-ttu-id="9c232-103">Получает свойства пропускной способности "Проект", задав свойства пропускной способности базы данных MongoDB.</span><span class="sxs-lookup"><span data-stu-id="9c232-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="9c232-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9c232-104">SYNTAX</span></span>

### <span data-ttu-id="9c232-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c232-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c232-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c232-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c232-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c232-107">DESCRIPTION</span></span>
<span data-ttu-id="9c232-108">С **помощью cmdlet get-AzCosmosDBMongoDBDatabaseThroughput** можно получить свойства пропускной способности базы данных MongoDB.</span><span class="sxs-lookup"><span data-stu-id="9c232-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="9c232-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9c232-109">EXAMPLES</span></span>

### <span data-ttu-id="9c232-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c232-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="9c232-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c232-111">PARAMETERS</span></span>

### <span data-ttu-id="9c232-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c232-112">-AccountName</span></span>
<span data-ttu-id="9c232-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="9c232-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9c232-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c232-114">-DefaultProfile</span></span>
<span data-ttu-id="9c232-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c232-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c232-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c232-116">-InputObject</span></span>
<span data-ttu-id="9c232-117">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="9c232-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9c232-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9c232-118">-Name</span></span>
<span data-ttu-id="9c232-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9c232-119">Database name.</span></span>

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

### <span data-ttu-id="9c232-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c232-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c232-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c232-121">Name of resource group.</span></span>

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

### <span data-ttu-id="9c232-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c232-122">CommonParameters</span></span>
<span data-ttu-id="9c232-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c232-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c232-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c232-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c232-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c232-125">INPUTS</span></span>

### <span data-ttu-id="9c232-126">Нет</span><span class="sxs-lookup"><span data-stu-id="9c232-126">None</span></span>

## <span data-ttu-id="9c232-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c232-127">OUTPUTS</span></span>

### <span data-ttu-id="9c232-128">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9c232-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9c232-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9c232-129">NOTES</span></span>

## <span data-ttu-id="9c232-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c232-130">RELATED LINKS</span></span>
