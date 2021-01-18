---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505917"
---
# <span data-ttu-id="0faab-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="0faab-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="0faab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0faab-102">SYNOPSIS</span></span>
<span data-ttu-id="0faab-103">Создание задания</span><span class="sxs-lookup"><span data-stu-id="0faab-103">Creates a new job</span></span>

## <span data-ttu-id="0faab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0faab-104">SYNTAX</span></span>

### <span data-ttu-id="0faab-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0faab-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0faab-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="0faab-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0faab-107">Повторяющийся</span><span class="sxs-lookup"><span data-stu-id="0faab-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0faab-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0faab-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0faab-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0faab-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0faab-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0faab-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0faab-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0faab-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0faab-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0faab-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0faab-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0faab-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0faab-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0faab-114">DESCRIPTION</span></span>
<span data-ttu-id="0faab-115">С New-AzSqlElasticJob-код создается новое задание.</span><span class="sxs-lookup"><span data-stu-id="0faab-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="0faab-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0faab-116">EXAMPLES</span></span>

### <span data-ttu-id="0faab-117">Пример 1. Создание задания</span><span class="sxs-lookup"><span data-stu-id="0faab-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="0faab-118">Создание задания</span><span class="sxs-lookup"><span data-stu-id="0faab-118">Creates a new job</span></span>

### <span data-ttu-id="0faab-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0faab-119">Example 2</span></span>

<span data-ttu-id="0faab-120">Создает задание.</span><span class="sxs-lookup"><span data-stu-id="0faab-120">Creates a new job.</span></span> <span data-ttu-id="0faab-121">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="0faab-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="0faab-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0faab-122">PARAMETERS</span></span>

### <span data-ttu-id="0faab-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0faab-123">-AgentName</span></span>
<span data-ttu-id="0faab-124">Имя агента</span><span class="sxs-lookup"><span data-stu-id="0faab-124">The agent name</span></span>

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

### <span data-ttu-id="0faab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0faab-125">-DefaultProfile</span></span>
<span data-ttu-id="0faab-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0faab-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0faab-127">-Description</span><span class="sxs-lookup"><span data-stu-id="0faab-127">-Description</span></span>
<span data-ttu-id="0faab-128">Описание должности</span><span class="sxs-lookup"><span data-stu-id="0faab-128">The job description</span></span>

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

### <span data-ttu-id="0faab-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="0faab-129">-Enable</span></span>
<span data-ttu-id="0faab-130">Флажок, который указывает, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="0faab-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="0faab-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0faab-131">-EndTime</span></span>
<span data-ttu-id="0faab-132">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="0faab-132">The job schedule end time</span></span>

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

### <span data-ttu-id="0faab-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="0faab-133">-IntervalCount</span></span>
<span data-ttu-id="0faab-134">Количество интервалов повторяющегося расписания</span><span class="sxs-lookup"><span data-stu-id="0faab-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="0faab-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="0faab-135">-IntervalType</span></span>
<span data-ttu-id="0faab-136">Тип интервала повторяющегося расписания: "Минуты", "Часы", "День", "Неделя", "Месяц"</span><span class="sxs-lookup"><span data-stu-id="0faab-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="0faab-137">-Name</span><span class="sxs-lookup"><span data-stu-id="0faab-137">-Name</span></span>
<span data-ttu-id="0faab-138">Имя задания</span><span class="sxs-lookup"><span data-stu-id="0faab-138">The job name</span></span>

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

### <span data-ttu-id="0faab-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0faab-139">-ParentObject</span></span>
<span data-ttu-id="0faab-140">Объект ввода агента</span><span class="sxs-lookup"><span data-stu-id="0faab-140">The agent input object</span></span>

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

### <span data-ttu-id="0faab-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0faab-141">-ParentResourceId</span></span>
<span data-ttu-id="0faab-142">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="0faab-142">The agent resource id</span></span>

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

### <span data-ttu-id="0faab-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0faab-143">-ResourceGroupName</span></span>
<span data-ttu-id="0faab-144">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0faab-144">The resource group name</span></span>

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

### <span data-ttu-id="0faab-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="0faab-145">-RunOnce</span></span>
<span data-ttu-id="0faab-146">Флажок, который указывает на то, что задание будет выполниться один раз</span><span class="sxs-lookup"><span data-stu-id="0faab-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="0faab-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0faab-147">-ServerName</span></span>
<span data-ttu-id="0faab-148">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="0faab-148">The server name</span></span>

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

### <span data-ttu-id="0faab-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0faab-149">-StartTime</span></span>
<span data-ttu-id="0faab-150">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="0faab-150">The job schedule start time</span></span>

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

### <span data-ttu-id="0faab-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0faab-151">-Confirm</span></span>
<span data-ttu-id="0faab-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0faab-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0faab-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0faab-153">-WhatIf</span></span>
<span data-ttu-id="0faab-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0faab-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0faab-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0faab-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0faab-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0faab-156">CommonParameters</span></span>
<span data-ttu-id="0faab-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0faab-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0faab-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0faab-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0faab-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0faab-159">INPUTS</span></span>

### <span data-ttu-id="0faab-160">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="0faab-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="0faab-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0faab-161">OUTPUTS</span></span>

### <span data-ttu-id="0faab-162">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="0faab-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0faab-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0faab-163">NOTES</span></span>

## <span data-ttu-id="0faab-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0faab-164">RELATED LINKS</span></span>
