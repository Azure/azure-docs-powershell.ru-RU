---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 28b616315913ae70722b5a600d4b10879c7b8334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986908"
---
# <span data-ttu-id="42e05-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="42e05-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="42e05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42e05-102">SYNOPSIS</span></span>
<span data-ttu-id="42e05-103">Получает триггер SqlDb.</span><span class="sxs-lookup"><span data-stu-id="42e05-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="42e05-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="42e05-104">SYNTAX</span></span>

### <span data-ttu-id="42e05-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42e05-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42e05-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42e05-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42e05-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42e05-107">DESCRIPTION</span></span>
<span data-ttu-id="42e05-108">Cmdlet **Get-AzCosmosDBSqlTrigger** получает список всех существующих триггеров Sql Для AzsDB для заданного названия группы ресурсов, AccountName, DatabaseName и ContainerName и получает один триггер Sql ПеретассDB для заданного имени группы ресурсов, AccountName, DatabaseName, ContainerName и TriggerName.</span><span class="sxs-lookup"><span data-stu-id="42e05-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="42e05-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="42e05-109">EXAMPLES</span></span>

### <span data-ttu-id="42e05-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42e05-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="42e05-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42e05-111">PARAMETERS</span></span>

### <span data-ttu-id="42e05-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42e05-112">-AccountName</span></span>
<span data-ttu-id="42e05-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="42e05-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="42e05-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="42e05-114">-ContainerName</span></span>
<span data-ttu-id="42e05-115">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="42e05-115">Container name.</span></span>

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

### <span data-ttu-id="42e05-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="42e05-116">-DatabaseName</span></span>
<span data-ttu-id="42e05-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="42e05-117">Database name.</span></span>

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

### <span data-ttu-id="42e05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e05-118">-DefaultProfile</span></span>
<span data-ttu-id="42e05-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42e05-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42e05-120">-Name</span><span class="sxs-lookup"><span data-stu-id="42e05-120">-Name</span></span>
<span data-ttu-id="42e05-121">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="42e05-121">Trigger name.</span></span>

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

### <span data-ttu-id="42e05-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="42e05-122">-ParentObject</span></span>
<span data-ttu-id="42e05-123">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="42e05-123">Sql Container object.</span></span>

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

### <span data-ttu-id="42e05-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e05-124">-ResourceGroupName</span></span>
<span data-ttu-id="42e05-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42e05-125">Name of resource group.</span></span>

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

### <span data-ttu-id="42e05-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e05-126">CommonParameters</span></span>
<span data-ttu-id="42e05-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e05-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e05-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42e05-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e05-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42e05-129">INPUTS</span></span>

### <span data-ttu-id="42e05-130">Нет</span><span class="sxs-lookup"><span data-stu-id="42e05-130">None</span></span>

## <span data-ttu-id="42e05-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="42e05-131">OUTPUTS</span></span>

### <span data-ttu-id="42e05-132">Microsoft.Azure.Commands.GetsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="42e05-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="42e05-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="42e05-133">NOTES</span></span>

## <span data-ttu-id="42e05-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42e05-134">RELATED LINKS</span></span>
