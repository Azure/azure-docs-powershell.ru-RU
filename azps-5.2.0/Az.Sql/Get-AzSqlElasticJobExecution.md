---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402871"
---
# <span data-ttu-id="7d68d-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="7d68d-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="7d68d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d68d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d68d-103">Одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="7d68d-103">Gets one or more job executions</span></span>

## <span data-ttu-id="7d68d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d68d-104">SYNTAX</span></span>

### <span data-ttu-id="7d68d-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d68d-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d68d-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="7d68d-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d68d-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7d68d-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d68d-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7d68d-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d68d-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7d68d-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d68d-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7d68d-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d68d-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d68d-111">DESCRIPTION</span></span>
<span data-ttu-id="7d68d-112">Этот Get-AzSqlElasticJobExecution возвращает одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="7d68d-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="7d68d-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d68d-113">EXAMPLES</span></span>

### <span data-ttu-id="7d68d-114">Пример 1. Возвращает одно или несколько выполнения заданий по всем заданиям</span><span class="sxs-lookup"><span data-stu-id="7d68d-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="7d68d-115">Пример 2. Возвращает одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="7d68d-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="7d68d-116">Одно или несколько выполнения задания</span><span class="sxs-lookup"><span data-stu-id="7d68d-116">Gets one or more job executions</span></span>

### <span data-ttu-id="7d68d-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7d68d-117">Example 3</span></span>

<span data-ttu-id="7d68d-118">Возвращает одно или несколько выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="7d68d-118">Gets one or more job executions.</span></span> <span data-ttu-id="7d68d-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="7d68d-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="7d68d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d68d-120">PARAMETERS</span></span>

### <span data-ttu-id="7d68d-121">-Активные</span><span class="sxs-lookup"><span data-stu-id="7d68d-121">-Active</span></span>
<span data-ttu-id="7d68d-122">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="7d68d-122">Filter by create time min</span></span>

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

### <span data-ttu-id="7d68d-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7d68d-123">-AgentName</span></span>
<span data-ttu-id="7d68d-124">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="7d68d-124">The agent name.</span></span>

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

### <span data-ttu-id="7d68d-125">-Count</span><span class="sxs-lookup"><span data-stu-id="7d68d-125">-Count</span></span>
<span data-ttu-id="7d68d-126">Count возвращает большее количество выполнения.</span><span class="sxs-lookup"><span data-stu-id="7d68d-126">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="7d68d-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="7d68d-127">-CreateTimeMax</span></span>
<span data-ttu-id="7d68d-128">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="7d68d-128">Filter by create time min</span></span>

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

### <span data-ttu-id="7d68d-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="7d68d-129">-CreateTimeMin</span></span>
<span data-ttu-id="7d68d-130">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="7d68d-130">Filter by create time min</span></span>

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

### <span data-ttu-id="7d68d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d68d-131">-DefaultProfile</span></span>
<span data-ttu-id="7d68d-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d68d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d68d-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="7d68d-133">-EndTimeMax</span></span>
<span data-ttu-id="7d68d-134">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="7d68d-134">Filter by create time min</span></span>

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

### <span data-ttu-id="7d68d-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="7d68d-135">-EndTimeMin</span></span>
<span data-ttu-id="7d68d-136">Фильтрация по создать мин времени</span><span class="sxs-lookup"><span data-stu-id="7d68d-136">Filter by create time min</span></span>

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

### <span data-ttu-id="7d68d-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="7d68d-137">-JobExecutionId</span></span>
<span data-ttu-id="7d68d-138">ИД выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="7d68d-138">The job execution id.</span></span>

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

### <span data-ttu-id="7d68d-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="7d68d-139">-JobName</span></span>
<span data-ttu-id="7d68d-140">Имя задания.</span><span class="sxs-lookup"><span data-stu-id="7d68d-140">The job name.</span></span>

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

### <span data-ttu-id="7d68d-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7d68d-141">-ParentObject</span></span>
<span data-ttu-id="7d68d-142">ИД выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="7d68d-142">The job execution id.</span></span>

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

### <span data-ttu-id="7d68d-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7d68d-143">-ParentResourceId</span></span>
<span data-ttu-id="7d68d-144">ИД агента ресурса.</span><span class="sxs-lookup"><span data-stu-id="7d68d-144">The agent resource id.</span></span>

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

### <span data-ttu-id="7d68d-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d68d-145">-ResourceGroupName</span></span>
<span data-ttu-id="7d68d-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d68d-146">The resource group name.</span></span>

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

### <span data-ttu-id="7d68d-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7d68d-147">-ServerName</span></span>
<span data-ttu-id="7d68d-148">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="7d68d-148">The server name.</span></span>

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

### <span data-ttu-id="7d68d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d68d-149">CommonParameters</span></span>
<span data-ttu-id="7d68d-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d68d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d68d-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d68d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d68d-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d68d-152">INPUTS</span></span>

### <span data-ttu-id="7d68d-153">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="7d68d-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="7d68d-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d68d-154">OUTPUTS</span></span>

### <span data-ttu-id="7d68d-155">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="7d68d-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="7d68d-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d68d-156">NOTES</span></span>

## <span data-ttu-id="7d68d-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d68d-157">RELATED LINKS</span></span>
