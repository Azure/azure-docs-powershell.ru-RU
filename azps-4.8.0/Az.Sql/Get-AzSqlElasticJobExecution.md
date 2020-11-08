---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236604"
---
# <span data-ttu-id="69c15-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="69c15-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="69c15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69c15-102">SYNOPSIS</span></span>
<span data-ttu-id="69c15-103">Получение одного или нескольких выполнения заданий</span><span class="sxs-lookup"><span data-stu-id="69c15-103">Gets one or more job executions</span></span>

## <span data-ttu-id="69c15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69c15-104">SYNTAX</span></span>

### <span data-ttu-id="69c15-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69c15-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69c15-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="69c15-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69c15-107">Объект</span><span class="sxs-lookup"><span data-stu-id="69c15-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69c15-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="69c15-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69c15-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="69c15-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69c15-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="69c15-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69c15-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69c15-111">DESCRIPTION</span></span>
<span data-ttu-id="69c15-112">Командлет Get-AzSqlElasticJobExecution возвращает одно или несколько выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="69c15-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="69c15-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69c15-113">EXAMPLES</span></span>

### <span data-ttu-id="69c15-114">Пример 1: получение одного или нескольких выполнения заданий во всех заданиях</span><span class="sxs-lookup"><span data-stu-id="69c15-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="69c15-115">Пример 2: получение одного или нескольких выполнения задания для задания</span><span class="sxs-lookup"><span data-stu-id="69c15-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="69c15-116">Получение одного или нескольких выполнения заданий</span><span class="sxs-lookup"><span data-stu-id="69c15-116">Gets one or more job executions</span></span>

### <span data-ttu-id="69c15-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="69c15-117">Example 3</span></span>

<span data-ttu-id="69c15-118">Получает одно или несколько выполнения заданий.</span><span class="sxs-lookup"><span data-stu-id="69c15-118">Gets one or more job executions.</span></span> <span data-ttu-id="69c15-119">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="69c15-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="69c15-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69c15-120">PARAMETERS</span></span>

### <span data-ttu-id="69c15-121">-Активный</span><span class="sxs-lookup"><span data-stu-id="69c15-121">-Active</span></span>
<span data-ttu-id="69c15-122">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="69c15-122">Filter by create time min</span></span>

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

### <span data-ttu-id="69c15-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="69c15-123">-AgentName</span></span>
<span data-ttu-id="69c15-124">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="69c15-124">The agent name.</span></span>

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

### <span data-ttu-id="69c15-125">— Количество</span><span class="sxs-lookup"><span data-stu-id="69c15-125">-Count</span></span>
<span data-ttu-id="69c15-126">Функция Count возвращает наибольшее количество выполнений.</span><span class="sxs-lookup"><span data-stu-id="69c15-126">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="69c15-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="69c15-127">-CreateTimeMax</span></span>
<span data-ttu-id="69c15-128">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="69c15-128">Filter by create time min</span></span>

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

### <span data-ttu-id="69c15-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="69c15-129">-CreateTimeMin</span></span>
<span data-ttu-id="69c15-130">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="69c15-130">Filter by create time min</span></span>

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

### <span data-ttu-id="69c15-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c15-131">-DefaultProfile</span></span>
<span data-ttu-id="69c15-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69c15-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69c15-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="69c15-133">-EndTimeMax</span></span>
<span data-ttu-id="69c15-134">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="69c15-134">Filter by create time min</span></span>

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

### <span data-ttu-id="69c15-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="69c15-135">-EndTimeMin</span></span>
<span data-ttu-id="69c15-136">Фильтрация по времени создания (мин)</span><span class="sxs-lookup"><span data-stu-id="69c15-136">Filter by create time min</span></span>

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

### <span data-ttu-id="69c15-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="69c15-137">-JobExecutionId</span></span>
<span data-ttu-id="69c15-138">Идентификатор выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="69c15-138">The job execution id.</span></span>

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

### <span data-ttu-id="69c15-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="69c15-139">-JobName</span></span>
<span data-ttu-id="69c15-140">Имя задания.</span><span class="sxs-lookup"><span data-stu-id="69c15-140">The job name.</span></span>

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

### <span data-ttu-id="69c15-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="69c15-141">-ParentObject</span></span>
<span data-ttu-id="69c15-142">Идентификатор выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="69c15-142">The job execution id.</span></span>

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

### <span data-ttu-id="69c15-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="69c15-143">-ParentResourceId</span></span>
<span data-ttu-id="69c15-144">Идентификатор ресурса агента.</span><span class="sxs-lookup"><span data-stu-id="69c15-144">The agent resource id.</span></span>

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

### <span data-ttu-id="69c15-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c15-145">-ResourceGroupName</span></span>
<span data-ttu-id="69c15-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69c15-146">The resource group name.</span></span>

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

### <span data-ttu-id="69c15-147">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="69c15-147">-ServerName</span></span>
<span data-ttu-id="69c15-148">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="69c15-148">The server name.</span></span>

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

### <span data-ttu-id="69c15-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c15-149">CommonParameters</span></span>
<span data-ttu-id="69c15-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69c15-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c15-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69c15-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c15-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69c15-152">INPUTS</span></span>

### <span data-ttu-id="69c15-153">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="69c15-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="69c15-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69c15-154">OUTPUTS</span></span>

### <span data-ttu-id="69c15-155">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="69c15-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="69c15-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="69c15-156">NOTES</span></span>

## <span data-ttu-id="69c15-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69c15-157">RELATED LINKS</span></span>
