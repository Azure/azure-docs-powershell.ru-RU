---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3FC9E586-3962-437E-B89F-BB4EA1FBF403
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendedAction.md
ms.openlocfilehash: 1b7f309aca65683bc9a15784f07ec2fbda4c66c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562572"
---
# <span data-ttu-id="3a187-101">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="3a187-101">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>

## <span data-ttu-id="3a187-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a187-102">SYNOPSIS</span></span>
<span data-ttu-id="3a187-103">Получает одно или несколько рекомендованных действий для советника по пулам эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3a187-103">Gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a187-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a187-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a187-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a187-105">DESCRIPTION</span></span>
<span data-ttu-id="3a187-106">Командлет **Get-AzureRmSqlElasticPoolRecommendedAction** получает одно или несколько рекомендованных действий для помощника по пулам эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3a187-106">The **Get-AzureRmSqlElasticPoolRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="3a187-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a187-107">EXAMPLES</span></span>

### <span data-ttu-id="3a187-108">Пример 1: список всех рекомендуемых действий для помощника</span><span class="sxs-lookup"><span data-stu-id="3a187-108">Example 1: List all recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

ElasticPoolName            : WIRunnerPool
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

ElasticPoolName            : WIRunnerPool
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

<span data-ttu-id="3a187-109">Эта команда возвращает список всех рекомендованных действий помощника с именем CreateIndex, доступных для пула эластичных БД с именем WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="3a187-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="3a187-110">Пример 2: получение одного рекомендуемого действия для помощника</span><span class="sxs-lookup"><span data-stu-id="3a187-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="3a187-111">Эта команда получает рекомендованное действие с именем IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 из помощника с именем CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="3a187-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="3a187-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a187-112">PARAMETERS</span></span>

### <span data-ttu-id="3a187-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="3a187-113">-AdvisorName</span></span>
<span data-ttu-id="3a187-114">Указывает имя помощника, для которого этот командлет запрашивает Рекомендуемые действия.</span><span class="sxs-lookup"><span data-stu-id="3a187-114">Specifies the name of the advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="3a187-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a187-115">-DefaultProfile</span></span>
<span data-ttu-id="3a187-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3a187-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a187-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3a187-117">-ElasticPoolName</span></span>
<span data-ttu-id="3a187-118">Указывает имя эластичного пула, для которого этот командлет запрашивает Рекомендуемые действия.</span><span class="sxs-lookup"><span data-stu-id="3a187-118">Specifies the name of the elastic pool for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="3a187-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="3a187-119">-RecommendedActionName</span></span>
<span data-ttu-id="3a187-120">Указывает имя рекомендуемого действия, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3a187-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3a187-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a187-121">-ResourceGroupName</span></span>
<span data-ttu-id="3a187-122">Указывает имя группы ресурсов сервера, содержащего этот эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="3a187-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="3a187-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3a187-123">-ServerName</span></span>
<span data-ttu-id="3a187-124">Указывает имя сервера, на котором находится пул эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="3a187-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="3a187-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a187-125">CommonParameters</span></span>
<span data-ttu-id="3a187-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a187-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a187-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a187-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a187-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a187-128">INPUTS</span></span>

### <span data-ttu-id="3a187-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3a187-129">System.String</span></span>

## <span data-ttu-id="3a187-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a187-130">OUTPUTS</span></span>

### <span data-ttu-id="3a187-131">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="3a187-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="3a187-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a187-132">NOTES</span></span>
* <span data-ttu-id="3a187-133">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="3a187-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="3a187-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a187-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a187-135">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="3a187-135">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="3a187-136">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="3a187-136">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="3a187-137">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="3a187-137">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="3a187-138">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="3a187-138">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="3a187-139">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3a187-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
