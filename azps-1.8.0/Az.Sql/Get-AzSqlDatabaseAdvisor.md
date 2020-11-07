---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 514a10788c28edacbca53dc8135c8d071aaff56b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729047"
---
# <span data-ttu-id="e1c43-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="e1c43-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="e1c43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1c43-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c43-103">Получает один или несколько консультантов для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c43-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="e1c43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1c43-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1c43-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1c43-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c43-106">Командлет **Get-AzSqlDatabaseAdvisor** получает один или несколько советников по базам данных SQL Azure для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c43-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="e1c43-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1c43-107">EXAMPLES</span></span>

### <span data-ttu-id="e1c43-108">Пример 1: список всех помощников для указанной базы данных</span><span class="sxs-lookup"><span data-stu-id="e1c43-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
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

<span data-ttu-id="e1c43-109">Эта команда возвращает список всех рекомендаций для базы данных с именем WIRunner, которая принадлежит серверу с именем Wi-Runner-Австралия-Восток.</span><span class="sxs-lookup"><span data-stu-id="e1c43-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="e1c43-110">Пример 2: получение одного помощника для указанной базы данных</span><span class="sxs-lookup"><span data-stu-id="e1c43-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
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

<span data-ttu-id="e1c43-111">Эта команда получает помощник с именем CreateIndex для базы данных с именем WIRunner.</span><span class="sxs-lookup"><span data-stu-id="e1c43-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="e1c43-112">Пример 3: список всех помощников с рекомендованными действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="e1c43-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
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

DatabaseName                   : WIRunner
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

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
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

<span data-ttu-id="e1c43-113">Эта команда получает все рекомендации для базы данных с именем "WIRunner" и рекомендуемые действия, включенные в ответ.</span><span class="sxs-lookup"><span data-stu-id="e1c43-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="e1c43-114">Поскольку в команде используется параметр *ExpandRecommendedActions* , командлет получает Рекомендуемые действия с ответом.</span><span class="sxs-lookup"><span data-stu-id="e1c43-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="e1c43-115">Пример 4: получение одного помощника с рекомендованными действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="e1c43-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
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

<span data-ttu-id="e1c43-116">Эта команда получает помощник с именем CreateIndex из базы данных с именем WIRunner и рекомендованными действиями, включенными в ответ.</span><span class="sxs-lookup"><span data-stu-id="e1c43-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="e1c43-117">Поскольку в команде используется параметр *ExpandRecommendedActions* , командлет получает Рекомендуемые действия с ответом.</span><span class="sxs-lookup"><span data-stu-id="e1c43-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="e1c43-118">Пример 5: список всех помощников для указанной базы данных с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="e1c43-118">Example 5: List all the advisors for the specified database using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName d*
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
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

<span data-ttu-id="e1c43-119">Эта команда возвращает список всех рекомендаций для базы данных с именем WIRunner, которая принадлежит серверу с именем Wi-Runner-Австралия-Восток и начинается с буквы "г".</span><span class="sxs-lookup"><span data-stu-id="e1c43-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="e1c43-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1c43-120">PARAMETERS</span></span>

### <span data-ttu-id="e1c43-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="e1c43-121">-AdvisorName</span></span>
<span data-ttu-id="e1c43-122">Указывает имя помощника, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e1c43-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e1c43-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1c43-123">-DatabaseName</span></span>
<span data-ttu-id="e1c43-124">Указывает имя базы данных, для которой этот командлет запрашивает помощника.</span><span class="sxs-lookup"><span data-stu-id="e1c43-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="e1c43-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c43-125">-DefaultProfile</span></span>
<span data-ttu-id="e1c43-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e1c43-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1c43-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="e1c43-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="e1c43-128">Указывает на то, что этот командлет получает Рекомендуемые действия с ответом.</span><span class="sxs-lookup"><span data-stu-id="e1c43-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="e1c43-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1c43-129">-ResourceGroupName</span></span>
<span data-ttu-id="e1c43-130">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="e1c43-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="e1c43-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e1c43-131">-ServerName</span></span>
<span data-ttu-id="e1c43-132">Указывает имя сервера, который содержит базу данных.</span><span class="sxs-lookup"><span data-stu-id="e1c43-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="e1c43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c43-133">CommonParameters</span></span>
<span data-ttu-id="e1c43-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1c43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c43-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1c43-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c43-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1c43-136">INPUTS</span></span>

### <span data-ttu-id="e1c43-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e1c43-137">System.String</span></span>

### <span data-ttu-id="e1c43-138">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e1c43-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1c43-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1c43-139">OUTPUTS</span></span>

### <span data-ttu-id="e1c43-140">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="e1c43-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="e1c43-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1c43-141">NOTES</span></span>
* <span data-ttu-id="e1c43-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL, помощник</span><span class="sxs-lookup"><span data-stu-id="e1c43-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="e1c43-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1c43-143">RELATED LINKS</span></span>

[<span data-ttu-id="e1c43-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="e1c43-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="e1c43-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="e1c43-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="e1c43-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e1c43-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="e1c43-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e1c43-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="e1c43-148">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="e1c43-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
