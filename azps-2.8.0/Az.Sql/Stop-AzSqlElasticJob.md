---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 0b7fc702ad331a2ad51e1adfaf4aefd6ae440259
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906778"
---
# <span data-ttu-id="4fccc-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="4fccc-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="4fccc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fccc-102">SYNOPSIS</span></span>
<span data-ttu-id="4fccc-103">Остановка задания с учетом его идентификатора выполнения задания</span><span class="sxs-lookup"><span data-stu-id="4fccc-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="4fccc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fccc-104">SYNTAX</span></span>

### <span data-ttu-id="4fccc-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4fccc-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fccc-106">Объект</span><span class="sxs-lookup"><span data-stu-id="4fccc-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fccc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4fccc-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fccc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fccc-108">DESCRIPTION</span></span>
<span data-ttu-id="4fccc-109">Командлет Stop-AzSqlElasticJob останавливает выполнение задания с выполнением.</span><span class="sxs-lookup"><span data-stu-id="4fccc-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="4fccc-110">Возвращает текущее состояние выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="4fccc-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="4fccc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fccc-111">EXAMPLES</span></span>

### <span data-ttu-id="4fccc-112">Пример 1: Остановка задания с выполнением выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="4fccc-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="4fccc-113">Останавливает выполняющееся выполнение задания и возвращает его текущее состояние</span><span class="sxs-lookup"><span data-stu-id="4fccc-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="4fccc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fccc-114">PARAMETERS</span></span>

### <span data-ttu-id="4fccc-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4fccc-115">-AgentName</span></span>
<span data-ttu-id="4fccc-116">Имя агента</span><span class="sxs-lookup"><span data-stu-id="4fccc-116">The agent name</span></span>

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

### <span data-ttu-id="4fccc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fccc-117">-DefaultProfile</span></span>
<span data-ttu-id="4fccc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fccc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fccc-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="4fccc-119">-JobExecutionId</span></span>
<span data-ttu-id="4fccc-120">Идентификатор выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="4fccc-120">The job execution id.</span></span>

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

### <span data-ttu-id="4fccc-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="4fccc-121">-JobName</span></span>
<span data-ttu-id="4fccc-122">Имя задания</span><span class="sxs-lookup"><span data-stu-id="4fccc-122">The job name</span></span>

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

### <span data-ttu-id="4fccc-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4fccc-123">-ParentObject</span></span>
<span data-ttu-id="4fccc-124">Объект базы данных элемента управления агента</span><span class="sxs-lookup"><span data-stu-id="4fccc-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="4fccc-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4fccc-125">-ParentResourceId</span></span>
<span data-ttu-id="4fccc-126">Идентификатор ресурса выполнения задания</span><span class="sxs-lookup"><span data-stu-id="4fccc-126">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fccc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fccc-127">-ResourceGroupName</span></span>
<span data-ttu-id="4fccc-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4fccc-128">The resource group name</span></span>

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

### <span data-ttu-id="4fccc-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4fccc-129">-ServerName</span></span>
<span data-ttu-id="4fccc-130">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="4fccc-130">The server name</span></span>

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

### <span data-ttu-id="4fccc-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fccc-131">-Confirm</span></span>
<span data-ttu-id="4fccc-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4fccc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fccc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fccc-133">-WhatIf</span></span>
<span data-ttu-id="4fccc-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4fccc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fccc-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4fccc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fccc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fccc-136">CommonParameters</span></span>
<span data-ttu-id="4fccc-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fccc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fccc-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fccc-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fccc-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fccc-139">INPUTS</span></span>

### <span data-ttu-id="4fccc-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="4fccc-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4fccc-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fccc-141">OUTPUTS</span></span>

### <span data-ttu-id="4fccc-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="4fccc-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4fccc-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fccc-143">NOTES</span></span>

## <span data-ttu-id="4fccc-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fccc-144">RELATED LINKS</span></span>

## <span data-ttu-id="4fccc-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fccc-145">RELATED LINKS</span></span>
