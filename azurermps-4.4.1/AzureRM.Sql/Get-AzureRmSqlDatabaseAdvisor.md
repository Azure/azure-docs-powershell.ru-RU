---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
ms.openlocfilehash: bc66e944a71cdd354bd102969ed2914c496bcfe8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568665"
---
# <span data-ttu-id="3323c-101">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="3323c-101">Get-AzureRmSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="3323c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3323c-102">SYNOPSIS</span></span>
<span data-ttu-id="3323c-103">Получает один или несколько консультантов для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3323c-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3323c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3323c-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3323c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3323c-105">DESCRIPTION</span></span>
<span data-ttu-id="3323c-106">Командлет **Get-AzureRmSqlDatabaseAdvisor** получает один или несколько советников по базам данных SQL Azure для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3323c-106">The **Get-AzureRmSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="3323c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3323c-107">EXAMPLES</span></span>

### <span data-ttu-id="3323c-108">Пример 1: список всех помощников для указанной базы данных</span><span class="sxs-lookup"><span data-stu-id="3323c-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
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

<span data-ttu-id="3323c-109">Эта команда возвращает список всех рекомендаций для базы данных с именем WIRunner, которая принадлежит серверу с именем Wi-Runner-Австралия-Восток.</span><span class="sxs-lookup"><span data-stu-id="3323c-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="3323c-110">Пример 2: получение одного помощника для указанной базы данных</span><span class="sxs-lookup"><span data-stu-id="3323c-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

<span data-ttu-id="3323c-111">Эта команда получает помощник с именем CreateIndex для базы данных с именем WIRunner.</span><span class="sxs-lookup"><span data-stu-id="3323c-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="3323c-112">Пример 3: список всех помощников с рекомендованными действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="3323c-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
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

<span data-ttu-id="3323c-113">Эта команда получает все рекомендации для базы данных с именем "WIRunner" и рекомендуемые действия, включенные в ответ.</span><span class="sxs-lookup"><span data-stu-id="3323c-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="3323c-114">Поскольку в команде используется параметр *ExpandRecommendedActions* , командлет получает Рекомендуемые действия с ответом.</span><span class="sxs-lookup"><span data-stu-id="3323c-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="3323c-115">Пример 4: получение одного помощника с рекомендованными действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="3323c-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="3323c-116">Эта команда получает помощник с именем CreateIndex из базы данных с именем WIRunner и рекомендованными действиями, включенными в ответ.</span><span class="sxs-lookup"><span data-stu-id="3323c-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="3323c-117">Поскольку в команде используется параметр *ExpandRecommendedActions* , командлет получает Рекомендуемые действия с ответом.</span><span class="sxs-lookup"><span data-stu-id="3323c-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

## <span data-ttu-id="3323c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3323c-118">PARAMETERS</span></span>

### <span data-ttu-id="3323c-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="3323c-119">-AdvisorName</span></span>
<span data-ttu-id="3323c-120">Указывает имя помощника, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3323c-120">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3323c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3323c-121">-DatabaseName</span></span>
<span data-ttu-id="3323c-122">Указывает имя базы данных, для которой этот командлет запрашивает помощника.</span><span class="sxs-lookup"><span data-stu-id="3323c-122">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="3323c-123">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="3323c-123">-ExpandRecommendedActions</span></span>
<span data-ttu-id="3323c-124">Указывает на то, что этот командлет получает Рекомендуемые действия с ответом.</span><span class="sxs-lookup"><span data-stu-id="3323c-124">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="3323c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3323c-125">-ResourceGroupName</span></span>
<span data-ttu-id="3323c-126">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="3323c-126">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="3323c-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3323c-127">-ServerName</span></span>
<span data-ttu-id="3323c-128">Указывает имя сервера, который содержит базу данных.</span><span class="sxs-lookup"><span data-stu-id="3323c-128">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="3323c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3323c-129">-DefaultProfile</span></span>
<span data-ttu-id="3323c-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3323c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3323c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3323c-131">CommonParameters</span></span>
<span data-ttu-id="3323c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3323c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3323c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3323c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3323c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3323c-134">INPUTS</span></span>

## <span data-ttu-id="3323c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3323c-135">OUTPUTS</span></span>

### <span data-ttu-id="3323c-136">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="3323c-136">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="3323c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="3323c-137">NOTES</span></span>
* <span data-ttu-id="3323c-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL, помощник</span><span class="sxs-lookup"><span data-stu-id="3323c-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="3323c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3323c-139">RELATED LINKS</span></span>

[<span data-ttu-id="3323c-140">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="3323c-140">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="3323c-141">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="3323c-141">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="3323c-142">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="3323c-142">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="3323c-143">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3323c-143">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="3323c-144">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3323c-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
