---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 6e61a83d843e0ceaa7d7926060da848d80d16eae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211001"
---
# <span data-ttu-id="04c71-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="04c71-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="04c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04c71-102">SYNOPSIS</span></span>
<span data-ttu-id="04c71-103">Возвращает одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="04c71-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="04c71-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="04c71-104">SYNTAX</span></span>

### <span data-ttu-id="04c71-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04c71-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04c71-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="04c71-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04c71-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="04c71-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c71-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04c71-108">DESCRIPTION</span></span>
<span data-ttu-id="04c71-109">Этот Get-AzSqlElasticJobTargetExecution получает одно или несколько целевых выполнения задания из выполнения задания</span><span class="sxs-lookup"><span data-stu-id="04c71-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="04c71-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="04c71-110">EXAMPLES</span></span>

### <span data-ttu-id="04c71-111">Пример 1. Возвращает одно или несколько целевых выполнения задания из выполнения задания</span><span class="sxs-lookup"><span data-stu-id="04c71-111">Example 1: Gets one or more job target executions from a job executions</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="04c71-112">Пример 2. Возвращает одно или несколько целевых выполнения задания из выполнения задания — фильтрация по имени шага</span><span class="sxs-lookup"><span data-stu-id="04c71-112">Example 2: Gets one or more job target executions from a job executions - filtering by step name</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="04c71-113">Возвращает одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="04c71-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="04c71-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04c71-114">PARAMETERS</span></span>

### <span data-ttu-id="04c71-115">-Активные</span><span class="sxs-lookup"><span data-stu-id="04c71-115">-Active</span></span>
<span data-ttu-id="04c71-116">Пометка для фильтрации по активным выполнениям.</span><span class="sxs-lookup"><span data-stu-id="04c71-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="04c71-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="04c71-117">-AgentName</span></span>
<span data-ttu-id="04c71-118">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="04c71-118">The agent name.</span></span>

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

### <span data-ttu-id="04c71-119">-Count</span><span class="sxs-lookup"><span data-stu-id="04c71-119">-Count</span></span>
<span data-ttu-id="04c71-120">Count возвращает большее число выполнения.</span><span class="sxs-lookup"><span data-stu-id="04c71-120">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c71-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="04c71-121">-CreateTimeMax</span></span>
<span data-ttu-id="04c71-122">Максимальное время фильтрации</span><span class="sxs-lookup"><span data-stu-id="04c71-122">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c71-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="04c71-123">-CreateTimeMin</span></span>
<span data-ttu-id="04c71-124">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="04c71-124">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c71-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c71-125">-DefaultProfile</span></span>
<span data-ttu-id="04c71-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04c71-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04c71-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="04c71-127">-EndTimeMax</span></span>
<span data-ttu-id="04c71-128">Максимальное время фильтрации.</span><span class="sxs-lookup"><span data-stu-id="04c71-128">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c71-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="04c71-129">-EndTimeMin</span></span>
<span data-ttu-id="04c71-130">Фильтрация по времени окончания мин.</span><span class="sxs-lookup"><span data-stu-id="04c71-130">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c71-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="04c71-131">-JobExecutionId</span></span>
<span data-ttu-id="04c71-132">ИД выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="04c71-132">The job execution id.</span></span>

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

### <span data-ttu-id="04c71-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="04c71-133">-JobName</span></span>
<span data-ttu-id="04c71-134">Имя задания.</span><span class="sxs-lookup"><span data-stu-id="04c71-134">The job name.</span></span>

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

### <span data-ttu-id="04c71-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="04c71-135">-ParentObject</span></span>
<span data-ttu-id="04c71-136">Объект выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="04c71-136">The job execution object.</span></span>

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

### <span data-ttu-id="04c71-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="04c71-137">-ParentResourceId</span></span>
<span data-ttu-id="04c71-138">ИД ресурса выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="04c71-138">The job execution resource id.</span></span>

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

### <span data-ttu-id="04c71-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c71-139">-ResourceGroupName</span></span>
<span data-ttu-id="04c71-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04c71-140">The resource group name.</span></span>

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

### <span data-ttu-id="04c71-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="04c71-141">-ServerName</span></span>
<span data-ttu-id="04c71-142">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="04c71-142">The server name.</span></span>

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

### <span data-ttu-id="04c71-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="04c71-143">-StepName</span></span>
<span data-ttu-id="04c71-144">Имя шага задания.</span><span class="sxs-lookup"><span data-stu-id="04c71-144">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c71-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c71-145">CommonParameters</span></span>
<span data-ttu-id="04c71-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c71-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c71-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04c71-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c71-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04c71-148">INPUTS</span></span>

### <span data-ttu-id="04c71-149">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="04c71-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="04c71-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04c71-150">OUTPUTS</span></span>

### <span data-ttu-id="04c71-151">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="04c71-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="04c71-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="04c71-152">NOTES</span></span>

## <span data-ttu-id="04c71-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04c71-153">RELATED LINKS</span></span>
