---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 9918c314d239bf822fa789bcab6a9de923b8c2e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999635"
---
# <span data-ttu-id="89ec4-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="89ec4-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="89ec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="89ec4-103">Одно или несколько выполнения шага задания</span><span class="sxs-lookup"><span data-stu-id="89ec4-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="89ec4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89ec4-104">SYNTAX</span></span>

### <span data-ttu-id="89ec4-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89ec4-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89ec4-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="89ec4-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89ec4-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="89ec4-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ec4-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="89ec4-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ec4-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="89ec4-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ec4-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="89ec4-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89ec4-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ec4-111">DESCRIPTION</span></span>
<span data-ttu-id="89ec4-112">Для Get-AzSqlElasticJobStepExecution выполнения задания возвращается один или несколько этапов выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="89ec4-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="89ec4-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89ec4-113">EXAMPLES</span></span>

### <span data-ttu-id="89ec4-114">Пример 1. Возвращает одно или несколько выполнения шага задания из выполнения задания</span><span class="sxs-lookup"><span data-stu-id="89ec4-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="89ec4-115">Пример 2. Получает одно или несколько выполнения шага задания из выполнения задания с фильтрацией по имени шага</span><span class="sxs-lookup"><span data-stu-id="89ec4-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="89ec4-116">Одно или несколько выполнения шага задания</span><span class="sxs-lookup"><span data-stu-id="89ec4-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="89ec4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89ec4-117">PARAMETERS</span></span>

### <span data-ttu-id="89ec4-118">-Активные</span><span class="sxs-lookup"><span data-stu-id="89ec4-118">-Active</span></span>
<span data-ttu-id="89ec4-119">Пометка для фильтрации по активным выполнениям.</span><span class="sxs-lookup"><span data-stu-id="89ec4-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="89ec4-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="89ec4-120">-AgentName</span></span>
<span data-ttu-id="89ec4-121">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="89ec4-121">The agent name.</span></span>

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

### <span data-ttu-id="89ec4-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="89ec4-122">-CreateTimeMax</span></span>
<span data-ttu-id="89ec4-123">Максимальное время фильтрации</span><span class="sxs-lookup"><span data-stu-id="89ec4-123">Filter by create time max</span></span>

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

### <span data-ttu-id="89ec4-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="89ec4-124">-CreateTimeMin</span></span>
<span data-ttu-id="89ec4-125">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="89ec4-125">Filter by create time min</span></span>

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

### <span data-ttu-id="89ec4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ec4-126">-DefaultProfile</span></span>
<span data-ttu-id="89ec4-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89ec4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ec4-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="89ec4-128">-EndTimeMax</span></span>
<span data-ttu-id="89ec4-129">Максимальное время фильтрации.</span><span class="sxs-lookup"><span data-stu-id="89ec4-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="89ec4-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="89ec4-130">-EndTimeMin</span></span>
<span data-ttu-id="89ec4-131">Фильтрация по времени окончания мин.</span><span class="sxs-lookup"><span data-stu-id="89ec4-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="89ec4-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="89ec4-132">-JobExecutionId</span></span>
<span data-ttu-id="89ec4-133">ИД выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="89ec4-133">The job execution id.</span></span>

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

### <span data-ttu-id="89ec4-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="89ec4-134">-JobName</span></span>
<span data-ttu-id="89ec4-135">Имя задания.</span><span class="sxs-lookup"><span data-stu-id="89ec4-135">The job name.</span></span>

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

### <span data-ttu-id="89ec4-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="89ec4-136">-ParentObject</span></span>
<span data-ttu-id="89ec4-137">Объект агента.</span><span class="sxs-lookup"><span data-stu-id="89ec4-137">The agent object.</span></span>

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

### <span data-ttu-id="89ec4-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="89ec4-138">-ParentResourceId</span></span>
<span data-ttu-id="89ec4-139">ИД ресурса выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="89ec4-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="89ec4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ec4-140">-ResourceGroupName</span></span>
<span data-ttu-id="89ec4-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89ec4-141">The resource group name.</span></span>

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

### <span data-ttu-id="89ec4-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="89ec4-142">-ServerName</span></span>
<span data-ttu-id="89ec4-143">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="89ec4-143">The server name.</span></span>

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

### <span data-ttu-id="89ec4-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="89ec4-144">-StepName</span></span>
<span data-ttu-id="89ec4-145">Имя шага задания.</span><span class="sxs-lookup"><span data-stu-id="89ec4-145">The job step name.</span></span>

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

### <span data-ttu-id="89ec4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ec4-146">CommonParameters</span></span>
<span data-ttu-id="89ec4-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89ec4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ec4-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89ec4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ec4-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89ec4-149">INPUTS</span></span>

### <span data-ttu-id="89ec4-150">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="89ec4-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="89ec4-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89ec4-151">OUTPUTS</span></span>

### <span data-ttu-id="89ec4-152">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="89ec4-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="89ec4-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89ec4-153">NOTES</span></span>

## <span data-ttu-id="89ec4-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89ec4-154">RELATED LINKS</span></span>
