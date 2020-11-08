---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235788"
---
# <span data-ttu-id="5e953-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="5e953-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="5e953-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e953-102">SYNOPSIS</span></span>
<span data-ttu-id="5e953-103">Удаляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="5e953-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="5e953-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e953-104">SYNTAX</span></span>

### <span data-ttu-id="5e953-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5e953-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e953-106">Объект</span><span class="sxs-lookup"><span data-stu-id="5e953-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e953-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5e953-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e953-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e953-108">DESCRIPTION</span></span>
<span data-ttu-id="5e953-109">Командлет Remove-AzSqlElasticJobAgent удаляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="5e953-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="5e953-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e953-110">EXAMPLES</span></span>

### <span data-ttu-id="5e953-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e953-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="5e953-112">Удаление агента эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="5e953-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="5e953-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e953-113">PARAMETERS</span></span>

### <span data-ttu-id="5e953-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e953-114">-DefaultProfile</span></span>
<span data-ttu-id="5e953-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e953-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e953-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5e953-116">-Force</span></span>
<span data-ttu-id="5e953-117">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="5e953-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e953-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e953-118">-InputObject</span></span>
<span data-ttu-id="5e953-119">Объект Agent</span><span class="sxs-lookup"><span data-stu-id="5e953-119">The agent object</span></span>

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

### <span data-ttu-id="5e953-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e953-120">-Name</span></span>
<span data-ttu-id="5e953-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="5e953-121">The agent name</span></span>

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

### <span data-ttu-id="5e953-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e953-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e953-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5e953-123">The resource group name</span></span>

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

### <span data-ttu-id="5e953-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e953-124">-ResourceId</span></span>
<span data-ttu-id="5e953-125">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="5e953-125">The agent resource id</span></span>

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

### <span data-ttu-id="5e953-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5e953-126">-ServerName</span></span>
<span data-ttu-id="5e953-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="5e953-127">The server name</span></span>

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

### <span data-ttu-id="5e953-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e953-128">-Confirm</span></span>
<span data-ttu-id="5e953-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e953-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e953-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e953-130">-WhatIf</span></span>
<span data-ttu-id="5e953-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e953-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e953-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e953-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e953-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e953-133">CommonParameters</span></span>
<span data-ttu-id="5e953-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e953-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e953-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e953-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e953-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e953-136">INPUTS</span></span>

### <span data-ttu-id="5e953-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5e953-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5e953-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e953-138">OUTPUTS</span></span>

### <span data-ttu-id="5e953-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5e953-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5e953-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e953-140">NOTES</span></span>

## <span data-ttu-id="5e953-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e953-141">RELATED LINKS</span></span>
