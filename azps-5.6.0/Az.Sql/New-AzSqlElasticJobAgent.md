---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: ca23ba63e2f92fa14c97957a2b21b38d91e453ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982019"
---
# <span data-ttu-id="43b3a-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="43b3a-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="43b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="43b3a-103">Создание нового эластичного агента задания</span><span class="sxs-lookup"><span data-stu-id="43b3a-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="43b3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43b3a-104">SYNTAX</span></span>

### <span data-ttu-id="43b3a-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43b3a-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43b3a-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="43b3a-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43b3a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="43b3a-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43b3a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43b3a-108">DESCRIPTION</span></span>
<span data-ttu-id="43b3a-109">С New-AzSqlElasticJobAgent создается новый агент эластичного задания</span><span class="sxs-lookup"><span data-stu-id="43b3a-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="43b3a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43b3a-110">EXAMPLES</span></span>

### <span data-ttu-id="43b3a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43b3a-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="43b3a-112">Создание нового агента эластичного задания</span><span class="sxs-lookup"><span data-stu-id="43b3a-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="43b3a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43b3a-113">PARAMETERS</span></span>

### <span data-ttu-id="43b3a-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="43b3a-114">-DatabaseName</span></span>
<span data-ttu-id="43b3a-115">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="43b3a-115">The database name</span></span>

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

### <span data-ttu-id="43b3a-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="43b3a-116">-DatabaseObject</span></span>
<span data-ttu-id="43b3a-117">Объект базы данных под управлением агента</span><span class="sxs-lookup"><span data-stu-id="43b3a-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="43b3a-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="43b3a-118">-DatabaseResourceId</span></span>
<span data-ttu-id="43b3a-119">ИД агента для управления базой данных</span><span class="sxs-lookup"><span data-stu-id="43b3a-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="43b3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b3a-120">-DefaultProfile</span></span>
<span data-ttu-id="43b3a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43b3a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43b3a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="43b3a-122">-Name</span></span>
<span data-ttu-id="43b3a-123">Имя агента</span><span class="sxs-lookup"><span data-stu-id="43b3a-123">The Agent Name</span></span>

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

### <span data-ttu-id="43b3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="43b3a-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="43b3a-125">The resource group name</span></span>

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

### <span data-ttu-id="43b3a-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43b3a-126">-ServerName</span></span>
<span data-ttu-id="43b3a-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="43b3a-127">The server name</span></span>

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

### <span data-ttu-id="43b3a-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="43b3a-128">-Tag</span></span>
<span data-ttu-id="43b3a-129">Теги агента</span><span class="sxs-lookup"><span data-stu-id="43b3a-129">The Agent Tags</span></span>

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

### <span data-ttu-id="43b3a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43b3a-130">-Confirm</span></span>
<span data-ttu-id="43b3a-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="43b3a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43b3a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43b3a-132">-WhatIf</span></span>
<span data-ttu-id="43b3a-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43b3a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43b3a-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="43b3a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43b3a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b3a-135">CommonParameters</span></span>
<span data-ttu-id="43b3a-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b3a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b3a-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43b3a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b3a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43b3a-138">INPUTS</span></span>

### <span data-ttu-id="43b3a-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="43b3a-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="43b3a-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43b3a-140">OUTPUTS</span></span>

### <span data-ttu-id="43b3a-141">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="43b3a-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="43b3a-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43b3a-142">NOTES</span></span>

## <span data-ttu-id="43b3a-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43b3a-143">RELATED LINKS</span></span>
