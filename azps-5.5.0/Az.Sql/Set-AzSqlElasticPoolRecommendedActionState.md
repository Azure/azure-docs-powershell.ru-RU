---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210817"
---
# <span data-ttu-id="1d989-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1d989-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="1d989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d989-102">SYNOPSIS</span></span>
<span data-ttu-id="1d989-103">Обновляет состояние рекомендуемого SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1d989-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="1d989-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d989-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d989-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d989-105">DESCRIPTION</span></span>
<span data-ttu-id="1d989-106">Состояние **cmdletState Set-AzSqlElasticPoolRecommendedActionState** обновляется в состоянии рекомендуемого SQL Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1d989-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="1d989-107">Этот cmdlet применяет рекомендуемое действие, возвращает его в состояние "Отменено" или "Отменено" в зависимости от нового состояния.</span><span class="sxs-lookup"><span data-stu-id="1d989-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="1d989-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d989-108">EXAMPLES</span></span>

### <span data-ttu-id="1d989-109">Пример 1. Обновление состояния рекомендуемого действия на "Ожидание ожидания"</span><span class="sxs-lookup"><span data-stu-id="1d989-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="1d989-110">Эта команда обновляет состояние рекомендуемого бинастика с именем IR_ \[ test_schema \] _ \[ test_table_0.0361551 \] _6C7AE8CC9C87E7FD5893 ожиданию.</span><span class="sxs-lookup"><span data-stu-id="1d989-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="1d989-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d989-111">PARAMETERS</span></span>

### <span data-ttu-id="1d989-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1d989-112">-AdvisorName</span></span>
<span data-ttu-id="1d989-113">Имя консультанта, к которому относится это рекомендуемое действие.</span><span class="sxs-lookup"><span data-stu-id="1d989-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="1d989-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d989-114">-DefaultProfile</span></span>
<span data-ttu-id="1d989-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1d989-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d989-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1d989-116">-ElasticPoolName</span></span>
<span data-ttu-id="1d989-117">Определяет имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="1d989-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="1d989-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="1d989-118">-RecommendedActionName</span></span>
<span data-ttu-id="1d989-119">Указывает имя рекомендуемого действия, для которого этот cmdlet обновляет состояние.</span><span class="sxs-lookup"><span data-stu-id="1d989-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="1d989-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d989-120">-ResourceGroupName</span></span>
<span data-ttu-id="1d989-121">Указывает имя группы ресурсов сервера, который содержит этот эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="1d989-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="1d989-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1d989-122">-ServerName</span></span>
<span data-ttu-id="1d989-123">Указывает имя сервера, на который находится эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="1d989-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="1d989-124">-State</span><span class="sxs-lookup"><span data-stu-id="1d989-124">-State</span></span>
<span data-ttu-id="1d989-125">Определяет значение, до которого этот cmdlet обновляет рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="1d989-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="1d989-126">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="1d989-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d989-127">Активные</span><span class="sxs-lookup"><span data-stu-id="1d989-127">Active</span></span>
- <span data-ttu-id="1d989-128">Ожидание</span><span class="sxs-lookup"><span data-stu-id="1d989-128">Pending</span></span>
- <span data-ttu-id="1d989-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="1d989-129">PendingRevert</span></span>
- <span data-ttu-id="1d989-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="1d989-130">RevertCancelled</span></span>
- <span data-ttu-id="1d989-131">Пропущено</span><span class="sxs-lookup"><span data-stu-id="1d989-131">Ignored</span></span>
- <span data-ttu-id="1d989-132">Разрешено</span><span class="sxs-lookup"><span data-stu-id="1d989-132">Resolved</span></span>

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

### <span data-ttu-id="1d989-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d989-133">-Confirm</span></span>
<span data-ttu-id="1d989-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1d989-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d989-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d989-135">-WhatIf</span></span>
<span data-ttu-id="1d989-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d989-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d989-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d989-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d989-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d989-138">CommonParameters</span></span>
<span data-ttu-id="1d989-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d989-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d989-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d989-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d989-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d989-141">INPUTS</span></span>

### <span data-ttu-id="1d989-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1d989-142">System.String</span></span>

### <span data-ttu-id="1d989-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1d989-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="1d989-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d989-144">OUTPUTS</span></span>

### <span data-ttu-id="1d989-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="1d989-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="1d989-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d989-146">NOTES</span></span>
* <span data-ttu-id="1d989-147">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql,элестика, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="1d989-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="1d989-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d989-148">RELATED LINKS</span></span>

[<span data-ttu-id="1d989-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1d989-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="1d989-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1d989-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="1d989-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1d989-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="1d989-152">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="1d989-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
