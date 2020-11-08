---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245094"
---
# <span data-ttu-id="c22ac-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="c22ac-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="c22ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c22ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c22ac-103">Возвращает триггер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c22ac-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="c22ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c22ac-104">SYNTAX</span></span>

### <span data-ttu-id="c22ac-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c22ac-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c22ac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c22ac-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c22ac-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c22ac-107">DESCRIPTION</span></span>
<span data-ttu-id="c22ac-108">Командлет **Get-AzCosmosDBSqlTrigger** получает список всех существующих триггеров CosmosDB SQL для заданных ResourceGroupName, имя_учетной_записи, DatabaseName и ContainerName и получает один CosmosDBный триггер SQL для данного ResourceGroupName, имя_учетной_записи, DatabaseName, ContainerName и TriggerName.</span><span class="sxs-lookup"><span data-stu-id="c22ac-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="c22ac-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c22ac-109">EXAMPLES</span></span>

### <span data-ttu-id="c22ac-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c22ac-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="c22ac-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c22ac-111">PARAMETERS</span></span>

### <span data-ttu-id="c22ac-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="c22ac-112">-AccountName</span></span>
<span data-ttu-id="c22ac-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c22ac-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c22ac-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c22ac-114">-ContainerName</span></span>
<span data-ttu-id="c22ac-115">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="c22ac-115">Container name.</span></span>

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

### <span data-ttu-id="c22ac-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c22ac-116">-DatabaseName</span></span>
<span data-ttu-id="c22ac-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c22ac-117">Database name.</span></span>

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

### <span data-ttu-id="c22ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22ac-118">-DefaultProfile</span></span>
<span data-ttu-id="c22ac-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c22ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c22ac-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c22ac-120">-Name</span></span>
<span data-ttu-id="c22ac-121">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="c22ac-121">Trigger name.</span></span>

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

### <span data-ttu-id="c22ac-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c22ac-122">-ParentObject</span></span>
<span data-ttu-id="c22ac-123">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="c22ac-123">Sql Container object.</span></span>

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

### <span data-ttu-id="c22ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="c22ac-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c22ac-125">Name of resource group.</span></span>

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

### <span data-ttu-id="c22ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22ac-126">CommonParameters</span></span>
<span data-ttu-id="c22ac-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c22ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22ac-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c22ac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22ac-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c22ac-129">INPUTS</span></span>

### <span data-ttu-id="c22ac-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="c22ac-130">None</span></span>

## <span data-ttu-id="c22ac-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c22ac-131">OUTPUTS</span></span>

### <span data-ttu-id="c22ac-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="c22ac-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="c22ac-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c22ac-133">NOTES</span></span>

## <span data-ttu-id="c22ac-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c22ac-134">RELATED LINKS</span></span>
