---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066140"
---
# <span data-ttu-id="842da-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="842da-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="842da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="842da-102">SYNOPSIS</span></span>
<span data-ttu-id="842da-103">Создание нового агента эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="842da-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="842da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="842da-104">SYNTAX</span></span>

### <span data-ttu-id="842da-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="842da-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="842da-106">Объект</span><span class="sxs-lookup"><span data-stu-id="842da-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="842da-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="842da-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="842da-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="842da-108">DESCRIPTION</span></span>
<span data-ttu-id="842da-109">Командлет New-AzSqlElasticJobAgent создает новый агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="842da-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="842da-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="842da-110">EXAMPLES</span></span>

### <span data-ttu-id="842da-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="842da-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="842da-112">Создание нового агента эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="842da-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="842da-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="842da-113">PARAMETERS</span></span>

### <span data-ttu-id="842da-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="842da-114">-DatabaseName</span></span>
<span data-ttu-id="842da-115">Имя базы данных;</span><span class="sxs-lookup"><span data-stu-id="842da-115">The database name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842da-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="842da-116">-DatabaseObject</span></span>
<span data-ttu-id="842da-117">Объект базы данных элемента управления агента</span><span class="sxs-lookup"><span data-stu-id="842da-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="842da-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="842da-118">-DatabaseResourceId</span></span>
<span data-ttu-id="842da-119">Идентификатор ресурса базы данных агента управления агентом</span><span class="sxs-lookup"><span data-stu-id="842da-119">The Agent Control Database Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842da-120">-DefaultProfile</span></span>
<span data-ttu-id="842da-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="842da-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842da-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="842da-122">-Name</span></span>
<span data-ttu-id="842da-123">Имя агента</span><span class="sxs-lookup"><span data-stu-id="842da-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842da-124">-ResourceGroupName</span></span>
<span data-ttu-id="842da-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="842da-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842da-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="842da-126">-ServerName</span></span>
<span data-ttu-id="842da-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="842da-127">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842da-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="842da-128">-Tag</span></span>
<span data-ttu-id="842da-129">Теги агента</span><span class="sxs-lookup"><span data-stu-id="842da-129">The Agent Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842da-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="842da-130">-Confirm</span></span>
<span data-ttu-id="842da-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="842da-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="842da-132">-WhatIf</span></span>
<span data-ttu-id="842da-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="842da-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="842da-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="842da-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842da-135">CommonParameters</span></span>
<span data-ttu-id="842da-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="842da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842da-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="842da-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842da-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="842da-138">INPUTS</span></span>

### <span data-ttu-id="842da-139">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="842da-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="842da-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="842da-140">OUTPUTS</span></span>

### <span data-ttu-id="842da-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="842da-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="842da-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="842da-142">NOTES</span></span>

## <span data-ttu-id="842da-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="842da-143">RELATED LINKS</span></span>
