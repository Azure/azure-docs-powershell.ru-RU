---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078620"
---
# <span data-ttu-id="d6b28-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="d6b28-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="d6b28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6b28-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b28-103">Обновляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="d6b28-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="d6b28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6b28-104">SYNTAX</span></span>

### <span data-ttu-id="d6b28-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6b28-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b28-106">Объект</span><span class="sxs-lookup"><span data-stu-id="d6b28-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b28-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d6b28-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6b28-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6b28-108">DESCRIPTION</span></span>
<span data-ttu-id="d6b28-109">Командлет Set-AzSqlElasticJobAgent обновляет агенты эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="d6b28-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="d6b28-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6b28-110">EXAMPLES</span></span>

### <span data-ttu-id="d6b28-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6b28-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="d6b28-112">Обновляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="d6b28-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="d6b28-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6b28-113">PARAMETERS</span></span>

### <span data-ttu-id="d6b28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b28-114">-DefaultProfile</span></span>
<span data-ttu-id="d6b28-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6b28-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6b28-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6b28-116">-InputObject</span></span>
<span data-ttu-id="d6b28-117">Входной объект агента</span><span class="sxs-lookup"><span data-stu-id="d6b28-117">The agent input object</span></span>

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

### <span data-ttu-id="d6b28-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6b28-118">-Name</span></span>
<span data-ttu-id="d6b28-119">Имя агента</span><span class="sxs-lookup"><span data-stu-id="d6b28-119">The agent name</span></span>

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

### <span data-ttu-id="d6b28-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b28-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6b28-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d6b28-121">The resource group name</span></span>

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

### <span data-ttu-id="d6b28-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6b28-122">-ResourceId</span></span>
<span data-ttu-id="d6b28-123">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="d6b28-123">The agent resource id</span></span>

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

### <span data-ttu-id="d6b28-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d6b28-124">-ServerName</span></span>
<span data-ttu-id="d6b28-125">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="d6b28-125">The server name</span></span>

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

### <span data-ttu-id="d6b28-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="d6b28-126">-Tag</span></span>
<span data-ttu-id="d6b28-127">Теги, связываемые с агентом базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="d6b28-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="d6b28-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6b28-128">-Confirm</span></span>
<span data-ttu-id="d6b28-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6b28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6b28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b28-130">-WhatIf</span></span>
<span data-ttu-id="d6b28-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6b28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6b28-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6b28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6b28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b28-133">CommonParameters</span></span>
<span data-ttu-id="d6b28-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6b28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b28-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6b28-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b28-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6b28-136">INPUTS</span></span>

### <span data-ttu-id="d6b28-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d6b28-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d6b28-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6b28-138">OUTPUTS</span></span>

### <span data-ttu-id="d6b28-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d6b28-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d6b28-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6b28-140">NOTES</span></span>

## <span data-ttu-id="d6b28-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6b28-141">RELATED LINKS</span></span>
