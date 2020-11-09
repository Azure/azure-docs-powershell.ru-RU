---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314999"
---
# <span data-ttu-id="46477-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="46477-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="46477-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46477-102">SYNOPSIS</span></span>
<span data-ttu-id="46477-103">Получает параметры пропускной способности, соответствующие базе данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="46477-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="46477-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46477-104">SYNTAX</span></span>

### <span data-ttu-id="46477-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46477-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46477-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46477-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46477-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46477-107">DESCRIPTION</span></span>
<span data-ttu-id="46477-108">Командлет **Get-AzCosmosDBSqlDatabaseThroughput** получает параметры пропускной способности, соответствующие базе данных CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="46477-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="46477-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46477-109">EXAMPLES</span></span>

### <span data-ttu-id="46477-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46477-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="46477-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46477-111">PARAMETERS</span></span>

### <span data-ttu-id="46477-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="46477-112">-AccountName</span></span>
<span data-ttu-id="46477-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="46477-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46477-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46477-114">-DefaultProfile</span></span>
<span data-ttu-id="46477-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46477-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46477-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46477-116">-InputObject</span></span>
<span data-ttu-id="46477-117">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="46477-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="46477-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46477-118">-Name</span></span>
<span data-ttu-id="46477-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="46477-119">Database name.</span></span>

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

### <span data-ttu-id="46477-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46477-120">-ResourceGroupName</span></span>
<span data-ttu-id="46477-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46477-121">Name of resource group.</span></span>

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

### <span data-ttu-id="46477-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46477-122">CommonParameters</span></span>
<span data-ttu-id="46477-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46477-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46477-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46477-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46477-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46477-125">INPUTS</span></span>

### <span data-ttu-id="46477-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="46477-126">None</span></span>

## <span data-ttu-id="46477-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46477-127">OUTPUTS</span></span>

### <span data-ttu-id="46477-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="46477-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="46477-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="46477-129">NOTES</span></span>

## <span data-ttu-id="46477-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46477-130">RELATED LINKS</span></span>
