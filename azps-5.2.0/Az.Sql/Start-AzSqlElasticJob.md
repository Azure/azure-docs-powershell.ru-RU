---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399783"
---
# <span data-ttu-id="44e1a-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="44e1a-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="44e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="44e1a-103">Запускает задание, возвращая ид выполнения задания, который можно опросить для просмотра его состояния.</span><span class="sxs-lookup"><span data-stu-id="44e1a-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="44e1a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="44e1a-104">SYNTAX</span></span>

### <span data-ttu-id="44e1a-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44e1a-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44e1a-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="44e1a-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44e1a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="44e1a-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44e1a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44e1a-108">DESCRIPTION</span></span>
<span data-ttu-id="44e1a-109">С Start-AzSqlElasticJob запускается задание, возвращающие новое выполнение задания</span><span class="sxs-lookup"><span data-stu-id="44e1a-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="44e1a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="44e1a-110">EXAMPLES</span></span>

### <span data-ttu-id="44e1a-111">Пример 1. Начало задания, возвращаемого для выполнения нового задания</span><span class="sxs-lookup"><span data-stu-id="44e1a-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="44e1a-112">Начало задания, возвращающих новое выполнение задания</span><span class="sxs-lookup"><span data-stu-id="44e1a-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="44e1a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44e1a-113">PARAMETERS</span></span>

### <span data-ttu-id="44e1a-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="44e1a-114">-AgentName</span></span>
<span data-ttu-id="44e1a-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="44e1a-115">The agent name</span></span>

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

### <span data-ttu-id="44e1a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44e1a-116">-AsJob</span></span>
<span data-ttu-id="44e1a-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="44e1a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44e1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e1a-118">-DefaultProfile</span></span>
<span data-ttu-id="44e1a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44e1a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44e1a-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="44e1a-120">-JobName</span></span>
<span data-ttu-id="44e1a-121">Имя задания</span><span class="sxs-lookup"><span data-stu-id="44e1a-121">The job name</span></span>

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

### <span data-ttu-id="44e1a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="44e1a-122">-ParentObject</span></span>
<span data-ttu-id="44e1a-123">Объект задания</span><span class="sxs-lookup"><span data-stu-id="44e1a-123">The job object</span></span>

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

### <span data-ttu-id="44e1a-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="44e1a-124">-ParentResourceId</span></span>
<span data-ttu-id="44e1a-125">ИД ресурса задания</span><span class="sxs-lookup"><span data-stu-id="44e1a-125">The job resource id</span></span>

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

### <span data-ttu-id="44e1a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44e1a-126">-ResourceGroupName</span></span>
<span data-ttu-id="44e1a-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="44e1a-127">The resource group name</span></span>

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

### <span data-ttu-id="44e1a-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="44e1a-128">-ServerName</span></span>
<span data-ttu-id="44e1a-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="44e1a-129">The server name</span></span>

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

### <span data-ttu-id="44e1a-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="44e1a-130">-Wait</span></span>
<span data-ttu-id="44e1a-131">Флажок "Ожидание", который указывает на то, что нужно подождать, пока выполнение задания будет сделано</span><span class="sxs-lookup"><span data-stu-id="44e1a-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="44e1a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44e1a-132">-Confirm</span></span>
<span data-ttu-id="44e1a-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="44e1a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44e1a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44e1a-134">-WhatIf</span></span>
<span data-ttu-id="44e1a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44e1a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44e1a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="44e1a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44e1a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e1a-137">CommonParameters</span></span>
<span data-ttu-id="44e1a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44e1a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e1a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44e1a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e1a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44e1a-140">INPUTS</span></span>

### <span data-ttu-id="44e1a-141">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="44e1a-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="44e1a-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="44e1a-142">OUTPUTS</span></span>

### <span data-ttu-id="44e1a-143">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="44e1a-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="44e1a-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="44e1a-144">NOTES</span></span>

## <span data-ttu-id="44e1a-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44e1a-145">RELATED LINKS</span></span>
