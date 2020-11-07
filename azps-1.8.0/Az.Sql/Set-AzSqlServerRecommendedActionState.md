---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: b8be70708ddb504825f151eedbf7b3d0502d2781
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728751"
---
# <span data-ttu-id="f56f8-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f56f8-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="f56f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f56f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f56f8-103">Обновляет состояние рекомендуемого действия для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f56f8-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="f56f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f56f8-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f56f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f56f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f56f8-106">Состояние обновления командлета **Set-AzSqlServerRecommendedActionState** , рекомендованное действием Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f56f8-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="f56f8-107">Этот командлет применяется, Возвращает или сбрасывает рекомендованное действие на основе нового состояния.</span><span class="sxs-lookup"><span data-stu-id="f56f8-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="f56f8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f56f8-108">EXAMPLES</span></span>

### <span data-ttu-id="f56f8-109">Example1: обновление состояния указанного рекомендуемого действия на ожидание</span><span class="sxs-lookup"><span data-stu-id="f56f8-109">Example1: Update the state of the specified recommended action to Pending</span></span>
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

<span data-ttu-id="f56f8-110">Обновляет состояние рекомендуемого для сервера действия с именем "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" на "ожидание"</span><span class="sxs-lookup"><span data-stu-id="f56f8-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="f56f8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f56f8-111">PARAMETERS</span></span>

### <span data-ttu-id="f56f8-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="f56f8-112">-AdvisorName</span></span>
<span data-ttu-id="f56f8-113">Указывает имя помощника, содержащего рекомендованное действие.</span><span class="sxs-lookup"><span data-stu-id="f56f8-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="f56f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f56f8-114">-DefaultProfile</span></span>
<span data-ttu-id="f56f8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f56f8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f56f8-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="f56f8-116">-RecommendedActionName</span></span>
<span data-ttu-id="f56f8-117">Указывает имя рекомендуемого действия, для которого этот командлет обновляет состояние.</span><span class="sxs-lookup"><span data-stu-id="f56f8-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="f56f8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f56f8-118">-ResourceGroupName</span></span>
<span data-ttu-id="f56f8-119">Указывает имя группы ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="f56f8-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="f56f8-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f56f8-120">-ServerName</span></span>
<span data-ttu-id="f56f8-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f56f8-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f56f8-122">-State</span><span class="sxs-lookup"><span data-stu-id="f56f8-122">-State</span></span>
<span data-ttu-id="f56f8-123">Указывает новое значение, на которое этот командлет обновляет рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="f56f8-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="f56f8-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f56f8-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f56f8-125">Службы</span><span class="sxs-lookup"><span data-stu-id="f56f8-125">Active</span></span>
- <span data-ttu-id="f56f8-126">Типа</span><span class="sxs-lookup"><span data-stu-id="f56f8-126">Pending</span></span>
- <span data-ttu-id="f56f8-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="f56f8-127">PendingRevert</span></span>
- <span data-ttu-id="f56f8-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="f56f8-128">RevertCancelled</span></span>
- <span data-ttu-id="f56f8-129">Учитываться</span><span class="sxs-lookup"><span data-stu-id="f56f8-129">Ignored</span></span>
- <span data-ttu-id="f56f8-130">Разрешившего</span><span class="sxs-lookup"><span data-stu-id="f56f8-130">Resolved</span></span>

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

### <span data-ttu-id="f56f8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f56f8-131">-Confirm</span></span>
<span data-ttu-id="f56f8-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f56f8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f56f8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f56f8-133">-WhatIf</span></span>
<span data-ttu-id="f56f8-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f56f8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f56f8-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f56f8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f56f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f56f8-136">CommonParameters</span></span>
<span data-ttu-id="f56f8-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f56f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f56f8-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f56f8-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f56f8-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f56f8-139">INPUTS</span></span>

### <span data-ttu-id="f56f8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f56f8-140">System.String</span></span>

### <span data-ttu-id="f56f8-141">Microsoft. Azure. Commands. SQL. RecommendedAction. командлет. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f56f8-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="f56f8-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f56f8-142">OUTPUTS</span></span>

### <span data-ttu-id="f56f8-143">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="f56f8-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="f56f8-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="f56f8-144">NOTES</span></span>
* <span data-ttu-id="f56f8-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, сервер, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="f56f8-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="f56f8-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f56f8-146">RELATED LINKS</span></span>

[<span data-ttu-id="f56f8-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="f56f8-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="f56f8-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="f56f8-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="f56f8-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f56f8-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="f56f8-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f56f8-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="f56f8-151">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f56f8-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
