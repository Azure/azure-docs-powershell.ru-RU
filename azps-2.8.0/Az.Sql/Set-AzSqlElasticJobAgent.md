---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 0da9fd57db1391a78b22ca0b3d4c67598214b164
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906446"
---
# <span data-ttu-id="e1878-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="e1878-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="e1878-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1878-102">SYNOPSIS</span></span>
<span data-ttu-id="e1878-103">Обновляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="e1878-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="e1878-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1878-104">SYNTAX</span></span>

### <span data-ttu-id="e1878-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1878-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1878-106">Объект</span><span class="sxs-lookup"><span data-stu-id="e1878-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1878-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e1878-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1878-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1878-108">DESCRIPTION</span></span>
<span data-ttu-id="e1878-109">Командлет Set-AzSqlElasticJobAgent обновляет агенты эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="e1878-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="e1878-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1878-110">EXAMPLES</span></span>

### <span data-ttu-id="e1878-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1878-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="e1878-112">Обновляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="e1878-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="e1878-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1878-113">PARAMETERS</span></span>

### <span data-ttu-id="e1878-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1878-114">-DefaultProfile</span></span>
<span data-ttu-id="e1878-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1878-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1878-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1878-116">-InputObject</span></span>
<span data-ttu-id="e1878-117">Входной объект агента</span><span class="sxs-lookup"><span data-stu-id="e1878-117">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1878-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1878-118">-Name</span></span>
<span data-ttu-id="e1878-119">Имя агента</span><span class="sxs-lookup"><span data-stu-id="e1878-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1878-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1878-120">-ResourceGroupName</span></span>
<span data-ttu-id="e1878-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e1878-121">The resource group name</span></span>

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

### <span data-ttu-id="e1878-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1878-122">-ResourceId</span></span>
<span data-ttu-id="e1878-123">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="e1878-123">The agent resource id</span></span>

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

### <span data-ttu-id="e1878-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e1878-124">-ServerName</span></span>
<span data-ttu-id="e1878-125">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="e1878-125">The server name</span></span>

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

### <span data-ttu-id="e1878-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="e1878-126">-Tag</span></span>
<span data-ttu-id="e1878-127">Теги, связываемые с агентом базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="e1878-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="e1878-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1878-128">-Confirm</span></span>
<span data-ttu-id="e1878-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1878-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1878-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1878-130">-WhatIf</span></span>
<span data-ttu-id="e1878-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1878-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1878-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1878-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1878-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1878-133">CommonParameters</span></span>
<span data-ttu-id="e1878-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1878-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1878-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1878-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1878-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1878-136">INPUTS</span></span>

### <span data-ttu-id="e1878-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="e1878-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e1878-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1878-138">OUTPUTS</span></span>

### <span data-ttu-id="e1878-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="e1878-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e1878-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1878-140">NOTES</span></span>

## <span data-ttu-id="e1878-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1878-141">RELATED LINKS</span></span>
