---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404524"
---
# <span data-ttu-id="99bab-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="99bab-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="99bab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99bab-102">SYNOPSIS</span></span>
<span data-ttu-id="99bab-103">Получает одного или несколько консультантов для службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="99bab-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="99bab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="99bab-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99bab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99bab-105">DESCRIPTION</span></span>
<span data-ttu-id="99bab-106">Чтобы **получить одного** или несколько помощников по SQL Server Azure для Azure SQL Server, можно получить один или несколько SQL Server.</span><span class="sxs-lookup"><span data-stu-id="99bab-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="99bab-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="99bab-107">EXAMPLES</span></span>

### <span data-ttu-id="99bab-108">Пример 1. Список всех помощников для сервера</span><span class="sxs-lookup"><span data-stu-id="99bab-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

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

<span data-ttu-id="99bab-109">Эта команда получает список всех консультантов для сервера Wi-runner-australia-east, который принадлежит к группе ресурсов WIRunnersProd.</span><span class="sxs-lookup"><span data-stu-id="99bab-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="99bab-110">Пример 2. Получить одного помощника для сервера</span><span class="sxs-lookup"><span data-stu-id="99bab-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="99bab-111">Эта команда получает помощник CreateIndex для сервера Wi-runner-australia-east.</span><span class="sxs-lookup"><span data-stu-id="99bab-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="99bab-112">Пример 3. Укаймь всех помощников, включив в ответ рекомендуемые действия</span><span class="sxs-lookup"><span data-stu-id="99bab-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
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

<span data-ttu-id="99bab-113">Эта команда получает всех помощников для сервера Wi-runner-australia-east.</span><span class="sxs-lookup"><span data-stu-id="99bab-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="99bab-114">Так как команда использует параметр *ExpandRecommendedActions,* командлет получает рекомендации помощников, включенные в ответ.</span><span class="sxs-lookup"><span data-stu-id="99bab-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="99bab-115">Пример 4. Получить одного консультанта с рекомендуемыми действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="99bab-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="99bab-116">Эта команда получает помощник CreateIndex с сервера Wi-runner-australia-east с рекомендуемыми действиями, включенными в ответ.</span><span class="sxs-lookup"><span data-stu-id="99bab-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="99bab-117">Пример 5. Список всех помощников для сервера с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="99bab-117">Example 5: List all the advisors for the server using filtering</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName d*
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

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

<span data-ttu-id="99bab-118">Эта команда получает список всех консультантов для сервера Wi-run-australia-east, который принадлежит к группе ресурсов WIRunnersProd, которые начинаются с буквы "d".</span><span class="sxs-lookup"><span data-stu-id="99bab-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="99bab-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99bab-119">PARAMETERS</span></span>

### <span data-ttu-id="99bab-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="99bab-120">-AdvisorName</span></span>
<span data-ttu-id="99bab-121">Указывает имя консультанта, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99bab-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="99bab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99bab-122">-DefaultProfile</span></span>
<span data-ttu-id="99bab-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="99bab-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99bab-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="99bab-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="99bab-125">Указывает на то, что в этот список включены рекомендуемые действия помощников, включенных в ответ.</span><span class="sxs-lookup"><span data-stu-id="99bab-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="99bab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99bab-126">-ResourceGroupName</span></span>
<span data-ttu-id="99bab-127">Указывает имя группы ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="99bab-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="99bab-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99bab-128">-ServerName</span></span>
<span data-ttu-id="99bab-129">Имя сервера, запрашиваемого этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99bab-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="99bab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99bab-130">CommonParameters</span></span>
<span data-ttu-id="99bab-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99bab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99bab-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99bab-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99bab-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99bab-133">INPUTS</span></span>

### <span data-ttu-id="99bab-134">System.String</span><span class="sxs-lookup"><span data-stu-id="99bab-134">System.String</span></span>

### <span data-ttu-id="99bab-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99bab-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99bab-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99bab-136">OUTPUTS</span></span>

### <span data-ttu-id="99bab-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="99bab-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="99bab-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="99bab-138">NOTES</span></span>
* <span data-ttu-id="99bab-139">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="99bab-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="99bab-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99bab-140">RELATED LINKS</span></span>

[<span data-ttu-id="99bab-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="99bab-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="99bab-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="99bab-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="99bab-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="99bab-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="99bab-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="99bab-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="99bab-145">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="99bab-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

