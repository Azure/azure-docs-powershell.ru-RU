---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248788"
---
# <span data-ttu-id="9ccbb-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9ccbb-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="9ccbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ccbb-102">SYNOPSIS</span></span>
<span data-ttu-id="9ccbb-103">Обновляет состояние рекомендуемого действия для пула эластичных БД Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="9ccbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ccbb-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ccbb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ccbb-105">DESCRIPTION</span></span>
<span data-ttu-id="9ccbb-106">Состояние обновления командлета **Set-AzSqlElasticPoolRecommendedActionState** рекомендуемого действия для пула эластичных БД Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="9ccbb-107">Этот командлет применяет рекомендуемое действие, отменяет или удаляет его в соответствии с новым состоянием.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="9ccbb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ccbb-108">EXAMPLES</span></span>

### <span data-ttu-id="9ccbb-109">Пример 1: обновление состояния рекомендуемого действия на ожидание</span><span class="sxs-lookup"><span data-stu-id="9ccbb-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="9ccbb-110">Эта команда обновляет состояние рекомендуемого действия для пула эластичных БД с именем IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 — ожидание.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="9ccbb-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ccbb-111">PARAMETERS</span></span>

### <span data-ttu-id="9ccbb-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="9ccbb-112">-AdvisorName</span></span>
<span data-ttu-id="9ccbb-113">Указывает имя помощника, которому принадлежит рекомендуемое действие.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="9ccbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ccbb-114">-DefaultProfile</span></span>
<span data-ttu-id="9ccbb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9ccbb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ccbb-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9ccbb-116">-ElasticPoolName</span></span>
<span data-ttu-id="9ccbb-117">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="9ccbb-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="9ccbb-118">-RecommendedActionName</span></span>
<span data-ttu-id="9ccbb-119">Указывает имя рекомендуемого действия, для которого этот командлет обновляет состояние.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="9ccbb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ccbb-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ccbb-121">Указывает имя группы ресурсов сервера, содержащего этот эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="9ccbb-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9ccbb-122">-ServerName</span></span>
<span data-ttu-id="9ccbb-123">Указывает имя сервера, на котором находится пул эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="9ccbb-124">-State</span><span class="sxs-lookup"><span data-stu-id="9ccbb-124">-State</span></span>
<span data-ttu-id="9ccbb-125">Указывает значение, на которое этот командлет обновляет рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="9ccbb-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9ccbb-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9ccbb-127">Службы</span><span class="sxs-lookup"><span data-stu-id="9ccbb-127">Active</span></span>
- <span data-ttu-id="9ccbb-128">Типа</span><span class="sxs-lookup"><span data-stu-id="9ccbb-128">Pending</span></span>
- <span data-ttu-id="9ccbb-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="9ccbb-129">PendingRevert</span></span>
- <span data-ttu-id="9ccbb-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="9ccbb-130">RevertCancelled</span></span>
- <span data-ttu-id="9ccbb-131">Учитываться</span><span class="sxs-lookup"><span data-stu-id="9ccbb-131">Ignored</span></span>
- <span data-ttu-id="9ccbb-132">Разрешившего</span><span class="sxs-lookup"><span data-stu-id="9ccbb-132">Resolved</span></span>

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

### <span data-ttu-id="9ccbb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ccbb-133">-Confirm</span></span>
<span data-ttu-id="9ccbb-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ccbb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ccbb-135">-WhatIf</span></span>
<span data-ttu-id="9ccbb-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ccbb-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ccbb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ccbb-138">CommonParameters</span></span>
<span data-ttu-id="9ccbb-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ccbb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ccbb-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ccbb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ccbb-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ccbb-141">INPUTS</span></span>

### <span data-ttu-id="9ccbb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9ccbb-142">System.String</span></span>

### <span data-ttu-id="9ccbb-143">Microsoft. Azure. Commands. SQL. RecommendedAction. командлет. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9ccbb-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="9ccbb-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ccbb-144">OUTPUTS</span></span>

### <span data-ttu-id="9ccbb-145">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="9ccbb-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="9ccbb-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ccbb-146">NOTES</span></span>
* <span data-ttu-id="9ccbb-147">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="9ccbb-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="9ccbb-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ccbb-148">RELATED LINKS</span></span>

[<span data-ttu-id="9ccbb-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="9ccbb-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="9ccbb-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9ccbb-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="9ccbb-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9ccbb-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="9ccbb-152">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9ccbb-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
