---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 961f37db94cff87952b2811a528a94cc71ffabff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010163"
---
# <span data-ttu-id="c73a6-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="c73a6-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="c73a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c73a6-102">SYNOPSIS</span></span>
<span data-ttu-id="c73a6-103">Создание задания</span><span class="sxs-lookup"><span data-stu-id="c73a6-103">Creates a new job</span></span>

## <span data-ttu-id="c73a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c73a6-104">SYNTAX</span></span>

### <span data-ttu-id="c73a6-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c73a6-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c73a6-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="c73a6-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c73a6-107">Повторяющийся</span><span class="sxs-lookup"><span data-stu-id="c73a6-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c73a6-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c73a6-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c73a6-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c73a6-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c73a6-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c73a6-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c73a6-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c73a6-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c73a6-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c73a6-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c73a6-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c73a6-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c73a6-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c73a6-114">DESCRIPTION</span></span>
<span data-ttu-id="c73a6-115">С New-AzSqlElasticJob-за другго условия создается задание</span><span class="sxs-lookup"><span data-stu-id="c73a6-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="c73a6-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c73a6-116">EXAMPLES</span></span>

### <span data-ttu-id="c73a6-117">Пример 1. Создание задания</span><span class="sxs-lookup"><span data-stu-id="c73a6-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="c73a6-118">Создание задания</span><span class="sxs-lookup"><span data-stu-id="c73a6-118">Creates a new job</span></span>

### <span data-ttu-id="c73a6-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c73a6-119">Example 2</span></span>

<span data-ttu-id="c73a6-120">Создает задание.</span><span class="sxs-lookup"><span data-stu-id="c73a6-120">Creates a new job.</span></span> <span data-ttu-id="c73a6-121">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c73a6-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="c73a6-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c73a6-122">PARAMETERS</span></span>

### <span data-ttu-id="c73a6-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c73a6-123">-AgentName</span></span>
<span data-ttu-id="c73a6-124">Имя агента</span><span class="sxs-lookup"><span data-stu-id="c73a6-124">The agent name</span></span>

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

### <span data-ttu-id="c73a6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73a6-125">-DefaultProfile</span></span>
<span data-ttu-id="c73a6-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c73a6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c73a6-127">-Description</span><span class="sxs-lookup"><span data-stu-id="c73a6-127">-Description</span></span>
<span data-ttu-id="c73a6-128">Описание должности</span><span class="sxs-lookup"><span data-stu-id="c73a6-128">The job description</span></span>

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

### <span data-ttu-id="c73a6-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="c73a6-129">-Enable</span></span>
<span data-ttu-id="c73a6-130">Флажок, который указывает, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="c73a6-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="c73a6-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c73a6-131">-EndTime</span></span>
<span data-ttu-id="c73a6-132">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="c73a6-132">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73a6-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="c73a6-133">-IntervalCount</span></span>
<span data-ttu-id="c73a6-134">Количество интервалов повторяющегося расписания</span><span class="sxs-lookup"><span data-stu-id="c73a6-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="c73a6-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="c73a6-135">-IntervalType</span></span>
<span data-ttu-id="c73a6-136">Тип интервала повторяющегося расписания: "Минуты", "Часы", "День", "Неделя", "Месяц"</span><span class="sxs-lookup"><span data-stu-id="c73a6-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="c73a6-137">-Name</span><span class="sxs-lookup"><span data-stu-id="c73a6-137">-Name</span></span>
<span data-ttu-id="c73a6-138">Имя задания</span><span class="sxs-lookup"><span data-stu-id="c73a6-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73a6-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c73a6-139">-ParentObject</span></span>
<span data-ttu-id="c73a6-140">Объект ввода агента</span><span class="sxs-lookup"><span data-stu-id="c73a6-140">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c73a6-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c73a6-141">-ParentResourceId</span></span>
<span data-ttu-id="c73a6-142">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="c73a6-142">The agent resource id</span></span>

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

### <span data-ttu-id="c73a6-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c73a6-143">-ResourceGroupName</span></span>
<span data-ttu-id="c73a6-144">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c73a6-144">The resource group name</span></span>

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

### <span data-ttu-id="c73a6-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="c73a6-145">-RunOnce</span></span>
<span data-ttu-id="c73a6-146">Флаг, который указывает на то, что задание будет выполниться один раз</span><span class="sxs-lookup"><span data-stu-id="c73a6-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="c73a6-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c73a6-147">-ServerName</span></span>
<span data-ttu-id="c73a6-148">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="c73a6-148">The server name</span></span>

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

### <span data-ttu-id="c73a6-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c73a6-149">-StartTime</span></span>
<span data-ttu-id="c73a6-150">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="c73a6-150">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73a6-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c73a6-151">-Confirm</span></span>
<span data-ttu-id="c73a6-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c73a6-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c73a6-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c73a6-153">-WhatIf</span></span>
<span data-ttu-id="c73a6-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c73a6-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c73a6-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c73a6-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c73a6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73a6-156">CommonParameters</span></span>
<span data-ttu-id="c73a6-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c73a6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73a6-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c73a6-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73a6-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c73a6-159">INPUTS</span></span>

### <span data-ttu-id="c73a6-160">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="c73a6-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="c73a6-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c73a6-161">OUTPUTS</span></span>

### <span data-ttu-id="c73a6-162">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="c73a6-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="c73a6-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c73a6-163">NOTES</span></span>

## <span data-ttu-id="c73a6-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c73a6-164">RELATED LINKS</span></span>
