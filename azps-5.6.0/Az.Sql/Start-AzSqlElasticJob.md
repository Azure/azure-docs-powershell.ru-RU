---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 6163c7be725d66c7e1f64fced3be0269ffedd32f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011475"
---
# <span data-ttu-id="9d9ed-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="9d9ed-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="9d9ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d9ed-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9ed-103">Запускает задание, возвращая ид выполнения задания, который можно опросить для просмотра его состояния.</span><span class="sxs-lookup"><span data-stu-id="9d9ed-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="9d9ed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d9ed-104">SYNTAX</span></span>

### <span data-ttu-id="9d9ed-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d9ed-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d9ed-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9d9ed-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9ed-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9d9ed-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d9ed-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d9ed-108">DESCRIPTION</span></span>
<span data-ttu-id="9d9ed-109">С Start-AzSqlElasticJob запускается задание, возвращающие новое выполнение задания</span><span class="sxs-lookup"><span data-stu-id="9d9ed-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="9d9ed-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d9ed-110">EXAMPLES</span></span>

### <span data-ttu-id="9d9ed-111">Пример 1. Начало задания, возвращаемого для выполнения нового задания</span><span class="sxs-lookup"><span data-stu-id="9d9ed-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="9d9ed-112">Начало задания, возвращающих новое выполнение задания</span><span class="sxs-lookup"><span data-stu-id="9d9ed-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="9d9ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d9ed-113">PARAMETERS</span></span>

### <span data-ttu-id="9d9ed-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9d9ed-114">-AgentName</span></span>
<span data-ttu-id="9d9ed-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="9d9ed-115">The agent name</span></span>

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

### <span data-ttu-id="9d9ed-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d9ed-116">-AsJob</span></span>
<span data-ttu-id="9d9ed-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9d9ed-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d9ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9ed-118">-DefaultProfile</span></span>
<span data-ttu-id="9d9ed-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d9ed-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="9d9ed-120">-JobName</span></span>
<span data-ttu-id="9d9ed-121">Имя задания</span><span class="sxs-lookup"><span data-stu-id="9d9ed-121">The job name</span></span>

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

### <span data-ttu-id="9d9ed-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9d9ed-122">-ParentObject</span></span>
<span data-ttu-id="9d9ed-123">Объект задания</span><span class="sxs-lookup"><span data-stu-id="9d9ed-123">The job object</span></span>

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

### <span data-ttu-id="9d9ed-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9d9ed-124">-ParentResourceId</span></span>
<span data-ttu-id="9d9ed-125">ИД ресурса задания</span><span class="sxs-lookup"><span data-stu-id="9d9ed-125">The job resource id</span></span>

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

### <span data-ttu-id="9d9ed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d9ed-126">-ResourceGroupName</span></span>
<span data-ttu-id="9d9ed-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9d9ed-127">The resource group name</span></span>

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

### <span data-ttu-id="9d9ed-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9d9ed-128">-ServerName</span></span>
<span data-ttu-id="9d9ed-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="9d9ed-129">The server name</span></span>

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

### <span data-ttu-id="9d9ed-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="9d9ed-130">-Wait</span></span>
<span data-ttu-id="9d9ed-131">Флажок ожидания, который указывает на то, что нужно подождать, пока выполнение задания будет сделано</span><span class="sxs-lookup"><span data-stu-id="9d9ed-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="9d9ed-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d9ed-132">-Confirm</span></span>
<span data-ttu-id="9d9ed-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d9ed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d9ed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d9ed-134">-WhatIf</span></span>
<span data-ttu-id="9d9ed-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d9ed-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d9ed-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d9ed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d9ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9ed-137">CommonParameters</span></span>
<span data-ttu-id="9d9ed-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9ed-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d9ed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9ed-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d9ed-140">INPUTS</span></span>

### <span data-ttu-id="9d9ed-141">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="9d9ed-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="9d9ed-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d9ed-142">OUTPUTS</span></span>

### <span data-ttu-id="9d9ed-143">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="9d9ed-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="9d9ed-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d9ed-144">NOTES</span></span>

## <span data-ttu-id="9d9ed-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d9ed-145">RELATED LINKS</span></span>
