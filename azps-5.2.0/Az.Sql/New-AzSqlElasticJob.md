---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325195"
---
# <span data-ttu-id="2352c-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="2352c-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="2352c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2352c-102">SYNOPSIS</span></span>
<span data-ttu-id="2352c-103">Создание задания</span><span class="sxs-lookup"><span data-stu-id="2352c-103">Creates a new job</span></span>

## <span data-ttu-id="2352c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2352c-104">SYNTAX</span></span>

### <span data-ttu-id="2352c-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2352c-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2352c-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="2352c-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2352c-107">Повторяющийся</span><span class="sxs-lookup"><span data-stu-id="2352c-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2352c-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2352c-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2352c-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2352c-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2352c-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2352c-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2352c-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2352c-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2352c-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2352c-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2352c-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2352c-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2352c-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2352c-114">DESCRIPTION</span></span>
<span data-ttu-id="2352c-115">С New-AzSqlElasticJob-за другго условия создается задание</span><span class="sxs-lookup"><span data-stu-id="2352c-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="2352c-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2352c-116">EXAMPLES</span></span>

### <span data-ttu-id="2352c-117">Пример 1. Создание задания</span><span class="sxs-lookup"><span data-stu-id="2352c-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="2352c-118">Создание задания</span><span class="sxs-lookup"><span data-stu-id="2352c-118">Creates a new job</span></span>

### <span data-ttu-id="2352c-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2352c-119">Example 2</span></span>

<span data-ttu-id="2352c-120">Создает задание.</span><span class="sxs-lookup"><span data-stu-id="2352c-120">Creates a new job.</span></span> <span data-ttu-id="2352c-121">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2352c-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="2352c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2352c-122">PARAMETERS</span></span>

### <span data-ttu-id="2352c-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2352c-123">-AgentName</span></span>
<span data-ttu-id="2352c-124">Имя агента</span><span class="sxs-lookup"><span data-stu-id="2352c-124">The agent name</span></span>

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

### <span data-ttu-id="2352c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2352c-125">-DefaultProfile</span></span>
<span data-ttu-id="2352c-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2352c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2352c-127">-Description</span><span class="sxs-lookup"><span data-stu-id="2352c-127">-Description</span></span>
<span data-ttu-id="2352c-128">Описание должности</span><span class="sxs-lookup"><span data-stu-id="2352c-128">The job description</span></span>

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

### <span data-ttu-id="2352c-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="2352c-129">-Enable</span></span>
<span data-ttu-id="2352c-130">Флажок, который указывает, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="2352c-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="2352c-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2352c-131">-EndTime</span></span>
<span data-ttu-id="2352c-132">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="2352c-132">The job schedule end time</span></span>

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

### <span data-ttu-id="2352c-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="2352c-133">-IntervalCount</span></span>
<span data-ttu-id="2352c-134">Количество интервалов повторяющегося календарного плана</span><span class="sxs-lookup"><span data-stu-id="2352c-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="2352c-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="2352c-135">-IntervalType</span></span>
<span data-ttu-id="2352c-136">Тип интервала повторяющегося расписания: "Минуты", "Часы", "День", "Неделя", "Месяц"</span><span class="sxs-lookup"><span data-stu-id="2352c-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="2352c-137">-Name</span><span class="sxs-lookup"><span data-stu-id="2352c-137">-Name</span></span>
<span data-ttu-id="2352c-138">Имя задания</span><span class="sxs-lookup"><span data-stu-id="2352c-138">The job name</span></span>

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

### <span data-ttu-id="2352c-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2352c-139">-ParentObject</span></span>
<span data-ttu-id="2352c-140">Объект ввода агента</span><span class="sxs-lookup"><span data-stu-id="2352c-140">The agent input object</span></span>

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

### <span data-ttu-id="2352c-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2352c-141">-ParentResourceId</span></span>
<span data-ttu-id="2352c-142">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="2352c-142">The agent resource id</span></span>

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

### <span data-ttu-id="2352c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2352c-143">-ResourceGroupName</span></span>
<span data-ttu-id="2352c-144">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2352c-144">The resource group name</span></span>

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

### <span data-ttu-id="2352c-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="2352c-145">-RunOnce</span></span>
<span data-ttu-id="2352c-146">Флаг, который указывает на то, что задание будет выполниться один раз</span><span class="sxs-lookup"><span data-stu-id="2352c-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="2352c-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2352c-147">-ServerName</span></span>
<span data-ttu-id="2352c-148">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="2352c-148">The server name</span></span>

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

### <span data-ttu-id="2352c-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2352c-149">-StartTime</span></span>
<span data-ttu-id="2352c-150">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="2352c-150">The job schedule start time</span></span>

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

### <span data-ttu-id="2352c-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2352c-151">-Confirm</span></span>
<span data-ttu-id="2352c-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2352c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2352c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2352c-153">-WhatIf</span></span>
<span data-ttu-id="2352c-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2352c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2352c-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2352c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2352c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2352c-156">CommonParameters</span></span>
<span data-ttu-id="2352c-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2352c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2352c-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2352c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2352c-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2352c-159">INPUTS</span></span>

### <span data-ttu-id="2352c-160">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2352c-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2352c-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2352c-161">OUTPUTS</span></span>

### <span data-ttu-id="2352c-162">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="2352c-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="2352c-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2352c-163">NOTES</span></span>

## <span data-ttu-id="2352c-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2352c-164">RELATED LINKS</span></span>
