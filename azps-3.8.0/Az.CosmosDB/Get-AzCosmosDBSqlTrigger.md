---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6631cad83260a935f2849391941ec0cf6514b188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065030"
---
# <span data-ttu-id="93c9e-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="93c9e-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="93c9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="93c9e-103">Возвращает триггер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="93c9e-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="93c9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93c9e-104">SYNTAX</span></span>

### <span data-ttu-id="93c9e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c9e-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93c9e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c9e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93c9e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93c9e-107">DESCRIPTION</span></span>
<span data-ttu-id="93c9e-108">Командлет **Get-AzCosmosDBSqlTrigger** получает список всех существующих триггеров CosmosDB SQL для заданных ResourceGroupName, имя_учетной_записи, DatabaseName и ContainerName и получает один CosmosDBный триггер SQL для данного ResourceGroupName, имя_учетной_записи, DatabaseName, ContainerName и TriggerName.</span><span class="sxs-lookup"><span data-stu-id="93c9e-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="93c9e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93c9e-109">EXAMPLES</span></span>

### <span data-ttu-id="93c9e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93c9e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="93c9e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93c9e-111">PARAMETERS</span></span>

### <span data-ttu-id="93c9e-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="93c9e-112">-AccountName</span></span>
<span data-ttu-id="93c9e-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="93c9e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="93c9e-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="93c9e-114">-ContainerName</span></span>
<span data-ttu-id="93c9e-115">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="93c9e-115">Container name.</span></span>

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

### <span data-ttu-id="93c9e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="93c9e-116">-DatabaseName</span></span>
<span data-ttu-id="93c9e-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="93c9e-117">Database name.</span></span>

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

### <span data-ttu-id="93c9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c9e-118">-DefaultProfile</span></span>
<span data-ttu-id="93c9e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93c9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93c9e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93c9e-120">-InputObject</span></span>
<span data-ttu-id="93c9e-121">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="93c9e-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93c9e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93c9e-122">-Name</span></span>
<span data-ttu-id="93c9e-123">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="93c9e-123">Trigger name.</span></span>

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

### <span data-ttu-id="93c9e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93c9e-124">-ResourceGroupName</span></span>
<span data-ttu-id="93c9e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93c9e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="93c9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c9e-126">CommonParameters</span></span>
<span data-ttu-id="93c9e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93c9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c9e-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93c9e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c9e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93c9e-129">INPUTS</span></span>

### <span data-ttu-id="93c9e-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="93c9e-130">None</span></span>

## <span data-ttu-id="93c9e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93c9e-131">OUTPUTS</span></span>

### <span data-ttu-id="93c9e-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="93c9e-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="93c9e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="93c9e-133">NOTES</span></span>

## <span data-ttu-id="93c9e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93c9e-134">RELATED LINKS</span></span>
