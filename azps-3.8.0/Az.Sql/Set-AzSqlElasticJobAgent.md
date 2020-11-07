---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912528"
---
# <span data-ttu-id="ceba5-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="ceba5-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="ceba5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ceba5-102">SYNOPSIS</span></span>
<span data-ttu-id="ceba5-103">Обновляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="ceba5-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="ceba5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ceba5-104">SYNTAX</span></span>

### <span data-ttu-id="ceba5-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ceba5-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceba5-106">Объект</span><span class="sxs-lookup"><span data-stu-id="ceba5-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceba5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ceba5-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceba5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceba5-108">DESCRIPTION</span></span>
<span data-ttu-id="ceba5-109">Командлет Set-AzSqlElasticJobAgent обновляет агенты эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="ceba5-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="ceba5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ceba5-110">EXAMPLES</span></span>

### <span data-ttu-id="ceba5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ceba5-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="ceba5-112">Обновляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="ceba5-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="ceba5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ceba5-113">PARAMETERS</span></span>

### <span data-ttu-id="ceba5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceba5-114">-DefaultProfile</span></span>
<span data-ttu-id="ceba5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ceba5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceba5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ceba5-116">-InputObject</span></span>
<span data-ttu-id="ceba5-117">Входной объект агента</span><span class="sxs-lookup"><span data-stu-id="ceba5-117">The agent input object</span></span>

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

### <span data-ttu-id="ceba5-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ceba5-118">-Name</span></span>
<span data-ttu-id="ceba5-119">Имя агента</span><span class="sxs-lookup"><span data-stu-id="ceba5-119">The agent name</span></span>

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

### <span data-ttu-id="ceba5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceba5-120">-ResourceGroupName</span></span>
<span data-ttu-id="ceba5-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ceba5-121">The resource group name</span></span>

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

### <span data-ttu-id="ceba5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ceba5-122">-ResourceId</span></span>
<span data-ttu-id="ceba5-123">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="ceba5-123">The agent resource id</span></span>

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

### <span data-ttu-id="ceba5-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ceba5-124">-ServerName</span></span>
<span data-ttu-id="ceba5-125">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="ceba5-125">The server name</span></span>

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

### <span data-ttu-id="ceba5-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="ceba5-126">-Tag</span></span>
<span data-ttu-id="ceba5-127">Теги, связываемые с агентом базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ceba5-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="ceba5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceba5-128">-Confirm</span></span>
<span data-ttu-id="ceba5-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ceba5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceba5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceba5-130">-WhatIf</span></span>
<span data-ttu-id="ceba5-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ceba5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceba5-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ceba5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceba5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceba5-133">CommonParameters</span></span>
<span data-ttu-id="ceba5-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ceba5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceba5-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ceba5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceba5-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ceba5-136">INPUTS</span></span>

### <span data-ttu-id="ceba5-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="ceba5-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="ceba5-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceba5-138">OUTPUTS</span></span>

### <span data-ttu-id="ceba5-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="ceba5-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="ceba5-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="ceba5-140">NOTES</span></span>

## <span data-ttu-id="ceba5-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ceba5-141">RELATED LINKS</span></span>
