---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217361"
---
# <span data-ttu-id="8e273-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="8e273-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="8e273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e273-102">SYNOPSIS</span></span>
<span data-ttu-id="8e273-103">Создание задания</span><span class="sxs-lookup"><span data-stu-id="8e273-103">Creates a new job</span></span>

## <span data-ttu-id="8e273-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e273-104">SYNTAX</span></span>

### <span data-ttu-id="8e273-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e273-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e273-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="8e273-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e273-107">Повторяющийся</span><span class="sxs-lookup"><span data-stu-id="8e273-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e273-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8e273-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e273-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8e273-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e273-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8e273-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e273-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8e273-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e273-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8e273-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e273-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8e273-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e273-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e273-114">DESCRIPTION</span></span>
<span data-ttu-id="8e273-115">С New-AzSqlElasticJob-за другго условия создается задание</span><span class="sxs-lookup"><span data-stu-id="8e273-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="8e273-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e273-116">EXAMPLES</span></span>

### <span data-ttu-id="8e273-117">Пример 1. Создание задания</span><span class="sxs-lookup"><span data-stu-id="8e273-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="8e273-118">Создание задания</span><span class="sxs-lookup"><span data-stu-id="8e273-118">Creates a new job</span></span>

### <span data-ttu-id="8e273-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8e273-119">Example 2</span></span>

<span data-ttu-id="8e273-120">Создает задание.</span><span class="sxs-lookup"><span data-stu-id="8e273-120">Creates a new job.</span></span> <span data-ttu-id="8e273-121">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="8e273-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="8e273-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e273-122">PARAMETERS</span></span>

### <span data-ttu-id="8e273-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8e273-123">-AgentName</span></span>
<span data-ttu-id="8e273-124">Имя агента</span><span class="sxs-lookup"><span data-stu-id="8e273-124">The agent name</span></span>

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

### <span data-ttu-id="8e273-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e273-125">-DefaultProfile</span></span>
<span data-ttu-id="8e273-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e273-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e273-127">-Description</span><span class="sxs-lookup"><span data-stu-id="8e273-127">-Description</span></span>
<span data-ttu-id="8e273-128">Описание должности</span><span class="sxs-lookup"><span data-stu-id="8e273-128">The job description</span></span>

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

### <span data-ttu-id="8e273-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="8e273-129">-Enable</span></span>
<span data-ttu-id="8e273-130">Флажок, который указывает, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="8e273-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="8e273-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8e273-131">-EndTime</span></span>
<span data-ttu-id="8e273-132">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="8e273-132">The job schedule end time</span></span>

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

### <span data-ttu-id="8e273-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="8e273-133">-IntervalCount</span></span>
<span data-ttu-id="8e273-134">Количество интервалов повторяющегося календарного плана</span><span class="sxs-lookup"><span data-stu-id="8e273-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="8e273-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="8e273-135">-IntervalType</span></span>
<span data-ttu-id="8e273-136">Тип интервала повторяющегося расписания: "Минуты", "Часы", "День", "Неделя", "Месяц"</span><span class="sxs-lookup"><span data-stu-id="8e273-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="8e273-137">-Name</span><span class="sxs-lookup"><span data-stu-id="8e273-137">-Name</span></span>
<span data-ttu-id="8e273-138">Имя задания</span><span class="sxs-lookup"><span data-stu-id="8e273-138">The job name</span></span>

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

### <span data-ttu-id="8e273-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e273-139">-ParentObject</span></span>
<span data-ttu-id="8e273-140">Объект ввода агента</span><span class="sxs-lookup"><span data-stu-id="8e273-140">The agent input object</span></span>

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

### <span data-ttu-id="8e273-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8e273-141">-ParentResourceId</span></span>
<span data-ttu-id="8e273-142">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="8e273-142">The agent resource id</span></span>

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

### <span data-ttu-id="8e273-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e273-143">-ResourceGroupName</span></span>
<span data-ttu-id="8e273-144">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8e273-144">The resource group name</span></span>

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

### <span data-ttu-id="8e273-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="8e273-145">-RunOnce</span></span>
<span data-ttu-id="8e273-146">Флажок, который указывает на то, что задание будет выполниться один раз</span><span class="sxs-lookup"><span data-stu-id="8e273-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="8e273-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e273-147">-ServerName</span></span>
<span data-ttu-id="8e273-148">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="8e273-148">The server name</span></span>

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

### <span data-ttu-id="8e273-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8e273-149">-StartTime</span></span>
<span data-ttu-id="8e273-150">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="8e273-150">The job schedule start time</span></span>

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

### <span data-ttu-id="8e273-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e273-151">-Confirm</span></span>
<span data-ttu-id="8e273-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e273-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e273-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e273-153">-WhatIf</span></span>
<span data-ttu-id="8e273-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e273-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e273-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8e273-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e273-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e273-156">CommonParameters</span></span>
<span data-ttu-id="8e273-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e273-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e273-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e273-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e273-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e273-159">INPUTS</span></span>

### <span data-ttu-id="8e273-160">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="8e273-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="8e273-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e273-161">OUTPUTS</span></span>

### <span data-ttu-id="8e273-162">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="8e273-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="8e273-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e273-163">NOTES</span></span>

## <span data-ttu-id="8e273-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e273-164">RELATED LINKS</span></span>
