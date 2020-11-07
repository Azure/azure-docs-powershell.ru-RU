---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 688926d05b56234ce11d4524afdcce326c5e09e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906170"
---
# <span data-ttu-id="d1c50-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="d1c50-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="d1c50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1c50-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c50-103">Получение одного или нескольких заданий</span><span class="sxs-lookup"><span data-stu-id="d1c50-103">Gets one or more jobs</span></span>

## <span data-ttu-id="d1c50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1c50-104">SYNTAX</span></span>

### <span data-ttu-id="d1c50-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1c50-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1c50-106">Объект</span><span class="sxs-lookup"><span data-stu-id="d1c50-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1c50-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d1c50-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1c50-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1c50-108">DESCRIPTION</span></span>
<span data-ttu-id="d1c50-109">Командлет Get-AzSqlElasticJob получает одно или несколько заданий.</span><span class="sxs-lookup"><span data-stu-id="d1c50-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="d1c50-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1c50-110">EXAMPLES</span></span>

### <span data-ttu-id="d1c50-111">Пример 1 — получение задания</span><span class="sxs-lookup"><span data-stu-id="d1c50-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="d1c50-112">Получает задание</span><span class="sxs-lookup"><span data-stu-id="d1c50-112">Gets a job</span></span>

## <span data-ttu-id="d1c50-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1c50-113">PARAMETERS</span></span>

### <span data-ttu-id="d1c50-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d1c50-114">-AgentName</span></span>
<span data-ttu-id="d1c50-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="d1c50-115">The agent name</span></span>

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

### <span data-ttu-id="d1c50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c50-116">-DefaultProfile</span></span>
<span data-ttu-id="d1c50-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1c50-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1c50-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1c50-118">-Name</span></span>
<span data-ttu-id="d1c50-119">Имя задания</span><span class="sxs-lookup"><span data-stu-id="d1c50-119">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c50-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1c50-120">-ParentObject</span></span>
<span data-ttu-id="d1c50-121">Входной объект агента</span><span class="sxs-lookup"><span data-stu-id="d1c50-121">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c50-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d1c50-122">-ParentResourceId</span></span>
<span data-ttu-id="d1c50-123">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="d1c50-123">The agent resource id</span></span>

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

### <span data-ttu-id="d1c50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c50-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1c50-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d1c50-125">The resource group name</span></span>

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

### <span data-ttu-id="d1c50-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d1c50-126">-ServerName</span></span>
<span data-ttu-id="d1c50-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="d1c50-127">The server name</span></span>

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

### <span data-ttu-id="d1c50-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c50-128">CommonParameters</span></span>
<span data-ttu-id="d1c50-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1c50-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c50-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1c50-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c50-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1c50-131">INPUTS</span></span>

### <span data-ttu-id="d1c50-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d1c50-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d1c50-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1c50-133">OUTPUTS</span></span>

### <span data-ttu-id="d1c50-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="d1c50-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="d1c50-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1c50-135">NOTES</span></span>

## <span data-ttu-id="d1c50-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1c50-136">RELATED LINKS</span></span>
