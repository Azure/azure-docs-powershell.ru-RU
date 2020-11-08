---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074255"
---
# <span data-ttu-id="c0afb-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="c0afb-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="c0afb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0afb-102">SYNOPSIS</span></span>
<span data-ttu-id="c0afb-103">Получает один или несколько консультантов для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c0afb-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="c0afb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0afb-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0afb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0afb-105">DESCRIPTION</span></span>
<span data-ttu-id="c0afb-106">Командлет **Get-AzSqlServerAdvisor** получает один или несколько консультантов Azure SQL Server для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c0afb-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="c0afb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0afb-107">EXAMPLES</span></span>

### <span data-ttu-id="c0afb-108">Пример 1: список всех помощников для сервера</span><span class="sxs-lookup"><span data-stu-id="c0afb-108">Example 1: List all the advisors for the server</span></span>
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

<span data-ttu-id="c0afb-109">Эта команда получает список всех помощников для сервера с именем Wi-Runner-Австралия-Восток, который принадлежит группе ресурсов с именем WIRunnersProd.</span><span class="sxs-lookup"><span data-stu-id="c0afb-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="c0afb-110">Пример 2: получение одного помощника для сервера</span><span class="sxs-lookup"><span data-stu-id="c0afb-110">Example 2: Get a single advisor for the server</span></span>
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

<span data-ttu-id="c0afb-111">Эта команда получает помощник с именем CreateIndex для сервера с именем Wi-Runner-Австралия-Восток.</span><span class="sxs-lookup"><span data-stu-id="c0afb-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="c0afb-112">Пример 3: список всех помощников с рекомендованными действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="c0afb-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="c0afb-113">Эта команда получает все рекомендации для сервера с именем Wi-Runner-Австралия-Восток.</span><span class="sxs-lookup"><span data-stu-id="c0afb-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="c0afb-114">Поскольку в команде используется параметр *ExpandRecommendedActions* , командлет получает Рекомендуемые действия, которые содержатся в ответе на эти рекомендации.</span><span class="sxs-lookup"><span data-stu-id="c0afb-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="c0afb-115">Пример 4: получение одного помощника с рекомендованными действиями, включенными в ответ</span><span class="sxs-lookup"><span data-stu-id="c0afb-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="c0afb-116">Эта команда получает советник с именем CreateIndex с сервера с именем Wi-Runner-Австралия-Восток и его рекомендованными действиями, включенными в ответ.</span><span class="sxs-lookup"><span data-stu-id="c0afb-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="c0afb-117">Пример 5: список всех помощников для сервера с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="c0afb-117">Example 5: List all the advisors for the server using filtering</span></span>
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

<span data-ttu-id="c0afb-118">Эта команда получает список всех рекомендаций для сервера с именем Wi-Runner-Австралия-Восток, который принадлежит к группе ресурсов с именем WIRunnersProd, которая начинается с буквы "d".</span><span class="sxs-lookup"><span data-stu-id="c0afb-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="c0afb-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0afb-119">PARAMETERS</span></span>

### <span data-ttu-id="c0afb-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="c0afb-120">-AdvisorName</span></span>
<span data-ttu-id="c0afb-121">Указывает имя помощника, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c0afb-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c0afb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0afb-122">-DefaultProfile</span></span>
<span data-ttu-id="c0afb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c0afb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0afb-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="c0afb-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="c0afb-125">Указывает на то, что командлет включает Рекомендуемые действия для помощников, включенных в ответ.</span><span class="sxs-lookup"><span data-stu-id="c0afb-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="c0afb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0afb-126">-ResourceGroupName</span></span>
<span data-ttu-id="c0afb-127">Указывает имя группы ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="c0afb-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="c0afb-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c0afb-128">-ServerName</span></span>
<span data-ttu-id="c0afb-129">Указывает имя сервера для помощника, который запрашивает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c0afb-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="c0afb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0afb-130">CommonParameters</span></span>
<span data-ttu-id="c0afb-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0afb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0afb-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0afb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0afb-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0afb-133">INPUTS</span></span>

### <span data-ttu-id="c0afb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c0afb-134">System.String</span></span>

### <span data-ttu-id="c0afb-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c0afb-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c0afb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0afb-136">OUTPUTS</span></span>

### <span data-ttu-id="c0afb-137">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="c0afb-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="c0afb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0afb-138">NOTES</span></span>
* <span data-ttu-id="c0afb-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, сервер</span><span class="sxs-lookup"><span data-stu-id="c0afb-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="c0afb-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0afb-140">RELATED LINKS</span></span>

[<span data-ttu-id="c0afb-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="c0afb-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="c0afb-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="c0afb-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="c0afb-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="c0afb-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="c0afb-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c0afb-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c0afb-145">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="c0afb-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

