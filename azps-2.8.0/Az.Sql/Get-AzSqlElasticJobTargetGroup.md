---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: fd2f8cc12faa1a08eb8f30743c88d5d3e44e48fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906353"
---
# <span data-ttu-id="07563-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="07563-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="07563-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07563-102">SYNOPSIS</span></span>
<span data-ttu-id="07563-103">Возвращает одну или несколько конечных групп заданий.</span><span class="sxs-lookup"><span data-stu-id="07563-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="07563-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07563-104">SYNTAX</span></span>

### <span data-ttu-id="07563-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07563-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07563-106">Объект</span><span class="sxs-lookup"><span data-stu-id="07563-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07563-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="07563-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07563-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07563-108">DESCRIPTION</span></span>
<span data-ttu-id="07563-109">Командлет Get-AzSqlElasticJobTargetGroup получает целевую группу, а также ее целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="07563-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="07563-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07563-110">EXAMPLES</span></span>

### <span data-ttu-id="07563-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07563-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="07563-112">Получает целевую группу и ее целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="07563-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="07563-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07563-113">PARAMETERS</span></span>

### <span data-ttu-id="07563-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="07563-114">-AgentName</span></span>
<span data-ttu-id="07563-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="07563-115">The agent name</span></span>

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

### <span data-ttu-id="07563-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07563-116">-DefaultProfile</span></span>
<span data-ttu-id="07563-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07563-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07563-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07563-118">-Name</span></span>
<span data-ttu-id="07563-119">Имя целевой группы</span><span class="sxs-lookup"><span data-stu-id="07563-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07563-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="07563-120">-ParentObject</span></span>
<span data-ttu-id="07563-121">Объект Agent</span><span class="sxs-lookup"><span data-stu-id="07563-121">The agent object</span></span>

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

### <span data-ttu-id="07563-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="07563-122">-ParentResourceId</span></span>
<span data-ttu-id="07563-123">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="07563-123">The agent resource id</span></span>

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

### <span data-ttu-id="07563-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07563-124">-ResourceGroupName</span></span>
<span data-ttu-id="07563-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="07563-125">The resource group name</span></span>

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

### <span data-ttu-id="07563-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="07563-126">-ServerName</span></span>
<span data-ttu-id="07563-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="07563-127">The server name</span></span>

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

### <span data-ttu-id="07563-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07563-128">CommonParameters</span></span>
<span data-ttu-id="07563-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07563-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07563-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07563-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07563-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07563-131">INPUTS</span></span>

### <span data-ttu-id="07563-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="07563-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="07563-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07563-133">OUTPUTS</span></span>

### <span data-ttu-id="07563-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="07563-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="07563-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="07563-135">NOTES</span></span>

## <span data-ttu-id="07563-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07563-136">RELATED LINKS</span></span>
