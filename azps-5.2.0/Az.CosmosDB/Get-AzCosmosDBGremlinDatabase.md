---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400407"
---
# <span data-ttu-id="c41dc-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="c41dc-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="c41dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c41dc-102">SYNOPSIS</span></span>
<span data-ttu-id="c41dc-103">Получает базу данных "ГрадыDB Гремлин".</span><span class="sxs-lookup"><span data-stu-id="c41dc-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="c41dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c41dc-104">SYNTAX</span></span>

### <span data-ttu-id="c41dc-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c41dc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c41dc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c41dc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c41dc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c41dc-107">DESCRIPTION</span></span>
<span data-ttu-id="c41dc-108">**Cmdlet Get-AzCosmosDBGremlinDatabase** получает базу данных "РегинаDB Гремлин".</span><span class="sxs-lookup"><span data-stu-id="c41dc-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="c41dc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c41dc-109">EXAMPLES</span></span>

### <span data-ttu-id="c41dc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c41dc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="c41dc-111">Объект ресурсов содержит _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="c41dc-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="c41dc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c41dc-112">PARAMETERS</span></span>

### <span data-ttu-id="c41dc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c41dc-113">-AccountName</span></span>
<span data-ttu-id="c41dc-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="c41dc-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c41dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41dc-115">-DefaultProfile</span></span>
<span data-ttu-id="c41dc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c41dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c41dc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c41dc-117">-Name</span></span>
<span data-ttu-id="c41dc-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c41dc-118">Database name.</span></span>

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

### <span data-ttu-id="c41dc-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c41dc-119">-ParentObject</span></span>
<span data-ttu-id="c41dc-120">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="c41dc-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c41dc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c41dc-121">-ResourceGroupName</span></span>
<span data-ttu-id="c41dc-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c41dc-122">Name of resource group.</span></span>

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

### <span data-ttu-id="c41dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41dc-123">CommonParameters</span></span>
<span data-ttu-id="c41dc-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c41dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41dc-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c41dc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41dc-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c41dc-126">INPUTS</span></span>

### <span data-ttu-id="c41dc-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c41dc-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c41dc-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c41dc-128">OUTPUTS</span></span>

### <span data-ttu-id="c41dc-129">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c41dc-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="c41dc-130">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c41dc-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c41dc-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c41dc-131">NOTES</span></span>

## <span data-ttu-id="c41dc-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c41dc-132">RELATED LINKS</span></span>
