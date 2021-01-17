---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400420"
---
# <span data-ttu-id="b3957-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b3957-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="b3957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3957-102">SYNOPSIS</span></span>
<span data-ttu-id="b3957-103">Обновляет состояние рекомендуемого действия Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b3957-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="b3957-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3957-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3957-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3957-105">DESCRIPTION</span></span>
<span data-ttu-id="b3957-106">Состояние SQL Server Azure состояние **cmdlet Set-AzSqlServerRecommendedActionState.**</span><span class="sxs-lookup"><span data-stu-id="b3957-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="b3957-107">Этот cmdlet применяет, возвращает или удаляет рекомендуемое действие в зависимости от нового состояния.</span><span class="sxs-lookup"><span data-stu-id="b3957-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="b3957-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3957-108">EXAMPLES</span></span>

### <span data-ttu-id="b3957-109">Пример1. Обновление состояния указанного рекомендуемого действия на "Ожидание ожидания"</span><span class="sxs-lookup"><span data-stu-id="b3957-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="b3957-110">Обновление состояния рекомендуемого действия сервера "IR_ \[ test_schema _ \] \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893" на \] "Ожидание".</span><span class="sxs-lookup"><span data-stu-id="b3957-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="b3957-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3957-111">PARAMETERS</span></span>

### <span data-ttu-id="b3957-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="b3957-112">-AdvisorName</span></span>
<span data-ttu-id="b3957-113">Указывает имя консультанта, который содержит рекомендуемое действие.</span><span class="sxs-lookup"><span data-stu-id="b3957-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="b3957-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3957-114">-DefaultProfile</span></span>
<span data-ttu-id="b3957-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b3957-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3957-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="b3957-116">-RecommendedActionName</span></span>
<span data-ttu-id="b3957-117">Указывает имя рекомендуемого действия, для которого этот cmdlet обновляет состояние.</span><span class="sxs-lookup"><span data-stu-id="b3957-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="b3957-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3957-118">-ResourceGroupName</span></span>
<span data-ttu-id="b3957-119">Указывает имя группы ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="b3957-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="b3957-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3957-120">-ServerName</span></span>
<span data-ttu-id="b3957-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b3957-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b3957-122">-State</span><span class="sxs-lookup"><span data-stu-id="b3957-122">-State</span></span>
<span data-ttu-id="b3957-123">Определяет новое значение, до которого этот cmdlet обновляет рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="b3957-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="b3957-124">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="b3957-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b3957-125">Активные</span><span class="sxs-lookup"><span data-stu-id="b3957-125">Active</span></span>
- <span data-ttu-id="b3957-126">Ожидание</span><span class="sxs-lookup"><span data-stu-id="b3957-126">Pending</span></span>
- <span data-ttu-id="b3957-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="b3957-127">PendingRevert</span></span>
- <span data-ttu-id="b3957-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="b3957-128">RevertCancelled</span></span>
- <span data-ttu-id="b3957-129">Пропущено</span><span class="sxs-lookup"><span data-stu-id="b3957-129">Ignored</span></span>
- <span data-ttu-id="b3957-130">Разрешено</span><span class="sxs-lookup"><span data-stu-id="b3957-130">Resolved</span></span>

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

### <span data-ttu-id="b3957-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3957-131">-Confirm</span></span>
<span data-ttu-id="b3957-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b3957-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3957-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3957-133">-WhatIf</span></span>
<span data-ttu-id="b3957-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3957-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3957-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b3957-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3957-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3957-136">CommonParameters</span></span>
<span data-ttu-id="b3957-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3957-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3957-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3957-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3957-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3957-139">INPUTS</span></span>

### <span data-ttu-id="b3957-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b3957-140">System.String</span></span>

### <span data-ttu-id="b3957-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b3957-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="b3957-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3957-142">OUTPUTS</span></span>

### <span data-ttu-id="b3957-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="b3957-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="b3957-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3957-144">NOTES</span></span>
* <span data-ttu-id="b3957-145">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="b3957-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="b3957-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3957-146">RELATED LINKS</span></span>

[<span data-ttu-id="b3957-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b3957-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="b3957-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b3957-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="b3957-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b3957-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="b3957-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b3957-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="b3957-151">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="b3957-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
