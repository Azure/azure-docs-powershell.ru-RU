---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 05bde2ee8a5bbcae941203115c49ff6b9fbc6bae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231833"
---
# <span data-ttu-id="3f305-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="3f305-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="3f305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f305-102">SYNOPSIS</span></span>
<span data-ttu-id="3f305-103">Получает одного или несколько консультантов для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3f305-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="3f305-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f305-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f305-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f305-105">DESCRIPTION</span></span>
<span data-ttu-id="3f305-106">Для базы данных Azure SQL Azure вы получаете один или несколько помощников по базе данных Azure SQL **Get-AzSqlDataBase.**</span><span class="sxs-lookup"><span data-stu-id="3f305-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="3f305-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f305-107">EXAMPLES</span></span>

### <span data-ttu-id="3f305-108">Пример 1. Список всех консультантов для указанной базы данных</span><span class="sxs-lookup"><span data-stu-id="3f305-108">Example 1: List all the advisors for the specified database</span></span>
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

<span data-ttu-id="3f305-109">Эта команда возвращает список всех консультантов для базы данных WiRunner, которая принадлежит к серверу Wi-run-australia-east.</span><span class="sxs-lookup"><span data-stu-id="3f305-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="3f305-110">Пример 2. Получить одного помощника для указанной базы данных</span><span class="sxs-lookup"><span data-stu-id="3f305-110">Example 2: Get a single advisor for the specified database</span></span>
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

<span data-ttu-id="3f305-111">Эта команда получает помощник CreateIndex для базы данных с именем WIRunner.</span><span class="sxs-lookup"><span data-stu-id="3f305-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="3f305-112">Пример 3. Укаймь всех помощников, включив в ответ рекомендуемые действия</span><span class="sxs-lookup"><span data-stu-id="3f305-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="3f305-113">Эта команда получает всех консультантов для базы данных WiRunner с рекомендуемыми действиями, включенными в ответ.</span><span class="sxs-lookup"><span data-stu-id="3f305-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="3f305-114">Так как для команды используется параметр *ExpandRecommendedActions,* командлет получает рекомендуемые действия вместе с ответом.</span><span class="sxs-lookup"><span data-stu-id="3f305-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="3f305-115">Пример 4. Получить одного консультанта с рекомендуемыми действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="3f305-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="3f305-116">Эта команда получает помощник CreateIndex из базы данных WiRunner со своими рекомендуемами действиями, включенными в ответ.</span><span class="sxs-lookup"><span data-stu-id="3f305-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="3f305-117">Так как для команды используется параметр *ExpandRecommendedActions,* командлет получает рекомендуемые действия вместе с ответом.</span><span class="sxs-lookup"><span data-stu-id="3f305-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="3f305-118">Пример 5. Список всех помощников для указанной базы данных с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="3f305-118">Example 5: List all the advisors for the specified database using filtering</span></span>
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

<span data-ttu-id="3f305-119">Эта команда возвращает список всех консультантов для базы данных WiRunner, которая принадлежит к серверу Wi-run-australia-east и начинается с буквы "d".</span><span class="sxs-lookup"><span data-stu-id="3f305-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="3f305-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f305-120">PARAMETERS</span></span>

### <span data-ttu-id="3f305-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="3f305-121">-AdvisorName</span></span>
<span data-ttu-id="3f305-122">Указывает имя консультанта, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f305-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3f305-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f305-123">-DatabaseName</span></span>
<span data-ttu-id="3f305-124">Имя базы данных, для которой этот cmdlet запрашивает помощника.</span><span class="sxs-lookup"><span data-stu-id="3f305-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="3f305-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f305-125">-DefaultProfile</span></span>
<span data-ttu-id="3f305-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3f305-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f305-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="3f305-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="3f305-128">Указывает на то, что этот cmdlet получает рекомендуемые действия вместе с ответом.</span><span class="sxs-lookup"><span data-stu-id="3f305-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="3f305-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f305-129">-ResourceGroupName</span></span>
<span data-ttu-id="3f305-130">Указывает имя группы ресурсов сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="3f305-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="3f305-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3f305-131">-ServerName</span></span>
<span data-ttu-id="3f305-132">Указывает имя сервера, который содержит базу данных.</span><span class="sxs-lookup"><span data-stu-id="3f305-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="3f305-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f305-133">CommonParameters</span></span>
<span data-ttu-id="3f305-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f305-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f305-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f305-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f305-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f305-136">INPUTS</span></span>

### <span data-ttu-id="3f305-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3f305-137">System.String</span></span>

### <span data-ttu-id="3f305-138">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3f305-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3f305-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f305-139">OUTPUTS</span></span>

### <span data-ttu-id="3f305-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="3f305-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="3f305-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f305-141">NOTES</span></span>
* <span data-ttu-id="3f305-142">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="3f305-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="3f305-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f305-143">RELATED LINKS</span></span>

[<span data-ttu-id="3f305-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="3f305-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="3f305-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="3f305-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="3f305-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="3f305-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="3f305-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3f305-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="3f305-148">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="3f305-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
