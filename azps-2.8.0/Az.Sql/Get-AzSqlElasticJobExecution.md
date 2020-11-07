---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 5b5837fb0c5fa56e8e8f9887b6d85bfc3a3a559c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906162"
---
# <span data-ttu-id="5ac94-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="5ac94-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="5ac94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ac94-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac94-103">Получение одного или нескольких выполнения заданий</span><span class="sxs-lookup"><span data-stu-id="5ac94-103">Gets one or more job executions</span></span>

## <span data-ttu-id="5ac94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ac94-104">SYNTAX</span></span>

### <span data-ttu-id="5ac94-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ac94-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac94-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="5ac94-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac94-107">Объект</span><span class="sxs-lookup"><span data-stu-id="5ac94-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac94-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5ac94-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac94-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5ac94-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac94-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac94-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ac94-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ac94-111">DESCRIPTION</span></span>
<span data-ttu-id="5ac94-112">Командлет Get-AzSqlElasticJobExecution возвращает одно или несколько выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="5ac94-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="5ac94-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ac94-113">EXAMPLES</span></span>

### <span data-ttu-id="5ac94-114">Пример 1 — получение одного или нескольких выполняемых заданий во всех заданиях</span><span class="sxs-lookup"><span data-stu-id="5ac94-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="5ac94-115">Пример 2: получение одного или нескольких выполнения задания для задания</span><span class="sxs-lookup"><span data-stu-id="5ac94-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="5ac94-116">Получение одного или нескольких выполнения заданий</span><span class="sxs-lookup"><span data-stu-id="5ac94-116">Gets one or more job executions</span></span>

## <span data-ttu-id="5ac94-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ac94-117">PARAMETERS</span></span>

### <span data-ttu-id="5ac94-118">-Активный</span><span class="sxs-lookup"><span data-stu-id="5ac94-118">-Active</span></span>
<span data-ttu-id="5ac94-119">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="5ac94-119">Filter by create time min</span></span>

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

### <span data-ttu-id="5ac94-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5ac94-120">-AgentName</span></span>
<span data-ttu-id="5ac94-121">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="5ac94-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac94-122">— Количество</span><span class="sxs-lookup"><span data-stu-id="5ac94-122">-Count</span></span>
<span data-ttu-id="5ac94-123">Функция Count возвращает наибольшее количество выполнений.</span><span class="sxs-lookup"><span data-stu-id="5ac94-123">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac94-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="5ac94-124">-CreateTimeMax</span></span>
<span data-ttu-id="5ac94-125">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="5ac94-125">Filter by create time min</span></span>

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

### <span data-ttu-id="5ac94-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="5ac94-126">-CreateTimeMin</span></span>
<span data-ttu-id="5ac94-127">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="5ac94-127">Filter by create time min</span></span>

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

### <span data-ttu-id="5ac94-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac94-128">-DefaultProfile</span></span>
<span data-ttu-id="5ac94-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac94-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ac94-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="5ac94-130">-EndTimeMax</span></span>
<span data-ttu-id="5ac94-131">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="5ac94-131">Filter by create time min</span></span>

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

### <span data-ttu-id="5ac94-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="5ac94-132">-EndTimeMin</span></span>
<span data-ttu-id="5ac94-133">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="5ac94-133">Filter by create time min</span></span>

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

### <span data-ttu-id="5ac94-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="5ac94-134">-JobExecutionId</span></span>
<span data-ttu-id="5ac94-135">Идентификатор выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="5ac94-135">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac94-136">-JobName</span><span class="sxs-lookup"><span data-stu-id="5ac94-136">-JobName</span></span>
<span data-ttu-id="5ac94-137">Имя задания.</span><span class="sxs-lookup"><span data-stu-id="5ac94-137">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac94-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5ac94-138">-ParentObject</span></span>
<span data-ttu-id="5ac94-139">Идентификатор выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="5ac94-139">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac94-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac94-140">-ParentResourceId</span></span>
<span data-ttu-id="5ac94-141">Идентификатор ресурса агента.</span><span class="sxs-lookup"><span data-stu-id="5ac94-141">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac94-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac94-142">-ResourceGroupName</span></span>
<span data-ttu-id="5ac94-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ac94-143">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac94-144">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5ac94-144">-ServerName</span></span>
<span data-ttu-id="5ac94-145">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5ac94-145">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac94-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac94-146">CommonParameters</span></span>
<span data-ttu-id="5ac94-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ac94-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac94-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ac94-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac94-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ac94-149">INPUTS</span></span>

### <span data-ttu-id="5ac94-150">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5ac94-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5ac94-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ac94-151">OUTPUTS</span></span>

### <span data-ttu-id="5ac94-152">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="5ac94-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="5ac94-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ac94-153">NOTES</span></span>

## <span data-ttu-id="5ac94-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ac94-154">RELATED LINKS</span></span>
