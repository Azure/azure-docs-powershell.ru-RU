---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508866"
---
# <span data-ttu-id="a8d89-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="a8d89-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="a8d89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8d89-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d89-103">Получает таблицу "ЦыDB".</span><span class="sxs-lookup"><span data-stu-id="a8d89-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="a8d89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8d89-104">SYNTAX</span></span>

### <span data-ttu-id="a8d89-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8d89-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8d89-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8d89-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8d89-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8d89-107">DESCRIPTION</span></span>
<span data-ttu-id="a8d89-108">Для **получения существующей таблицы возвращается cmdlet Get-AzCosmosDBTable.**</span><span class="sxs-lookup"><span data-stu-id="a8d89-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="a8d89-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8d89-109">EXAMPLES</span></span>

### <span data-ttu-id="a8d89-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8d89-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="a8d89-111">Объект ресурса содержит свойства _rid, _ts, _tag_ таблицы.</span><span class="sxs-lookup"><span data-stu-id="a8d89-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="a8d89-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8d89-112">PARAMETERS</span></span>

### <span data-ttu-id="a8d89-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a8d89-113">-AccountName</span></span>
<span data-ttu-id="a8d89-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="a8d89-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a8d89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d89-115">-DefaultProfile</span></span>
<span data-ttu-id="a8d89-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8d89-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a8d89-117">-Name</span></span>
<span data-ttu-id="a8d89-118">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="a8d89-118">Name of the Table.</span></span>

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

### <span data-ttu-id="a8d89-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a8d89-119">-ParentObject</span></span>
<span data-ttu-id="a8d89-120">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="a8d89-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a8d89-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8d89-121">-ResourceGroupName</span></span>
<span data-ttu-id="a8d89-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8d89-122">Name of resource group.</span></span>

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

### <span data-ttu-id="a8d89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d89-123">CommonParameters</span></span>
<span data-ttu-id="a8d89-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8d89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d89-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8d89-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d89-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8d89-126">INPUTS</span></span>

### <span data-ttu-id="a8d89-127">Нет</span><span class="sxs-lookup"><span data-stu-id="a8d89-127">None</span></span>

## <span data-ttu-id="a8d89-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8d89-128">OUTPUTS</span></span>

### <span data-ttu-id="a8d89-129">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a8d89-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="a8d89-130">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a8d89-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a8d89-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8d89-131">NOTES</span></span>

## <span data-ttu-id="a8d89-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8d89-132">RELATED LINKS</span></span>
