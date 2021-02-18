---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215449"
---
# <span data-ttu-id="076d2-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="076d2-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="076d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="076d2-102">SYNOPSIS</span></span>
<span data-ttu-id="076d2-103">Получает триггер SqlDb.</span><span class="sxs-lookup"><span data-stu-id="076d2-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="076d2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="076d2-104">SYNTAX</span></span>

### <span data-ttu-id="076d2-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="076d2-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="076d2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="076d2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="076d2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="076d2-107">DESCRIPTION</span></span>
<span data-ttu-id="076d2-108">Cmdlet **Get-AzCosmosDBSqlTrigger** получает список всех существующих триггеров Sql Для AzsDB для заданного названия группы ресурсов, AccountName, DatabaseName и ContainerName и получает один триггер SqlББ для заданного имени ресурса ResourceGroupName, AccountName, DatabaseName, ContainerName и TriggerName.</span><span class="sxs-lookup"><span data-stu-id="076d2-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="076d2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="076d2-109">EXAMPLES</span></span>

### <span data-ttu-id="076d2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="076d2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="076d2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="076d2-111">PARAMETERS</span></span>

### <span data-ttu-id="076d2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="076d2-112">-AccountName</span></span>
<span data-ttu-id="076d2-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="076d2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="076d2-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="076d2-114">-ContainerName</span></span>
<span data-ttu-id="076d2-115">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="076d2-115">Container name.</span></span>

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

### <span data-ttu-id="076d2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="076d2-116">-DatabaseName</span></span>
<span data-ttu-id="076d2-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="076d2-117">Database name.</span></span>

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

### <span data-ttu-id="076d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="076d2-118">-DefaultProfile</span></span>
<span data-ttu-id="076d2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="076d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="076d2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="076d2-120">-Name</span></span>
<span data-ttu-id="076d2-121">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="076d2-121">Trigger name.</span></span>

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

### <span data-ttu-id="076d2-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="076d2-122">-ParentObject</span></span>
<span data-ttu-id="076d2-123">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="076d2-123">Sql Container object.</span></span>

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

### <span data-ttu-id="076d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="076d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="076d2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="076d2-125">Name of resource group.</span></span>

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

### <span data-ttu-id="076d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076d2-126">CommonParameters</span></span>
<span data-ttu-id="076d2-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="076d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076d2-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="076d2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076d2-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="076d2-129">INPUTS</span></span>

### <span data-ttu-id="076d2-130">Нет</span><span class="sxs-lookup"><span data-stu-id="076d2-130">None</span></span>

## <span data-ttu-id="076d2-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="076d2-131">OUTPUTS</span></span>

### <span data-ttu-id="076d2-132">Microsoft.Azure.Commands.GetsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="076d2-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="076d2-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="076d2-133">NOTES</span></span>

## <span data-ttu-id="076d2-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="076d2-134">RELATED LINKS</span></span>
