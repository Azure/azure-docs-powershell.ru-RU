---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 4652774b07ca3ae58baf29b614bd63519d537a0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906522"
---
# <span data-ttu-id="3a4e6-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="3a4e6-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="3a4e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4e6-103">Удаляет целевую группу</span><span class="sxs-lookup"><span data-stu-id="3a4e6-103">Removes the target group</span></span>

## <span data-ttu-id="3a4e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a4e6-104">SYNTAX</span></span>

### <span data-ttu-id="3a4e6-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a4e6-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a4e6-106">Объект</span><span class="sxs-lookup"><span data-stu-id="3a4e6-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a4e6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3a4e6-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a4e6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a4e6-108">DESCRIPTION</span></span>
<span data-ttu-id="3a4e6-109">Командлет Remove-AzSqlElasticJobTargetGroup удаляет целевую группу и ее целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="3a4e6-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="3a4e6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a4e6-110">EXAMPLES</span></span>

### <span data-ttu-id="3a4e6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a4e6-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="3a4e6-112">Удаляет целевую группу и ее целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="3a4e6-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="3a4e6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a4e6-113">PARAMETERS</span></span>

### <span data-ttu-id="3a4e6-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3a4e6-114">-AgentName</span></span>
<span data-ttu-id="3a4e6-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="3a4e6-115">The agent name</span></span>

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

### <span data-ttu-id="3a4e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4e6-116">-DefaultProfile</span></span>
<span data-ttu-id="3a4e6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a4e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a4e6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3a4e6-118">-Force</span></span>
<span data-ttu-id="3a4e6-119">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="3a4e6-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3a4e6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a4e6-120">-InputObject</span></span>
<span data-ttu-id="3a4e6-121">Целевой объект группы</span><span class="sxs-lookup"><span data-stu-id="3a4e6-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4e6-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a4e6-122">-Name</span></span>
<span data-ttu-id="3a4e6-123">Имя целевой группы</span><span class="sxs-lookup"><span data-stu-id="3a4e6-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a4e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a4e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a4e6-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3a4e6-125">The resource group name</span></span>

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

### <span data-ttu-id="3a4e6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a4e6-126">-ResourceId</span></span>
<span data-ttu-id="3a4e6-127">Идентификатор ресурса целевой группы</span><span class="sxs-lookup"><span data-stu-id="3a4e6-127">The target group resource id</span></span>

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

### <span data-ttu-id="3a4e6-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3a4e6-128">-ServerName</span></span>
<span data-ttu-id="3a4e6-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="3a4e6-129">The server name</span></span>

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

### <span data-ttu-id="3a4e6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a4e6-130">-Confirm</span></span>
<span data-ttu-id="3a4e6-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a4e6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a4e6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a4e6-132">-WhatIf</span></span>
<span data-ttu-id="3a4e6-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a4e6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a4e6-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a4e6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a4e6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4e6-135">CommonParameters</span></span>
<span data-ttu-id="3a4e6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a4e6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4e6-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a4e6-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4e6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a4e6-138">INPUTS</span></span>

### <span data-ttu-id="3a4e6-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="3a4e6-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="3a4e6-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a4e6-140">OUTPUTS</span></span>

### <span data-ttu-id="3a4e6-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="3a4e6-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="3a4e6-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a4e6-142">NOTES</span></span>

## <span data-ttu-id="3a4e6-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a4e6-143">RELATED LINKS</span></span>
