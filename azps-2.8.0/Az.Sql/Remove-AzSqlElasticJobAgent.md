---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 5f8b237a6f7d08fc0339d3ba34d253bc457dd49f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906534"
---
# <span data-ttu-id="955aa-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="955aa-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="955aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="955aa-102">SYNOPSIS</span></span>
<span data-ttu-id="955aa-103">Удаляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="955aa-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="955aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="955aa-104">SYNTAX</span></span>

### <span data-ttu-id="955aa-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="955aa-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955aa-106">Объект</span><span class="sxs-lookup"><span data-stu-id="955aa-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955aa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="955aa-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="955aa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="955aa-108">DESCRIPTION</span></span>
<span data-ttu-id="955aa-109">Командлет Remove-AzSqlElasticJobAgent удаляет агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="955aa-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="955aa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="955aa-110">EXAMPLES</span></span>

### <span data-ttu-id="955aa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="955aa-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="955aa-112">Удаление агента эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="955aa-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="955aa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="955aa-113">PARAMETERS</span></span>

### <span data-ttu-id="955aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955aa-114">-DefaultProfile</span></span>
<span data-ttu-id="955aa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="955aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="955aa-116">-Force</span><span class="sxs-lookup"><span data-stu-id="955aa-116">-Force</span></span>
<span data-ttu-id="955aa-117">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="955aa-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="955aa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="955aa-118">-InputObject</span></span>
<span data-ttu-id="955aa-119">Объект Agent</span><span class="sxs-lookup"><span data-stu-id="955aa-119">The agent object</span></span>

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

### <span data-ttu-id="955aa-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="955aa-120">-Name</span></span>
<span data-ttu-id="955aa-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="955aa-121">The agent name</span></span>

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

### <span data-ttu-id="955aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="955aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="955aa-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="955aa-123">The resource group name</span></span>

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

### <span data-ttu-id="955aa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="955aa-124">-ResourceId</span></span>
<span data-ttu-id="955aa-125">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="955aa-125">The agent resource id</span></span>

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

### <span data-ttu-id="955aa-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="955aa-126">-ServerName</span></span>
<span data-ttu-id="955aa-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="955aa-127">The server name</span></span>

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

### <span data-ttu-id="955aa-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="955aa-128">-Confirm</span></span>
<span data-ttu-id="955aa-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="955aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="955aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="955aa-130">-WhatIf</span></span>
<span data-ttu-id="955aa-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="955aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="955aa-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="955aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="955aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955aa-133">CommonParameters</span></span>
<span data-ttu-id="955aa-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="955aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955aa-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="955aa-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955aa-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="955aa-136">INPUTS</span></span>

### <span data-ttu-id="955aa-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="955aa-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="955aa-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="955aa-138">OUTPUTS</span></span>

### <span data-ttu-id="955aa-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="955aa-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="955aa-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="955aa-140">NOTES</span></span>

## <span data-ttu-id="955aa-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="955aa-141">RELATED LINKS</span></span>
