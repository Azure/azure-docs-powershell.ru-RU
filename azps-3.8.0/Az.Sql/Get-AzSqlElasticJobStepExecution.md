---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912944"
---
# <span data-ttu-id="79dce-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="79dce-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="79dce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79dce-102">SYNOPSIS</span></span>
<span data-ttu-id="79dce-103">Получение одного или нескольких выполнения шагов задания</span><span class="sxs-lookup"><span data-stu-id="79dce-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="79dce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79dce-104">SYNTAX</span></span>

### <span data-ttu-id="79dce-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79dce-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79dce-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="79dce-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79dce-107">Объект</span><span class="sxs-lookup"><span data-stu-id="79dce-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79dce-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="79dce-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79dce-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="79dce-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79dce-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="79dce-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79dce-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79dce-111">DESCRIPTION</span></span>
<span data-ttu-id="79dce-112">Командлет Get-AzSqlElasticJobStepExecution возвращает одно или несколько выполненных шагов задания из выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="79dce-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="79dce-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79dce-113">EXAMPLES</span></span>

### <span data-ttu-id="79dce-114">Пример 1 — получение одного или нескольких выполненных шагов задания из выполнения задания</span><span class="sxs-lookup"><span data-stu-id="79dce-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="79dce-115">Пример 2 — получение одного или нескольких выполнения шагов задания из выполнения задания с фильтрацией по имени шага</span><span class="sxs-lookup"><span data-stu-id="79dce-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="79dce-116">Получение одного или нескольких выполнения шагов задания</span><span class="sxs-lookup"><span data-stu-id="79dce-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="79dce-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79dce-117">PARAMETERS</span></span>

### <span data-ttu-id="79dce-118">-Активный</span><span class="sxs-lookup"><span data-stu-id="79dce-118">-Active</span></span>
<span data-ttu-id="79dce-119">Отметка для фильтрации по активным выполнению.</span><span class="sxs-lookup"><span data-stu-id="79dce-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="79dce-120">-AgentName</span></span>
<span data-ttu-id="79dce-121">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="79dce-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="79dce-122">-CreateTimeMax</span></span>
<span data-ttu-id="79dce-123">Фильтрация по времени создания Макс.</span><span class="sxs-lookup"><span data-stu-id="79dce-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="79dce-124">-CreateTimeMin</span></span>
<span data-ttu-id="79dce-125">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="79dce-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79dce-126">-DefaultProfile</span></span>
<span data-ttu-id="79dce-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79dce-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79dce-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="79dce-128">-EndTimeMax</span></span>
<span data-ttu-id="79dce-129">Фильтрация по времени окончания (Макс.)</span><span class="sxs-lookup"><span data-stu-id="79dce-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="79dce-130">-EndTimeMin</span></span>
<span data-ttu-id="79dce-131">Отфильтровать по времени окончания (мин.)</span><span class="sxs-lookup"><span data-stu-id="79dce-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="79dce-132">-JobExecutionId</span></span>
<span data-ttu-id="79dce-133">Идентификатор выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="79dce-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="79dce-134">-JobName</span></span>
<span data-ttu-id="79dce-135">Имя задания.</span><span class="sxs-lookup"><span data-stu-id="79dce-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79dce-136">-ParentObject</span></span>
<span data-ttu-id="79dce-137">Объект агента.</span><span class="sxs-lookup"><span data-stu-id="79dce-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="79dce-138">-ParentResourceId</span></span>
<span data-ttu-id="79dce-139">Идентификатор ресурса выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="79dce-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79dce-140">-ResourceGroupName</span></span>
<span data-ttu-id="79dce-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79dce-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-142">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="79dce-142">-ServerName</span></span>
<span data-ttu-id="79dce-143">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="79dce-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="79dce-144">-StepName</span></span>
<span data-ttu-id="79dce-145">Имя шага задания.</span><span class="sxs-lookup"><span data-stu-id="79dce-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dce-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79dce-146">CommonParameters</span></span>
<span data-ttu-id="79dce-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79dce-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79dce-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79dce-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79dce-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79dce-149">INPUTS</span></span>

### <span data-ttu-id="79dce-150">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="79dce-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="79dce-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79dce-151">OUTPUTS</span></span>

### <span data-ttu-id="79dce-152">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="79dce-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="79dce-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="79dce-153">NOTES</span></span>

## <span data-ttu-id="79dce-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79dce-154">RELATED LINKS</span></span>
