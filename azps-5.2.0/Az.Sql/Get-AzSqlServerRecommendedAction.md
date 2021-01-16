---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BB513A53-48A0-4F8F-93F0-D3DFA2C3D523
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerRecommendedAction.md
ms.openlocfilehash: b27ded3d1ec4dbf011ca819ab55ddef0fb0df9c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412023"
---
# <span data-ttu-id="0b9ec-101">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0b9ec-101">Get-AzSqlServerRecommendedAction</span></span>

## <span data-ttu-id="0b9ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="0b9ec-103">Получает одно или несколько рекомендуемых действий для помощника по SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-103">Gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="0b9ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0b9ec-104">SYNTAX</span></span>

```
Get-AzSqlServerRecommendedAction [-RecommendedActionName <String>] -ServerName <String> -AdvisorName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b9ec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="0b9ec-106">Для помощника по azure SQL Server одно или несколько рекомендуемых действий с SQL Server **Get-AzSqlServerRecommendedAction.**</span><span class="sxs-lookup"><span data-stu-id="0b9ec-106">The **Get-AzSqlServerRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="0b9ec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0b9ec-107">EXAMPLES</span></span>

### <span data-ttu-id="0b9ec-108">Пример 1. Получить список всех рекомендуемых действий для определенного консультанта</span><span class="sxs-lookup"><span data-stu-id="0b9ec-108">Example 1: Get a list of  all recommended actions for a specific Advisor</span></span>
```
PS C:\>Get-AzSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
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
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM

ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
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
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="0b9ec-109">Эта команда получает список всех рекомендуемых действий помощника по SQL Server CreateIndex для сервера Wi-runner-australia-east.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-109">This command gets a list of all recommended actions of for the SQL Server Advisor named CreateIndex available for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="0b9ec-110">Пример 2. Получите одно рекомендуемое действие для помощника</span><span class="sxs-lookup"><span data-stu-id="0b9ec-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName 
IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
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

<span data-ttu-id="0b9ec-111">Эта команда получает рекомендуемое действие IR_ \[ test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893 от помощника \] CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-111">This command gets a recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="0b9ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b9ec-112">PARAMETERS</span></span>

### <span data-ttu-id="0b9ec-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="0b9ec-113">-AdvisorName</span></span>
<span data-ttu-id="0b9ec-114">Указывает имя помощника, для которого этот cmdlet запрашивает действия.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-114">Specifies the name of the advisor for which this cmdlet requests actions.</span></span>

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

### <span data-ttu-id="0b9ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b9ec-115">-DefaultProfile</span></span>
<span data-ttu-id="0b9ec-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0b9ec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b9ec-117">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="0b9ec-117">-RecommendedActionName</span></span>
<span data-ttu-id="0b9ec-118">Указывает имя рекомендуемого действия, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-118">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b9ec-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b9ec-120">Указывает имя группы ресурсов сервера, который содержит этот сервер.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-120">Specifies the name of the resource group of the server that contains this server.</span></span>

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

### <span data-ttu-id="0b9ec-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b9ec-121">-ServerName</span></span>
<span data-ttu-id="0b9ec-122">Имя сервера, на который принадлежит консультант.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-122">Specifies the name of the server the Advisor belongs to.</span></span>

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

### <span data-ttu-id="0b9ec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b9ec-123">CommonParameters</span></span>
<span data-ttu-id="0b9ec-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b9ec-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b9ec-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b9ec-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b9ec-126">INPUTS</span></span>

### <span data-ttu-id="0b9ec-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0b9ec-127">System.String</span></span>

## <span data-ttu-id="0b9ec-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0b9ec-128">OUTPUTS</span></span>

### <span data-ttu-id="0b9ec-129">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="0b9ec-129">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="0b9ec-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0b9ec-130">NOTES</span></span>
* <span data-ttu-id="0b9ec-131">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="0b9ec-131">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="0b9ec-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b9ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b9ec-133">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="0b9ec-133">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="0b9ec-134">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0b9ec-134">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="0b9ec-135">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0b9ec-135">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="0b9ec-136">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0b9ec-136">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="0b9ec-137">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="0b9ec-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
