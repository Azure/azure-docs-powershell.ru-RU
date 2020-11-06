---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: d31af9321a474c1261b2ed75138696d9f1a45461
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562023"
---
# <span data-ttu-id="b6a1e-101">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b6a1e-101">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="b6a1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a1e-103">Обновляет состояние рекомендуемого действия для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-103">Updates the state of an Azure SQL Database recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6a1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6a1e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6a1e-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a1e-106">Командлет **Set-AzureRmSqlDatabaseRecommendedActionState** обновляет состояние рекомендуемого действия базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-106">The **Set-AzureRmSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="b6a1e-107">Это позволяет применять рекомендованное действие, возвращая или удаляя его в зависимости от нового состояния.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="b6a1e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6a1e-108">EXAMPLES</span></span>

### <span data-ttu-id="b6a1e-109">Пример 1: применение рекомендуемого состояния действия к ожиданию</span><span class="sxs-lookup"><span data-stu-id="b6a1e-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="b6a1e-110">Эта команда обновляет состояние рекомендуемого действия с именем IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893, которое принадлежит базе данных с именем WIRunner, в ожидание.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="b6a1e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6a1e-111">PARAMETERS</span></span>

### <span data-ttu-id="b6a1e-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="b6a1e-112">-AdvisorName</span></span>
<span data-ttu-id="b6a1e-113">Указывает имя помощника, которому принадлежит рекомендуемое действие.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="b6a1e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b6a1e-114">-DatabaseName</span></span>
<span data-ttu-id="b6a1e-115">Указывает имя базы данных, для которой этот командлет задает рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="b6a1e-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="b6a1e-116">-RecommendedActionName</span></span>
<span data-ttu-id="b6a1e-117">Указывает имя рекомендуемого действия, для которого обновляется состояние.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-117">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="b6a1e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a1e-118">-ResourceGroupName</span></span>
<span data-ttu-id="b6a1e-119">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-119">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="b6a1e-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b6a1e-120">-ServerName</span></span>
<span data-ttu-id="b6a1e-121">Указывает имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-121">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="b6a1e-122">-State</span><span class="sxs-lookup"><span data-stu-id="b6a1e-122">-State</span></span>
<span data-ttu-id="b6a1e-123">Указывает новое значение, на которое этот командлет обновляет рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="b6a1e-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b6a1e-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6a1e-125">Службы</span><span class="sxs-lookup"><span data-stu-id="b6a1e-125">Active</span></span>
- <span data-ttu-id="b6a1e-126">Типа</span><span class="sxs-lookup"><span data-stu-id="b6a1e-126">Pending</span></span>
- <span data-ttu-id="b6a1e-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="b6a1e-127">PendingRevert</span></span>
- <span data-ttu-id="b6a1e-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="b6a1e-128">RevertCancelled</span></span>
- <span data-ttu-id="b6a1e-129">Учитываться</span><span class="sxs-lookup"><span data-stu-id="b6a1e-129">Ignored</span></span>
- <span data-ttu-id="b6a1e-130">Разрешившего</span><span class="sxs-lookup"><span data-stu-id="b6a1e-130">Resolved</span></span>

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

### <span data-ttu-id="b6a1e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6a1e-131">-Confirm</span></span>
<span data-ttu-id="b6a1e-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a1e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a1e-133">-WhatIf</span></span>
<span data-ttu-id="b6a1e-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a1e-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a1e-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a1e-136">-DefaultProfile</span></span>
<span data-ttu-id="b6a1e-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a1e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a1e-138">CommonParameters</span></span>
<span data-ttu-id="b6a1e-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6a1e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a1e-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a1e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a1e-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6a1e-141">INPUTS</span></span>

## <span data-ttu-id="b6a1e-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6a1e-142">OUTPUTS</span></span>

### <span data-ttu-id="b6a1e-143">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="b6a1e-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="b6a1e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6a1e-144">NOTES</span></span>
* <span data-ttu-id="b6a1e-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база_данных, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="b6a1e-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="b6a1e-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6a1e-146">RELATED LINKS</span></span>

[<span data-ttu-id="b6a1e-147">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b6a1e-147">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="b6a1e-148">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="b6a1e-148">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="b6a1e-149">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b6a1e-149">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="b6a1e-150">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b6a1e-150">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="b6a1e-151">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b6a1e-151">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="b6a1e-152">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b6a1e-152">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="b6a1e-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b6a1e-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="b6a1e-154">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b6a1e-154">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="b6a1e-155">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b6a1e-155">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="b6a1e-156">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b6a1e-156">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="b6a1e-157">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="b6a1e-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
