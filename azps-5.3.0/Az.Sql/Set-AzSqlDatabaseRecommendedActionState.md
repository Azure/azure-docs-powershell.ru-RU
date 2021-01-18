---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 6d634760080e3fb26153b747e733369b20bc8336
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504751"
---
# <span data-ttu-id="f7d9f-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f7d9f-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="f7d9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d9f-103">Обновляет состояние рекомендуемого действия для базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="f7d9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7d9f-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d9f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7d9f-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d9f-106">Для обновления состояния рекомендуемой базы данных Azure SQL состояние **"Set-AzSqlDatabaseRecommendedActionState".**</span><span class="sxs-lookup"><span data-stu-id="f7d9f-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="f7d9f-107">Это позволит применить, отменить или отменить рекомендуемое действие в зависимости от нового состояния.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="f7d9f-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7d9f-108">EXAMPLES</span></span>

### <span data-ttu-id="f7d9f-109">Пример 1. Применение рекомендуемых состояния действий к ожиданию</span><span class="sxs-lookup"><span data-stu-id="f7d9f-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

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

<span data-ttu-id="f7d9f-110">Эта команда обновляет состояние рекомендуемого действия IR_ \[ test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893, которое принадлежит к базе данных \] WiRunner в ожидании.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="f7d9f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7d9f-111">PARAMETERS</span></span>

### <span data-ttu-id="f7d9f-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="f7d9f-112">-AdvisorName</span></span>
<span data-ttu-id="f7d9f-113">Имя консультанта, к которому относится это рекомендуемое действие.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="f7d9f-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f7d9f-114">-DatabaseName</span></span>
<span data-ttu-id="f7d9f-115">Задает имя базы данных, для которой этот cmdlet задает рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="f7d9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d9f-116">-DefaultProfile</span></span>
<span data-ttu-id="f7d9f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7d9f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7d9f-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="f7d9f-118">-RecommendedActionName</span></span>
<span data-ttu-id="f7d9f-119">Указывает имя рекомендуемого действия, для которого обновляется состояние.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="f7d9f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d9f-120">-ResourceGroupName</span></span>
<span data-ttu-id="f7d9f-121">Указывает имя группы ресурсов сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="f7d9f-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f7d9f-122">-ServerName</span></span>
<span data-ttu-id="f7d9f-123">Указывает имя сервера, на базе которого находится база данных.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="f7d9f-124">-State</span><span class="sxs-lookup"><span data-stu-id="f7d9f-124">-State</span></span>
<span data-ttu-id="f7d9f-125">Определяет новое значение, до которого этот cmdlet обновляет рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="f7d9f-126">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="f7d9f-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7d9f-127">Активные</span><span class="sxs-lookup"><span data-stu-id="f7d9f-127">Active</span></span>
- <span data-ttu-id="f7d9f-128">Ожидание</span><span class="sxs-lookup"><span data-stu-id="f7d9f-128">Pending</span></span>
- <span data-ttu-id="f7d9f-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="f7d9f-129">PendingRevert</span></span>
- <span data-ttu-id="f7d9f-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="f7d9f-130">RevertCancelled</span></span>
- <span data-ttu-id="f7d9f-131">Пропущено</span><span class="sxs-lookup"><span data-stu-id="f7d9f-131">Ignored</span></span>
- <span data-ttu-id="f7d9f-132">Разрешено</span><span class="sxs-lookup"><span data-stu-id="f7d9f-132">Resolved</span></span>

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

### <span data-ttu-id="f7d9f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7d9f-133">-Confirm</span></span>
<span data-ttu-id="f7d9f-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d9f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d9f-135">-WhatIf</span></span>
<span data-ttu-id="f7d9f-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d9f-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d9f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d9f-138">CommonParameters</span></span>
<span data-ttu-id="f7d9f-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d9f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d9f-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7d9f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d9f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7d9f-141">INPUTS</span></span>

### <span data-ttu-id="f7d9f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f7d9f-142">System.String</span></span>

### <span data-ttu-id="f7d9f-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f7d9f-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="f7d9f-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7d9f-144">OUTPUTS</span></span>

### <span data-ttu-id="f7d9f-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="f7d9f-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="f7d9f-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7d9f-146">NOTES</span></span>
* <span data-ttu-id="f7d9f-147">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="f7d9f-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="f7d9f-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7d9f-148">RELATED LINKS</span></span>

[<span data-ttu-id="f7d9f-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="f7d9f-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="f7d9f-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="f7d9f-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="f7d9f-151">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="f7d9f-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="f7d9f-152">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="f7d9f-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="f7d9f-153">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f7d9f-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="f7d9f-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f7d9f-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="f7d9f-155">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f7d9f-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="f7d9f-156">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f7d9f-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="f7d9f-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f7d9f-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="f7d9f-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f7d9f-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="f7d9f-159">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="f7d9f-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
