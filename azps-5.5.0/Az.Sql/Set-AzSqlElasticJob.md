---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230044"
---
# <span data-ttu-id="da1a0-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="da1a0-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="da1a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="da1a0-103">Обновление задания</span><span class="sxs-lookup"><span data-stu-id="da1a0-103">Updates a job</span></span>

## <span data-ttu-id="da1a0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da1a0-104">SYNTAX</span></span>

### <span data-ttu-id="da1a0-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da1a0-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1a0-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="da1a0-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1a0-107">Повторяющийся</span><span class="sxs-lookup"><span data-stu-id="da1a0-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1a0-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="da1a0-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da1a0-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="da1a0-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1a0-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="da1a0-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1a0-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="da1a0-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1a0-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="da1a0-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1a0-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="da1a0-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da1a0-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da1a0-114">DESCRIPTION</span></span>
<span data-ttu-id="da1a0-115">Новый Set-AzSqlElasticJob-код обновляет задание</span><span class="sxs-lookup"><span data-stu-id="da1a0-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="da1a0-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da1a0-116">EXAMPLES</span></span>

### <span data-ttu-id="da1a0-117">Пример 1. Обновляет задание, чтобы начать задание через час и повторять его каждые 1 час</span><span class="sxs-lookup"><span data-stu-id="da1a0-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="da1a0-118">Обновление задания</span><span class="sxs-lookup"><span data-stu-id="da1a0-118">Updates a job</span></span>

### <span data-ttu-id="da1a0-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="da1a0-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="da1a0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da1a0-120">PARAMETERS</span></span>

### <span data-ttu-id="da1a0-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="da1a0-121">-AgentName</span></span>
<span data-ttu-id="da1a0-122">Имя агента</span><span class="sxs-lookup"><span data-stu-id="da1a0-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1a0-123">-DefaultProfile</span></span>
<span data-ttu-id="da1a0-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da1a0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da1a0-125">-Description</span><span class="sxs-lookup"><span data-stu-id="da1a0-125">-Description</span></span>
<span data-ttu-id="da1a0-126">Описание должности</span><span class="sxs-lookup"><span data-stu-id="da1a0-126">The job description</span></span>

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

### <span data-ttu-id="da1a0-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="da1a0-127">-Enable</span></span>
<span data-ttu-id="da1a0-128">Флажок, который указывает, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="da1a0-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="da1a0-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="da1a0-129">-EndTime</span></span>
<span data-ttu-id="da1a0-130">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="da1a0-130">The job schedule end time</span></span>

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

### <span data-ttu-id="da1a0-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da1a0-131">-InputObject</span></span>
<span data-ttu-id="da1a0-132">Объект ввода задания</span><span class="sxs-lookup"><span data-stu-id="da1a0-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da1a0-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="da1a0-133">-IntervalCount</span></span>
<span data-ttu-id="da1a0-134">Количество интервалов повторяющегося календарного плана</span><span class="sxs-lookup"><span data-stu-id="da1a0-134">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a0-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="da1a0-135">-IntervalType</span></span>
<span data-ttu-id="da1a0-136">Тип интервала повторяющегося расписания: "Минуты", "Часы", "День", "Неделя", "Месяц"</span><span class="sxs-lookup"><span data-stu-id="da1a0-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a0-137">-Name</span><span class="sxs-lookup"><span data-stu-id="da1a0-137">-Name</span></span>
<span data-ttu-id="da1a0-138">Имя задания</span><span class="sxs-lookup"><span data-stu-id="da1a0-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da1a0-139">-ResourceGroupName</span></span>
<span data-ttu-id="da1a0-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="da1a0-140">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a0-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da1a0-141">-ResourceId</span></span>
<span data-ttu-id="da1a0-142">ИД ресурса задания</span><span class="sxs-lookup"><span data-stu-id="da1a0-142">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1a0-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="da1a0-143">-RunOnce</span></span>
<span data-ttu-id="da1a0-144">Флаг, который указывает на то, что задание будет выполниться один раз</span><span class="sxs-lookup"><span data-stu-id="da1a0-144">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a0-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da1a0-145">-ServerName</span></span>
<span data-ttu-id="da1a0-146">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="da1a0-146">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a0-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="da1a0-147">-StartTime</span></span>
<span data-ttu-id="da1a0-148">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="da1a0-148">The job schedule start time</span></span>

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

### <span data-ttu-id="da1a0-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da1a0-149">-Confirm</span></span>
<span data-ttu-id="da1a0-150">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="da1a0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da1a0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da1a0-151">-WhatIf</span></span>
<span data-ttu-id="da1a0-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da1a0-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da1a0-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="da1a0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da1a0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1a0-154">CommonParameters</span></span>
<span data-ttu-id="da1a0-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da1a0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1a0-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da1a0-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1a0-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da1a0-157">INPUTS</span></span>

### <span data-ttu-id="da1a0-158">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="da1a0-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="da1a0-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da1a0-159">OUTPUTS</span></span>

### <span data-ttu-id="da1a0-160">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="da1a0-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="da1a0-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da1a0-161">NOTES</span></span>

## <span data-ttu-id="da1a0-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da1a0-162">RELATED LINKS</span></span>
