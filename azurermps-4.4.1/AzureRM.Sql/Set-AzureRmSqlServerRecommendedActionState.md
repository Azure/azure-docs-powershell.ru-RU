---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: 4b000ef101b07bf882accb10b0256e0dbea513b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735033"
---
# <span data-ttu-id="66ccf-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66ccf-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="66ccf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="66ccf-103">Обновляет состояние рекомендуемого действия для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="66ccf-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66ccf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66ccf-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66ccf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66ccf-105">DESCRIPTION</span></span>
<span data-ttu-id="66ccf-106">Состояние обновления командлета **Set-AzureRmSqlServerRecommendedActionState** , рекомендованное действием Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="66ccf-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="66ccf-107">Этот командлет применяется, Возвращает или сбрасывает рекомендованное действие на основе нового состояния.</span><span class="sxs-lookup"><span data-stu-id="66ccf-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="66ccf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66ccf-108">EXAMPLES</span></span>

### <span data-ttu-id="66ccf-109">Example1: обновление состояния указанного рекомендуемого действия на ожидание</span><span class="sxs-lookup"><span data-stu-id="66ccf-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="66ccf-110">Обновляет состояние рекомендуемого для сервера действия с именем "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" на "ожидание"</span><span class="sxs-lookup"><span data-stu-id="66ccf-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="66ccf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66ccf-111">PARAMETERS</span></span>

### <span data-ttu-id="66ccf-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="66ccf-112">-AdvisorName</span></span>
<span data-ttu-id="66ccf-113">Указывает имя помощника, содержащего рекомендованное действие.</span><span class="sxs-lookup"><span data-stu-id="66ccf-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="66ccf-114">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="66ccf-114">-RecommendedActionName</span></span>
<span data-ttu-id="66ccf-115">Указывает имя рекомендуемого действия, для которого этот командлет обновляет состояние.</span><span class="sxs-lookup"><span data-stu-id="66ccf-115">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="66ccf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ccf-116">-ResourceGroupName</span></span>
<span data-ttu-id="66ccf-117">Указывает имя группы ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="66ccf-117">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="66ccf-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="66ccf-118">-ServerName</span></span>
<span data-ttu-id="66ccf-119">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="66ccf-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="66ccf-120">-State</span><span class="sxs-lookup"><span data-stu-id="66ccf-120">-State</span></span>
<span data-ttu-id="66ccf-121">Указывает новое значение, на которое этот командлет обновляет рекомендуемое состояние действия.</span><span class="sxs-lookup"><span data-stu-id="66ccf-121">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="66ccf-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="66ccf-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66ccf-123">Службы</span><span class="sxs-lookup"><span data-stu-id="66ccf-123">Active</span></span>
- <span data-ttu-id="66ccf-124">Типа</span><span class="sxs-lookup"><span data-stu-id="66ccf-124">Pending</span></span>
- <span data-ttu-id="66ccf-125">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="66ccf-125">PendingRevert</span></span>
- <span data-ttu-id="66ccf-126">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="66ccf-126">RevertCancelled</span></span>
- <span data-ttu-id="66ccf-127">Учитываться</span><span class="sxs-lookup"><span data-stu-id="66ccf-127">Ignored</span></span>
- <span data-ttu-id="66ccf-128">Разрешившего</span><span class="sxs-lookup"><span data-stu-id="66ccf-128">Resolved</span></span>

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

### <span data-ttu-id="66ccf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66ccf-129">-Confirm</span></span>
<span data-ttu-id="66ccf-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66ccf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ccf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ccf-131">-WhatIf</span></span>
<span data-ttu-id="66ccf-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="66ccf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ccf-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="66ccf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ccf-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ccf-134">-DefaultProfile</span></span>
<span data-ttu-id="66ccf-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66ccf-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66ccf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ccf-136">CommonParameters</span></span>
<span data-ttu-id="66ccf-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66ccf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ccf-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ccf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ccf-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66ccf-139">INPUTS</span></span>

## <span data-ttu-id="66ccf-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66ccf-140">OUTPUTS</span></span>

### <span data-ttu-id="66ccf-141">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="66ccf-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="66ccf-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="66ccf-142">NOTES</span></span>
* <span data-ttu-id="66ccf-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, сервер, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="66ccf-143">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="66ccf-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66ccf-144">RELATED LINKS</span></span>

[<span data-ttu-id="66ccf-145">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="66ccf-145">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="66ccf-146">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="66ccf-146">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="66ccf-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66ccf-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="66ccf-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66ccf-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="66ccf-149">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="66ccf-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
