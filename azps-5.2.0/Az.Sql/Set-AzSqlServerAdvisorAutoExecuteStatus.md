---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 02a4348511afabe7f398eafeb6d0849525f0abac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411631"
---
# <span data-ttu-id="64bc8-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="64bc8-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="64bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="64bc8-103">Обновляет состояние автоматического выполнения помощника azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="64bc8-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="64bc8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64bc8-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64bc8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="64bc8-106">Cmdlet **Set-AzSqlServerAdvisorAutoExecuteStatus** задает свойство автоматического выполнения для помощника azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="64bc8-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="64bc8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64bc8-107">EXAMPLES</span></span>

### <span data-ttu-id="64bc8-108">Пример 1. Включить автоматическое выполнение для помощника</span><span class="sxs-lookup"><span data-stu-id="64bc8-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="64bc8-109">Эта команда позволяет автоматически выполнять состояние помощника CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="64bc8-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="64bc8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64bc8-110">PARAMETERS</span></span>

### <span data-ttu-id="64bc8-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="64bc8-111">-AdvisorName</span></span>
<span data-ttu-id="64bc8-112">Указывает имя помощника, для которого этот cmdlet обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="64bc8-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="64bc8-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="64bc8-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="64bc8-114">Определяет значение, для которого этот cmdlet обновляет состояние автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="64bc8-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="64bc8-115">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="64bc8-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64bc8-116">Включено</span><span class="sxs-lookup"><span data-stu-id="64bc8-116">Enabled</span></span>
- <span data-ttu-id="64bc8-117">Отключено</span><span class="sxs-lookup"><span data-stu-id="64bc8-117">Disabled</span></span>
- <span data-ttu-id="64bc8-118">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="64bc8-118">Default</span></span>

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

### <span data-ttu-id="64bc8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bc8-119">-DefaultProfile</span></span>
<span data-ttu-id="64bc8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="64bc8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64bc8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64bc8-121">-ResourceGroupName</span></span>
<span data-ttu-id="64bc8-122">Указывает имя группы ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="64bc8-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="64bc8-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="64bc8-123">-ServerName</span></span>
<span data-ttu-id="64bc8-124">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="64bc8-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="64bc8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64bc8-125">-Confirm</span></span>
<span data-ttu-id="64bc8-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64bc8-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bc8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64bc8-127">-WhatIf</span></span>
<span data-ttu-id="64bc8-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64bc8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64bc8-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="64bc8-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bc8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bc8-130">CommonParameters</span></span>
<span data-ttu-id="64bc8-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bc8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bc8-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64bc8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bc8-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64bc8-133">INPUTS</span></span>

### <span data-ttu-id="64bc8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="64bc8-134">System.String</span></span>

### <span data-ttu-id="64bc8-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="64bc8-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="64bc8-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64bc8-136">OUTPUTS</span></span>

### <span data-ttu-id="64bc8-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="64bc8-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="64bc8-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64bc8-138">NOTES</span></span>
* <span data-ttu-id="64bc8-139">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="64bc8-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="64bc8-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64bc8-140">RELATED LINKS</span></span>

[<span data-ttu-id="64bc8-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="64bc8-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="64bc8-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="64bc8-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
