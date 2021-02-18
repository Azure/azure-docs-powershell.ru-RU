---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231737"
---
# <span data-ttu-id="f3a30-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3a30-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="f3a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3a30-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a30-103">Удаляет правило брандмауэра с SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="f3a30-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="f3a30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3a30-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3a30-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3a30-105">DESCRIPTION</span></span>
<span data-ttu-id="f3a30-106">С **помощью cmdlet Remove-AzSqlServerFirewallRule** вы удаляете правило брандмауэра с указанного сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f3a30-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="f3a30-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3a30-107">EXAMPLES</span></span>

### <span data-ttu-id="f3a30-108">Пример 1. Удаление правила</span><span class="sxs-lookup"><span data-stu-id="f3a30-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="f3a30-109">Эта команда удаляет правило брандмауэра с именем Rule01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="f3a30-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="f3a30-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3a30-110">PARAMETERS</span></span>

### <span data-ttu-id="f3a30-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a30-111">-DefaultProfile</span></span>
<span data-ttu-id="f3a30-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f3a30-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3a30-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f3a30-113">-FirewallRuleName</span></span>
<span data-ttu-id="f3a30-114">Указывает имя правила брандмауэра, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3a30-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a30-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f3a30-115">-Force</span></span>
<span data-ttu-id="f3a30-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f3a30-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a30-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a30-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3a30-118">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="f3a30-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f3a30-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3a30-119">-ServerName</span></span>
<span data-ttu-id="f3a30-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f3a30-120">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a30-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3a30-121">-Confirm</span></span>
<span data-ttu-id="f3a30-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3a30-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3a30-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a30-123">-WhatIf</span></span>
<span data-ttu-id="f3a30-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3a30-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3a30-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f3a30-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3a30-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a30-126">CommonParameters</span></span>
<span data-ttu-id="f3a30-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3a30-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a30-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3a30-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a30-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3a30-129">INPUTS</span></span>

### <span data-ttu-id="f3a30-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f3a30-130">System.String</span></span>

## <span data-ttu-id="f3a30-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3a30-131">OUTPUTS</span></span>

### <span data-ttu-id="f3a30-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="f3a30-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="f3a30-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3a30-133">NOTES</span></span>

## <span data-ttu-id="f3a30-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3a30-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3a30-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3a30-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f3a30-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3a30-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f3a30-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3a30-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f3a30-138">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="f3a30-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


