---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 5ef58938342845b437d714e44a55256892632546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002952"
---
# <span data-ttu-id="f534a-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f534a-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="f534a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f534a-102">SYNOPSIS</span></span>
<span data-ttu-id="f534a-103">Обновляет состояние рекомендуемого SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f534a-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="f534a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f534a-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f534a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f534a-105">DESCRIPTION</span></span>
<span data-ttu-id="f534a-106">Состояние **cmdletState Set-AzSqlElasticPoolRecommendedActionState** обновляется в состоянии рекомендуемого SQL Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f534a-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="f534a-107">Этот cmdlet применяет рекомендуемое действие, возвращается в состояние "Отменено" или "Удаляется" в зависимости от нового состояния.</span><span class="sxs-lookup"><span data-stu-id="f534a-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="f534a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f534a-108">EXAMPLES</span></span>

### <span data-ttu-id="f534a-109">Пример 1. Обновление состояния рекомендуемого действия на "Ожидание ожидания"</span><span class="sxs-lookup"><span data-stu-id="f534a-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="f534a-110">Эта команда обновляет состояние рекомендуемого пула эластичности с именем IR_ \[ test_schema \] _ \[ test_table_0.0361551 \] _6C7AE8CC9C87E7FD5893 ожиданию.</span><span class="sxs-lookup"><span data-stu-id="f534a-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="f534a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f534a-111">PARAMETERS</span></span>

### <span data-ttu-id="f534a-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="f534a-112">-AdvisorName</span></span>
<span data-ttu-id="f534a-113">Имя консультанта, к которому относится это рекомендуемое действие.</span><span class="sxs-lookup"><span data-stu-id="f534a-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f534a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f534a-114">-DefaultProfile</span></span>
<span data-ttu-id="f534a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f534a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f534a-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f534a-116">-ElasticPoolName</span></span>
<span data-ttu-id="f534a-117">Определяет имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="f534a-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f534a-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="f534a-118">-RecommendedActionName</span></span>
<span data-ttu-id="f534a-119">Указывает имя рекомендуемого действия, для которого этот cmdlet обновляет состояние.</span><span class="sxs-lookup"><span data-stu-id="f534a-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f534a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f534a-120">-ResourceGroupName</span></span>
<span data-ttu-id="f534a-121">Указывает имя группы ресурсов сервера, который содержит этот эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="f534a-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f534a-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f534a-122">-ServerName</span></span>
<span data-ttu-id="f534a-123">Указывает имя сервера, на который находится эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="f534a-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f534a-124">-State</span><span class="sxs-lookup"><span data-stu-id="f534a-124">-State</span></span>
<span data-ttu-id="f534a-125">Определяет значение, до которого этот cmdlet обновляет рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="f534a-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="f534a-126">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="f534a-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f534a-127">Активные</span><span class="sxs-lookup"><span data-stu-id="f534a-127">Active</span></span>
- <span data-ttu-id="f534a-128">Ожидание</span><span class="sxs-lookup"><span data-stu-id="f534a-128">Pending</span></span>
- <span data-ttu-id="f534a-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="f534a-129">PendingRevert</span></span>
- <span data-ttu-id="f534a-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="f534a-130">RevertCancelled</span></span>
- <span data-ttu-id="f534a-131">Пропущено</span><span class="sxs-lookup"><span data-stu-id="f534a-131">Ignored</span></span>
- <span data-ttu-id="f534a-132">Разрешено</span><span class="sxs-lookup"><span data-stu-id="f534a-132">Resolved</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f534a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f534a-133">-Confirm</span></span>
<span data-ttu-id="f534a-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f534a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f534a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f534a-135">-WhatIf</span></span>
<span data-ttu-id="f534a-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f534a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f534a-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f534a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f534a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f534a-138">CommonParameters</span></span>
<span data-ttu-id="f534a-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f534a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f534a-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f534a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f534a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f534a-141">INPUTS</span></span>

### <span data-ttu-id="f534a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f534a-142">System.String</span></span>

### <span data-ttu-id="f534a-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f534a-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="f534a-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f534a-144">OUTPUTS</span></span>

### <span data-ttu-id="f534a-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="f534a-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="f534a-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f534a-146">NOTES</span></span>
* <span data-ttu-id="f534a-147">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql,элестика, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="f534a-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="f534a-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f534a-148">RELATED LINKS</span></span>

[<span data-ttu-id="f534a-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="f534a-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="f534a-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f534a-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="f534a-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f534a-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="f534a-152">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="f534a-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
