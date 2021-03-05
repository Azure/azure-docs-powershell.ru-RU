---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 1279366f07ce071e223aea1f7cc048403b9b4379
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992368"
---
# <span data-ttu-id="4065f-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="4065f-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="4065f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4065f-102">SYNOPSIS</span></span>
<span data-ttu-id="4065f-103">Остановка задания с учетом его ид выполнения</span><span class="sxs-lookup"><span data-stu-id="4065f-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="4065f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4065f-104">SYNTAX</span></span>

### <span data-ttu-id="4065f-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4065f-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4065f-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4065f-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4065f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4065f-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4065f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4065f-108">DESCRIPTION</span></span>
<span data-ttu-id="4065f-109">Новый Stop-AzSqlElasticJob останавливает выполнение задания.</span><span class="sxs-lookup"><span data-stu-id="4065f-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="4065f-110">Возвращает текущее состояние выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="4065f-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="4065f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4065f-111">EXAMPLES</span></span>

### <span data-ttu-id="4065f-112">Пример 1. Остановка выполнения задания</span><span class="sxs-lookup"><span data-stu-id="4065f-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="4065f-113">Остановка выполнения задания и возврат текущего состояния</span><span class="sxs-lookup"><span data-stu-id="4065f-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="4065f-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4065f-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="4065f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4065f-115">PARAMETERS</span></span>

### <span data-ttu-id="4065f-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4065f-116">-AgentName</span></span>
<span data-ttu-id="4065f-117">Имя агента</span><span class="sxs-lookup"><span data-stu-id="4065f-117">The agent name</span></span>

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

### <span data-ttu-id="4065f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4065f-118">-DefaultProfile</span></span>
<span data-ttu-id="4065f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4065f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4065f-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="4065f-120">-JobExecutionId</span></span>
<span data-ttu-id="4065f-121">ИД выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="4065f-121">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4065f-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="4065f-122">-JobName</span></span>
<span data-ttu-id="4065f-123">Имя задания</span><span class="sxs-lookup"><span data-stu-id="4065f-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4065f-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4065f-124">-ParentObject</span></span>
<span data-ttu-id="4065f-125">Объект базы данных под управлением агента</span><span class="sxs-lookup"><span data-stu-id="4065f-125">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4065f-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4065f-126">-ParentResourceId</span></span>
<span data-ttu-id="4065f-127">ИД ресурса выполнения задания</span><span class="sxs-lookup"><span data-stu-id="4065f-127">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4065f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4065f-128">-ResourceGroupName</span></span>
<span data-ttu-id="4065f-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4065f-129">The resource group name</span></span>

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

### <span data-ttu-id="4065f-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4065f-130">-ServerName</span></span>
<span data-ttu-id="4065f-131">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="4065f-131">The server name</span></span>

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

### <span data-ttu-id="4065f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4065f-132">-Confirm</span></span>
<span data-ttu-id="4065f-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4065f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4065f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4065f-134">-WhatIf</span></span>
<span data-ttu-id="4065f-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4065f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4065f-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4065f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4065f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4065f-137">CommonParameters</span></span>
<span data-ttu-id="4065f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4065f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4065f-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4065f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4065f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4065f-140">INPUTS</span></span>

### <span data-ttu-id="4065f-141">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="4065f-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4065f-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4065f-142">OUTPUTS</span></span>

### <span data-ttu-id="4065f-143">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="4065f-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4065f-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4065f-144">NOTES</span></span>

## <span data-ttu-id="4065f-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4065f-145">RELATED LINKS</span></span>
