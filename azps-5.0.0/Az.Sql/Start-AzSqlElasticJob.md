---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315590"
---
# <span data-ttu-id="41c92-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="41c92-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="41c92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41c92-102">SYNOPSIS</span></span>
<span data-ttu-id="41c92-103">Запускает задание, возвращая идентификатор выполнения задания, который можно опросить, чтобы просмотреть его состояние</span><span class="sxs-lookup"><span data-stu-id="41c92-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="41c92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41c92-104">SYNTAX</span></span>

### <span data-ttu-id="41c92-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41c92-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41c92-106">Объект</span><span class="sxs-lookup"><span data-stu-id="41c92-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c92-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="41c92-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41c92-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41c92-108">DESCRIPTION</span></span>
<span data-ttu-id="41c92-109">Командлет Start-AzSqlElasticJob запускает задание, возвращающее новое выполнение задания.</span><span class="sxs-lookup"><span data-stu-id="41c92-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="41c92-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41c92-110">EXAMPLES</span></span>

### <span data-ttu-id="41c92-111">Пример 1: запуск задания, возвращающего новое выполнение задания</span><span class="sxs-lookup"><span data-stu-id="41c92-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="41c92-112">Запускает задание, возвращающее новое выполнение задания</span><span class="sxs-lookup"><span data-stu-id="41c92-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="41c92-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41c92-113">PARAMETERS</span></span>

### <span data-ttu-id="41c92-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="41c92-114">-AgentName</span></span>
<span data-ttu-id="41c92-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="41c92-115">The agent name</span></span>

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

### <span data-ttu-id="41c92-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41c92-116">-AsJob</span></span>
<span data-ttu-id="41c92-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="41c92-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41c92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c92-118">-DefaultProfile</span></span>
<span data-ttu-id="41c92-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41c92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c92-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="41c92-120">-JobName</span></span>
<span data-ttu-id="41c92-121">Имя задания</span><span class="sxs-lookup"><span data-stu-id="41c92-121">The job name</span></span>

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

### <span data-ttu-id="41c92-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="41c92-122">-ParentObject</span></span>
<span data-ttu-id="41c92-123">Объект "задание"</span><span class="sxs-lookup"><span data-stu-id="41c92-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41c92-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="41c92-124">-ParentResourceId</span></span>
<span data-ttu-id="41c92-125">Идентификатор ресурса задания</span><span class="sxs-lookup"><span data-stu-id="41c92-125">The job resource id</span></span>

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

### <span data-ttu-id="41c92-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c92-126">-ResourceGroupName</span></span>
<span data-ttu-id="41c92-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="41c92-127">The resource group name</span></span>

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

### <span data-ttu-id="41c92-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="41c92-128">-ServerName</span></span>
<span data-ttu-id="41c92-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="41c92-129">The server name</span></span>

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

### <span data-ttu-id="41c92-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="41c92-130">-Wait</span></span>
<span data-ttu-id="41c92-131">Флаг ожидания, указывающий, что нужно подождать, пока выполнение задания не будет завершено</span><span class="sxs-lookup"><span data-stu-id="41c92-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="41c92-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41c92-132">-Confirm</span></span>
<span data-ttu-id="41c92-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41c92-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c92-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c92-134">-WhatIf</span></span>
<span data-ttu-id="41c92-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41c92-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c92-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41c92-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c92-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c92-137">CommonParameters</span></span>
<span data-ttu-id="41c92-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41c92-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c92-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41c92-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c92-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41c92-140">INPUTS</span></span>

### <span data-ttu-id="41c92-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="41c92-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="41c92-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41c92-142">OUTPUTS</span></span>

### <span data-ttu-id="41c92-143">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="41c92-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="41c92-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="41c92-144">NOTES</span></span>

## <span data-ttu-id="41c92-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41c92-145">RELATED LINKS</span></span>
