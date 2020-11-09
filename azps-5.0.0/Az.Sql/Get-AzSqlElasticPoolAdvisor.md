---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 3032824d51e7892c21830decbdb1c92d03d7a2e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312167"
---
# <span data-ttu-id="e2028-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="e2028-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="e2028-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2028-102">SYNOPSIS</span></span>
<span data-ttu-id="e2028-103">Получает один или несколько консультантов для пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e2028-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="e2028-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2028-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2028-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2028-105">DESCRIPTION</span></span>
<span data-ttu-id="e2028-106">Командлет **Get-AzSqlElasticPoolAdvisor** получает один или несколько советников пула эластичных БД Azure SQL для пула эластичных БД Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e2028-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="e2028-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2028-107">EXAMPLES</span></span>

### <span data-ttu-id="e2028-108">Пример 1: список всех помощников для указанного эластичного пула</span><span class="sxs-lookup"><span data-stu-id="e2028-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="e2028-109">Команда возвращает список всех помощников для пула эластичных БД с именем WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="e2028-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="e2028-110">Пример 2: получение одного помощника для указанного эластичного пула</span><span class="sxs-lookup"><span data-stu-id="e2028-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="e2028-111">Эта команда получает помощник с именем CreateIndex для пула эластичных БД с именем WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="e2028-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="e2028-112">Пример 3: список всех помощников с рекомендованными действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="e2028-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="e2028-113">Эта команда получает все рекомендации для пула эластичных БД с рекомендованными действиями, включенными в ответ.</span><span class="sxs-lookup"><span data-stu-id="e2028-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="e2028-114">Пример 4: получение одного помощника с рекомендованными действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="e2028-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="e2028-115">Эта команда получает советник с именем CreateIndex с сервера с именем Wi-Runner-Австралия-Восток и его рекомендованными действиями, включенными в ответ.</span><span class="sxs-lookup"><span data-stu-id="e2028-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="e2028-116">Пример 5: список всех помощников для указанного эластичного пула с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="e2028-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName d*
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="e2028-117">Команда возвращает список всех рекомендаций для пула эластичных БД с именем WIRunnerPool, который начинается с буквы "d".</span><span class="sxs-lookup"><span data-stu-id="e2028-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="e2028-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2028-118">PARAMETERS</span></span>

### <span data-ttu-id="e2028-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="e2028-119">-AdvisorName</span></span>
<span data-ttu-id="e2028-120">Указывает имя помощника, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e2028-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e2028-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2028-121">-DefaultProfile</span></span>
<span data-ttu-id="e2028-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e2028-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2028-123">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e2028-123">-ElasticPoolName</span></span>
<span data-ttu-id="e2028-124">Указывает имя эластичного пула, для которого этот командлет запрашивает помощника.</span><span class="sxs-lookup"><span data-stu-id="e2028-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="e2028-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="e2028-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="e2028-126">Указывает на то, что командлет включает Рекомендуемые действия помощника в ответе.</span><span class="sxs-lookup"><span data-stu-id="e2028-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2028-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2028-127">-ResourceGroupName</span></span>
<span data-ttu-id="e2028-128">Указывает имя группы ресурсов сервера, содержащего этот эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="e2028-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="e2028-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e2028-129">-ServerName</span></span>
<span data-ttu-id="e2028-130">Указывает имя сервера, на котором находится пул эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="e2028-130">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="e2028-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2028-131">CommonParameters</span></span>
<span data-ttu-id="e2028-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2028-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2028-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2028-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2028-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2028-134">INPUTS</span></span>

### <span data-ttu-id="e2028-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e2028-135">System.String</span></span>

### <span data-ttu-id="e2028-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e2028-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e2028-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2028-137">OUTPUTS</span></span>

### <span data-ttu-id="e2028-138">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="e2028-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="e2028-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2028-139">NOTES</span></span>
* <span data-ttu-id="e2028-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="e2028-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="e2028-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2028-141">RELATED LINKS</span></span>

[<span data-ttu-id="e2028-142">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="e2028-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="e2028-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="e2028-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="e2028-144">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e2028-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="e2028-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e2028-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="e2028-146">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="e2028-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
