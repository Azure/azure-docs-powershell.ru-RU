---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 2913c390620e18fb1781b235edca9e4f50715cd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999667"
---
# <span data-ttu-id="2dc78-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="2dc78-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="2dc78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dc78-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc78-103">Одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="2dc78-103">Gets one or more job executions</span></span>

## <span data-ttu-id="2dc78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2dc78-104">SYNTAX</span></span>

### <span data-ttu-id="2dc78-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2dc78-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2dc78-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="2dc78-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dc78-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2dc78-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dc78-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2dc78-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dc78-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2dc78-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dc78-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2dc78-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dc78-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dc78-111">DESCRIPTION</span></span>
<span data-ttu-id="2dc78-112">Этот Get-AzSqlElasticJobExecution возвращает одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="2dc78-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="2dc78-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2dc78-113">EXAMPLES</span></span>

### <span data-ttu-id="2dc78-114">Пример 1. Возвращает одно или несколько выполнения заданий по всем заданиям</span><span class="sxs-lookup"><span data-stu-id="2dc78-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="2dc78-115">Пример 2. Возвращает одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="2dc78-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="2dc78-116">Одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="2dc78-116">Gets one or more job executions</span></span>

### <span data-ttu-id="2dc78-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2dc78-117">Example 3</span></span>

<span data-ttu-id="2dc78-118">Возвращает одно или несколько выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="2dc78-118">Gets one or more job executions.</span></span> <span data-ttu-id="2dc78-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2dc78-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="2dc78-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dc78-120">PARAMETERS</span></span>

### <span data-ttu-id="2dc78-121">-Активные</span><span class="sxs-lookup"><span data-stu-id="2dc78-121">-Active</span></span>
<span data-ttu-id="2dc78-122">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="2dc78-122">Filter by create time min</span></span>

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

### <span data-ttu-id="2dc78-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2dc78-123">-AgentName</span></span>
<span data-ttu-id="2dc78-124">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="2dc78-124">The agent name.</span></span>

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

### <span data-ttu-id="2dc78-125">-Count</span><span class="sxs-lookup"><span data-stu-id="2dc78-125">-Count</span></span>
<span data-ttu-id="2dc78-126">Count возвращает большее число выполнения.</span><span class="sxs-lookup"><span data-stu-id="2dc78-126">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="2dc78-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="2dc78-127">-CreateTimeMax</span></span>
<span data-ttu-id="2dc78-128">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="2dc78-128">Filter by create time min</span></span>

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

### <span data-ttu-id="2dc78-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="2dc78-129">-CreateTimeMin</span></span>
<span data-ttu-id="2dc78-130">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="2dc78-130">Filter by create time min</span></span>

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

### <span data-ttu-id="2dc78-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc78-131">-DefaultProfile</span></span>
<span data-ttu-id="2dc78-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dc78-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dc78-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="2dc78-133">-EndTimeMax</span></span>
<span data-ttu-id="2dc78-134">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="2dc78-134">Filter by create time min</span></span>

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

### <span data-ttu-id="2dc78-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="2dc78-135">-EndTimeMin</span></span>
<span data-ttu-id="2dc78-136">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="2dc78-136">Filter by create time min</span></span>

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

### <span data-ttu-id="2dc78-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="2dc78-137">-JobExecutionId</span></span>
<span data-ttu-id="2dc78-138">ИД выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="2dc78-138">The job execution id.</span></span>

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

### <span data-ttu-id="2dc78-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="2dc78-139">-JobName</span></span>
<span data-ttu-id="2dc78-140">Имя задания.</span><span class="sxs-lookup"><span data-stu-id="2dc78-140">The job name.</span></span>

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

### <span data-ttu-id="2dc78-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2dc78-141">-ParentObject</span></span>
<span data-ttu-id="2dc78-142">ИД выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="2dc78-142">The job execution id.</span></span>

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

### <span data-ttu-id="2dc78-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2dc78-143">-ParentResourceId</span></span>
<span data-ttu-id="2dc78-144">ИД агента ресурса.</span><span class="sxs-lookup"><span data-stu-id="2dc78-144">The agent resource id.</span></span>

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

### <span data-ttu-id="2dc78-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc78-145">-ResourceGroupName</span></span>
<span data-ttu-id="2dc78-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2dc78-146">The resource group name.</span></span>

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

### <span data-ttu-id="2dc78-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2dc78-147">-ServerName</span></span>
<span data-ttu-id="2dc78-148">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2dc78-148">The server name.</span></span>

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

### <span data-ttu-id="2dc78-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc78-149">CommonParameters</span></span>
<span data-ttu-id="2dc78-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc78-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc78-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dc78-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc78-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2dc78-152">INPUTS</span></span>

### <span data-ttu-id="2dc78-153">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2dc78-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2dc78-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2dc78-154">OUTPUTS</span></span>

### <span data-ttu-id="2dc78-155">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="2dc78-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2dc78-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2dc78-156">NOTES</span></span>

## <span data-ttu-id="2dc78-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dc78-157">RELATED LINKS</span></span>
