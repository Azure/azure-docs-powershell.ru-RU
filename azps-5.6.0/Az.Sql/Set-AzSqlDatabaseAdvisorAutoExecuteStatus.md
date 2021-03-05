---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 214fe4c32ed49433aa57752508604d0179334401
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995014"
---
# <span data-ttu-id="81e4e-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="81e4e-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="81e4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="81e4e-103">Изменяет состояние автоматического выполнения помощника по SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="81e4e-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="81e4e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="81e4e-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81e4e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81e4e-105">DESCRIPTION</span></span>
<span data-ttu-id="81e4e-106">Cmdlet **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** изменяет свойство автоматического выполнения для помощника по SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="81e4e-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="81e4e-107">В настоящее время этот cmdlet поддерживает значения Enabled, Disabled и Default.</span><span class="sxs-lookup"><span data-stu-id="81e4e-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="81e4e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="81e4e-108">EXAMPLES</span></span>

### <span data-ttu-id="81e4e-109">Пример 1. Включить автоматическое выполнение для помощника</span><span class="sxs-lookup"><span data-stu-id="81e4e-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="81e4e-110">Эта команда изменяет состояние автоматического выполнения помощника CreateIndex на Enabled.</span><span class="sxs-lookup"><span data-stu-id="81e4e-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="81e4e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81e4e-111">PARAMETERS</span></span>

### <span data-ttu-id="81e4e-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="81e4e-112">-AdvisorName</span></span>
<span data-ttu-id="81e4e-113">Указывает имя консультанта, состояние которого изменяется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e4e-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="81e4e-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="81e4e-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="81e4e-115">Указывает значение для состояния.</span><span class="sxs-lookup"><span data-stu-id="81e4e-115">Specifies the value for the status.</span></span>
<span data-ttu-id="81e4e-116">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="81e4e-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="81e4e-117">Включено</span><span class="sxs-lookup"><span data-stu-id="81e4e-117">Enabled</span></span> 
- <span data-ttu-id="81e4e-118">Отключено</span><span class="sxs-lookup"><span data-stu-id="81e4e-118">Disabled</span></span> 
- <span data-ttu-id="81e4e-119">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="81e4e-119">Default</span></span>

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

### <span data-ttu-id="81e4e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81e4e-120">-DatabaseName</span></span>
<span data-ttu-id="81e4e-121">Указывает имя базы данных, для которой этот cmdlet изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="81e4e-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="81e4e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e4e-122">-DefaultProfile</span></span>
<span data-ttu-id="81e4e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="81e4e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81e4e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e4e-124">-ResourceGroupName</span></span>
<span data-ttu-id="81e4e-125">Указывает имя группы ресурсов сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="81e4e-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="81e4e-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81e4e-126">-ServerName</span></span>
<span data-ttu-id="81e4e-127">Имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="81e4e-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="81e4e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81e4e-128">-Confirm</span></span>
<span data-ttu-id="81e4e-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e4e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e4e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e4e-130">-WhatIf</span></span>
<span data-ttu-id="81e4e-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e4e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81e4e-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="81e4e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e4e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e4e-133">CommonParameters</span></span>
<span data-ttu-id="81e4e-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e4e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e4e-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81e4e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e4e-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81e4e-136">INPUTS</span></span>

### <span data-ttu-id="81e4e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="81e4e-137">System.String</span></span>

### <span data-ttu-id="81e4e-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="81e4e-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="81e4e-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81e4e-139">OUTPUTS</span></span>

### <span data-ttu-id="81e4e-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="81e4e-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="81e4e-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="81e4e-141">NOTES</span></span>

## <span data-ttu-id="81e4e-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81e4e-142">RELATED LINKS</span></span>

[<span data-ttu-id="81e4e-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="81e4e-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="81e4e-144">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="81e4e-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

