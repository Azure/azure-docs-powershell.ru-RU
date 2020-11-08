---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236596"
---
# <span data-ttu-id="f8a00-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="f8a00-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="f8a00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8a00-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a00-103">Возвращает один или несколько шагов задания.</span><span class="sxs-lookup"><span data-stu-id="f8a00-103">Gets one or more job steps</span></span>

## <span data-ttu-id="f8a00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8a00-104">SYNTAX</span></span>

### <span data-ttu-id="f8a00-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8a00-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a00-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="f8a00-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8a00-107">Объект</span><span class="sxs-lookup"><span data-stu-id="f8a00-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a00-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="f8a00-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a00-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f8a00-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a00-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f8a00-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8a00-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8a00-111">DESCRIPTION</span></span>
<span data-ttu-id="f8a00-112">Командлет Get-AzSqlElasticJobStep получает один или несколько шагов задания из задания.</span><span class="sxs-lookup"><span data-stu-id="f8a00-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="f8a00-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8a00-113">EXAMPLES</span></span>

### <span data-ttu-id="f8a00-114">Пример 1: получение шага задания из задания</span><span class="sxs-lookup"><span data-stu-id="f8a00-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="f8a00-115">Получает шаг задания из задания</span><span class="sxs-lookup"><span data-stu-id="f8a00-115">Gets a job step from a job</span></span>

## <span data-ttu-id="f8a00-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8a00-116">PARAMETERS</span></span>

### <span data-ttu-id="f8a00-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f8a00-117">-AgentName</span></span>
<span data-ttu-id="f8a00-118">Имя агента</span><span class="sxs-lookup"><span data-stu-id="f8a00-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a00-119">-DefaultProfile</span></span>
<span data-ttu-id="f8a00-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a00-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8a00-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="f8a00-121">-JobName</span></span>
<span data-ttu-id="f8a00-122">Имя задания</span><span class="sxs-lookup"><span data-stu-id="f8a00-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a00-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8a00-123">-Name</span></span>
<span data-ttu-id="f8a00-124">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="f8a00-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a00-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f8a00-125">-ParentObject</span></span>
<span data-ttu-id="f8a00-126">Входной объект задания</span><span class="sxs-lookup"><span data-stu-id="f8a00-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a00-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f8a00-127">-ParentResourceId</span></span>
<span data-ttu-id="f8a00-128">Идентификатор ресурса задания</span><span class="sxs-lookup"><span data-stu-id="f8a00-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a00-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a00-129">-ResourceGroupName</span></span>
<span data-ttu-id="f8a00-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f8a00-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a00-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f8a00-131">-ServerName</span></span>
<span data-ttu-id="f8a00-132">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="f8a00-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a00-133">-Version</span><span class="sxs-lookup"><span data-stu-id="f8a00-133">-Version</span></span>
<span data-ttu-id="f8a00-134">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="f8a00-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a00-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a00-135">CommonParameters</span></span>
<span data-ttu-id="f8a00-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8a00-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a00-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8a00-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a00-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8a00-138">INPUTS</span></span>

### <span data-ttu-id="f8a00-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f8a00-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f8a00-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8a00-140">OUTPUTS</span></span>

### <span data-ttu-id="f8a00-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="f8a00-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="f8a00-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8a00-142">NOTES</span></span>

## <span data-ttu-id="f8a00-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8a00-143">RELATED LINKS</span></span>
