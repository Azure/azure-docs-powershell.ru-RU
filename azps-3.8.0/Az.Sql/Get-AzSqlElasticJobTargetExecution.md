---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 566bfb8caae85c6f4e6ef75a38bdd5363ddb1eaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912939"
---
# <span data-ttu-id="1d587-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="1d587-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="1d587-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d587-102">SYNOPSIS</span></span>
<span data-ttu-id="1d587-103">Получение одного или нескольких выполнения целевых целей задания</span><span class="sxs-lookup"><span data-stu-id="1d587-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="1d587-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d587-104">SYNTAX</span></span>

### <span data-ttu-id="1d587-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d587-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d587-106">Объект</span><span class="sxs-lookup"><span data-stu-id="1d587-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d587-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1d587-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d587-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d587-108">DESCRIPTION</span></span>
<span data-ttu-id="1d587-109">Командлет Get-AzSqlElasticJobTargetExecution получает одно или несколько выполнения целевых целей задания из выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="1d587-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="1d587-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d587-110">EXAMPLES</span></span>

### <span data-ttu-id="1d587-111">Пример 1 — получение одного или нескольких выполнения целевых целей задания из выполнения задания</span><span class="sxs-lookup"><span data-stu-id="1d587-111">Example 1 - Gets one or more job target executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="1d587-112">Пример 2 — получение одного или нескольких выполнения целевых целей задания с помощью выполнения задания — фильтрация по названию этапа</span><span class="sxs-lookup"><span data-stu-id="1d587-112">Example 2 - Gets one or more job target executions from a job executions - filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="1d587-113">Получение одного или нескольких выполнения целевых целей задания</span><span class="sxs-lookup"><span data-stu-id="1d587-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="1d587-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d587-114">PARAMETERS</span></span>

### <span data-ttu-id="1d587-115">-Активный</span><span class="sxs-lookup"><span data-stu-id="1d587-115">-Active</span></span>
<span data-ttu-id="1d587-116">Отметка для фильтрации по активным выполнению.</span><span class="sxs-lookup"><span data-stu-id="1d587-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="1d587-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1d587-117">-AgentName</span></span>
<span data-ttu-id="1d587-118">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="1d587-118">The agent name.</span></span>

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

### <span data-ttu-id="1d587-119">— Количество</span><span class="sxs-lookup"><span data-stu-id="1d587-119">-Count</span></span>
<span data-ttu-id="1d587-120">Функция Count возвращает наибольшее количество выполнений.</span><span class="sxs-lookup"><span data-stu-id="1d587-120">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="1d587-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="1d587-121">-CreateTimeMax</span></span>
<span data-ttu-id="1d587-122">Фильтрация по времени создания Макс.</span><span class="sxs-lookup"><span data-stu-id="1d587-122">Filter by create time max</span></span>

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

### <span data-ttu-id="1d587-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="1d587-123">-CreateTimeMin</span></span>
<span data-ttu-id="1d587-124">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="1d587-124">Filter by create time min</span></span>

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

### <span data-ttu-id="1d587-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d587-125">-DefaultProfile</span></span>
<span data-ttu-id="1d587-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d587-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d587-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="1d587-127">-EndTimeMax</span></span>
<span data-ttu-id="1d587-128">Фильтрация по времени окончания (Макс.)</span><span class="sxs-lookup"><span data-stu-id="1d587-128">Filter by end time max.</span></span>

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

### <span data-ttu-id="1d587-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="1d587-129">-EndTimeMin</span></span>
<span data-ttu-id="1d587-130">Отфильтровать по времени окончания (мин.)</span><span class="sxs-lookup"><span data-stu-id="1d587-130">Filter by end time min.</span></span>

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

### <span data-ttu-id="1d587-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="1d587-131">-JobExecutionId</span></span>
<span data-ttu-id="1d587-132">Идентификатор выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="1d587-132">The job execution id.</span></span>

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

### <span data-ttu-id="1d587-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="1d587-133">-JobName</span></span>
<span data-ttu-id="1d587-134">Имя задания.</span><span class="sxs-lookup"><span data-stu-id="1d587-134">The job name.</span></span>

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

### <span data-ttu-id="1d587-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1d587-135">-ParentObject</span></span>
<span data-ttu-id="1d587-136">Объект выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="1d587-136">The job execution object.</span></span>

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

### <span data-ttu-id="1d587-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1d587-137">-ParentResourceId</span></span>
<span data-ttu-id="1d587-138">Идентификатор ресурса выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="1d587-138">The job execution resource id.</span></span>

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

### <span data-ttu-id="1d587-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d587-139">-ResourceGroupName</span></span>
<span data-ttu-id="1d587-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d587-140">The resource group name.</span></span>

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

### <span data-ttu-id="1d587-141">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1d587-141">-ServerName</span></span>
<span data-ttu-id="1d587-142">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="1d587-142">The server name.</span></span>

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

### <span data-ttu-id="1d587-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="1d587-143">-StepName</span></span>
<span data-ttu-id="1d587-144">Имя шага задания.</span><span class="sxs-lookup"><span data-stu-id="1d587-144">The job step name.</span></span>

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

### <span data-ttu-id="1d587-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d587-145">CommonParameters</span></span>
<span data-ttu-id="1d587-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d587-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d587-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d587-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d587-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d587-148">INPUTS</span></span>

### <span data-ttu-id="1d587-149">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="1d587-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="1d587-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d587-150">OUTPUTS</span></span>

### <span data-ttu-id="1d587-151">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="1d587-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="1d587-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d587-152">NOTES</span></span>

## <span data-ttu-id="1d587-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d587-153">RELATED LINKS</span></span>
