---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315020"
---
# <span data-ttu-id="ad086-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="ad086-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="ad086-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad086-102">SYNOPSIS</span></span>
<span data-ttu-id="ad086-103">Возвращает базу данных CosmosDB MongoDB</span><span class="sxs-lookup"><span data-stu-id="ad086-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="ad086-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad086-104">SYNTAX</span></span>

### <span data-ttu-id="ad086-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad086-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad086-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad086-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad086-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad086-107">DESCRIPTION</span></span>
<span data-ttu-id="ad086-108">Командлет **Get-AzCosmosDBMongoDBDatabase** получает базу данных CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="ad086-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="ad086-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad086-109">EXAMPLES</span></span>

### <span data-ttu-id="ad086-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad086-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="ad086-111">Объект Resource (ресурс): _rid, _ts _etag свойств.</span><span class="sxs-lookup"><span data-stu-id="ad086-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="ad086-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad086-112">PARAMETERS</span></span>

### <span data-ttu-id="ad086-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ad086-113">-AccountName</span></span>
<span data-ttu-id="ad086-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ad086-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ad086-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad086-115">-DefaultProfile</span></span>
<span data-ttu-id="ad086-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad086-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad086-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad086-117">-Name</span></span>
<span data-ttu-id="ad086-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad086-118">Database name.</span></span>

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

### <span data-ttu-id="ad086-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ad086-119">-ParentObject</span></span>
<span data-ttu-id="ad086-120">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ad086-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad086-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad086-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad086-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad086-122">Name of resource group.</span></span>

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

### <span data-ttu-id="ad086-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad086-123">CommonParameters</span></span>
<span data-ttu-id="ad086-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad086-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad086-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad086-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad086-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad086-126">INPUTS</span></span>

### <span data-ttu-id="ad086-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ad086-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ad086-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad086-128">OUTPUTS</span></span>

### <span data-ttu-id="ad086-129">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ad086-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="ad086-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ad086-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ad086-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad086-131">NOTES</span></span>

## <span data-ttu-id="ad086-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad086-132">RELATED LINKS</span></span>
