---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 1d6348c5ede63dee1f76059277c8f7d142a2c327
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417359"
---
# <span data-ttu-id="f021d-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f021d-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f021d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f021d-102">SYNOPSIS</span></span>
<span data-ttu-id="f021d-103">Изменяет состояние автоматического выполнения помощника по SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f021d-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="f021d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f021d-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f021d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f021d-105">DESCRIPTION</span></span>
<span data-ttu-id="f021d-106">Cmdlet **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** изменяет свойство автоматического выполнения для помощника по базе данных Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f021d-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="f021d-107">В настоящее время этот cmdlet поддерживает значения Enabled, Disabled и Default.</span><span class="sxs-lookup"><span data-stu-id="f021d-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="f021d-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f021d-108">EXAMPLES</span></span>

### <span data-ttu-id="f021d-109">Пример 1. Включить автоматическое выполнение для помощника</span><span class="sxs-lookup"><span data-stu-id="f021d-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="f021d-110">Эта команда изменяет состояние автоматического выполнения помощника CreateIndex на Enabled.</span><span class="sxs-lookup"><span data-stu-id="f021d-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="f021d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f021d-111">PARAMETERS</span></span>

### <span data-ttu-id="f021d-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="f021d-112">-AdvisorName</span></span>
<span data-ttu-id="f021d-113">Указывает имя консультанта, состояние которого изменяется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f021d-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="f021d-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f021d-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="f021d-115">Указывает значение для состояния.</span><span class="sxs-lookup"><span data-stu-id="f021d-115">Specifies the value for the status.</span></span>
<span data-ttu-id="f021d-116">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="f021d-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f021d-117">Включено</span><span class="sxs-lookup"><span data-stu-id="f021d-117">Enabled</span></span> 
- <span data-ttu-id="f021d-118">Отключено</span><span class="sxs-lookup"><span data-stu-id="f021d-118">Disabled</span></span> 
- <span data-ttu-id="f021d-119">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="f021d-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f021d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f021d-120">-DatabaseName</span></span>
<span data-ttu-id="f021d-121">Указывает имя базы данных, для которой этот cmdlet изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="f021d-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="f021d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f021d-122">-DefaultProfile</span></span>
<span data-ttu-id="f021d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f021d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f021d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f021d-124">-ResourceGroupName</span></span>
<span data-ttu-id="f021d-125">Указывает имя группы ресурсов сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="f021d-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="f021d-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f021d-126">-ServerName</span></span>
<span data-ttu-id="f021d-127">Имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="f021d-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="f021d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f021d-128">-Confirm</span></span>
<span data-ttu-id="f021d-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f021d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f021d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f021d-130">-WhatIf</span></span>
<span data-ttu-id="f021d-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f021d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f021d-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f021d-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f021d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f021d-133">CommonParameters</span></span>
<span data-ttu-id="f021d-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f021d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f021d-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f021d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f021d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f021d-136">INPUTS</span></span>

### <span data-ttu-id="f021d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f021d-137">System.String</span></span>

### <span data-ttu-id="f021d-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f021d-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f021d-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f021d-139">OUTPUTS</span></span>

### <span data-ttu-id="f021d-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="f021d-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="f021d-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f021d-141">NOTES</span></span>

## <span data-ttu-id="f021d-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f021d-142">RELATED LINKS</span></span>

[<span data-ttu-id="f021d-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="f021d-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="f021d-144">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="f021d-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

