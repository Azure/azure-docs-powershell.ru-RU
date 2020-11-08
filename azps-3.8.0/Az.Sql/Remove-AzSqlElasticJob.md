---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: 03f2e9af6b7225fd7622c03347bdea87c63453c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073191"
---
# <span data-ttu-id="1cc4c-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="1cc4c-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="1cc4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1cc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc4c-103">Удаление задания</span><span class="sxs-lookup"><span data-stu-id="1cc4c-103">Removes a job</span></span>

## <span data-ttu-id="1cc4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1cc4c-104">SYNTAX</span></span>

### <span data-ttu-id="1cc4c-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1cc4c-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc4c-106">Объект</span><span class="sxs-lookup"><span data-stu-id="1cc4c-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc4c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1cc4c-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc4c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cc4c-108">DESCRIPTION</span></span>
<span data-ttu-id="1cc4c-109">Командлет Remove-AzSqlElasticJob удаляет задание.</span><span class="sxs-lookup"><span data-stu-id="1cc4c-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="1cc4c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1cc4c-110">EXAMPLES</span></span>

### <span data-ttu-id="1cc4c-111">Пример 1: удаление задания</span><span class="sxs-lookup"><span data-stu-id="1cc4c-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="1cc4c-112">Удаление задания</span><span class="sxs-lookup"><span data-stu-id="1cc4c-112">Removes a job</span></span>

## <span data-ttu-id="1cc4c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1cc4c-113">PARAMETERS</span></span>

### <span data-ttu-id="1cc4c-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1cc4c-114">-AgentName</span></span>
<span data-ttu-id="1cc4c-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="1cc4c-115">The agent name</span></span>

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

### <span data-ttu-id="1cc4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc4c-116">-DefaultProfile</span></span>
<span data-ttu-id="1cc4c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc4c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1cc4c-118">-Force</span></span>
<span data-ttu-id="1cc4c-119">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="1cc4c-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1cc4c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cc4c-120">-InputObject</span></span>
<span data-ttu-id="1cc4c-121">Входной объект задания</span><span class="sxs-lookup"><span data-stu-id="1cc4c-121">The job input object</span></span>

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

### <span data-ttu-id="1cc4c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1cc4c-122">-Name</span></span>
<span data-ttu-id="1cc4c-123">Имя задания</span><span class="sxs-lookup"><span data-stu-id="1cc4c-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc4c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc4c-124">-ResourceGroupName</span></span>
<span data-ttu-id="1cc4c-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1cc4c-125">The resource group name</span></span>

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

### <span data-ttu-id="1cc4c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cc4c-126">-ResourceId</span></span>
<span data-ttu-id="1cc4c-127">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="1cc4c-127">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cc4c-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1cc4c-128">-ServerName</span></span>
<span data-ttu-id="1cc4c-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="1cc4c-129">The server name</span></span>

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

### <span data-ttu-id="1cc4c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cc4c-130">-Confirm</span></span>
<span data-ttu-id="1cc4c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1cc4c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc4c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc4c-132">-WhatIf</span></span>
<span data-ttu-id="1cc4c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1cc4c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc4c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1cc4c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc4c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc4c-135">CommonParameters</span></span>
<span data-ttu-id="1cc4c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1cc4c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc4c-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cc4c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc4c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1cc4c-138">INPUTS</span></span>

### <span data-ttu-id="1cc4c-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="1cc4c-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="1cc4c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cc4c-140">OUTPUTS</span></span>

### <span data-ttu-id="1cc4c-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="1cc4c-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="1cc4c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1cc4c-142">NOTES</span></span>

## <span data-ttu-id="1cc4c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cc4c-143">RELATED LINKS</span></span>
