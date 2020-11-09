---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316931"
---
# <span data-ttu-id="9ef81-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="9ef81-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="9ef81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ef81-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef81-103">Обновляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="9ef81-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="9ef81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ef81-104">SYNTAX</span></span>

### <span data-ttu-id="9ef81-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ef81-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef81-106">Объект</span><span class="sxs-lookup"><span data-stu-id="9ef81-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef81-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9ef81-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ef81-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ef81-108">DESCRIPTION</span></span>
<span data-ttu-id="9ef81-109">Командлет Set-AzSqlElasticJobAgent обновляет агенты эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="9ef81-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="9ef81-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ef81-110">EXAMPLES</span></span>

### <span data-ttu-id="9ef81-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ef81-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="9ef81-112">Обновляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="9ef81-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="9ef81-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ef81-113">PARAMETERS</span></span>

### <span data-ttu-id="9ef81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef81-114">-DefaultProfile</span></span>
<span data-ttu-id="9ef81-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ef81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ef81-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ef81-116">-InputObject</span></span>
<span data-ttu-id="9ef81-117">Входной объект агента</span><span class="sxs-lookup"><span data-stu-id="9ef81-117">The agent input object</span></span>

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

### <span data-ttu-id="9ef81-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ef81-118">-Name</span></span>
<span data-ttu-id="9ef81-119">Имя агента</span><span class="sxs-lookup"><span data-stu-id="9ef81-119">The agent name</span></span>

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

### <span data-ttu-id="9ef81-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef81-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ef81-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9ef81-121">The resource group name</span></span>

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

### <span data-ttu-id="9ef81-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ef81-122">-ResourceId</span></span>
<span data-ttu-id="9ef81-123">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="9ef81-123">The agent resource id</span></span>

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

### <span data-ttu-id="9ef81-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9ef81-124">-ServerName</span></span>
<span data-ttu-id="9ef81-125">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="9ef81-125">The server name</span></span>

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

### <span data-ttu-id="9ef81-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="9ef81-126">-Tag</span></span>
<span data-ttu-id="9ef81-127">Теги, связываемые с агентом базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="9ef81-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="9ef81-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ef81-128">-Confirm</span></span>
<span data-ttu-id="9ef81-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ef81-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef81-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef81-130">-WhatIf</span></span>
<span data-ttu-id="9ef81-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ef81-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef81-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ef81-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef81-133">CommonParameters</span></span>
<span data-ttu-id="9ef81-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ef81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef81-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ef81-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef81-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ef81-136">INPUTS</span></span>

### <span data-ttu-id="9ef81-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="9ef81-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="9ef81-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ef81-138">OUTPUTS</span></span>

### <span data-ttu-id="9ef81-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="9ef81-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="9ef81-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ef81-140">NOTES</span></span>

## <span data-ttu-id="9ef81-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ef81-141">RELATED LINKS</span></span>
