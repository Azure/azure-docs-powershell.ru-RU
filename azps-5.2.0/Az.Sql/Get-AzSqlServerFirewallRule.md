---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404484"
---
# <span data-ttu-id="e5607-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5607-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="e5607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5607-102">SYNOPSIS</span></span>
<span data-ttu-id="e5607-103">Получает правила брандмауэра для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="e5607-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="e5607-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5607-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5607-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5607-105">DESCRIPTION</span></span>
<span data-ttu-id="e5607-106">Для сервера базы данных Azure SQL правила брандмауэра **Get-AzSqlServerFirewallRule.**</span><span class="sxs-lookup"><span data-stu-id="e5607-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="e5607-107">Если указать имя правила брандмауэра, он получит сведения об определенном правиле брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e5607-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="e5607-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5607-108">EXAMPLES</span></span>

### <span data-ttu-id="e5607-109">Пример 1. Получить все правила для сервера</span><span class="sxs-lookup"><span data-stu-id="e5607-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="e5607-110">Эта команда получает все правила брандмауэра для сервера Server01.</span><span class="sxs-lookup"><span data-stu-id="e5607-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="e5607-111">Пример 2. Получить все правила для сервера с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="e5607-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="e5607-112">Эта команда получает все правила брандмауэра для сервера Server01, которые начинаются с "Правило".</span><span class="sxs-lookup"><span data-stu-id="e5607-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="e5607-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5607-113">PARAMETERS</span></span>

### <span data-ttu-id="e5607-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5607-114">-DefaultProfile</span></span>
<span data-ttu-id="e5607-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e5607-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5607-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="e5607-116">-FirewallRuleName</span></span>
<span data-ttu-id="e5607-117">Указывает имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e5607-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5607-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5607-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5607-119">Имя группы ресурсов, которой назначена SQL Server ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5607-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="e5607-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e5607-120">-ServerName</span></span>
<span data-ttu-id="e5607-121">Указывает имя SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5607-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="e5607-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5607-122">-Confirm</span></span>
<span data-ttu-id="e5607-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e5607-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5607-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5607-124">-WhatIf</span></span>
<span data-ttu-id="e5607-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5607-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5607-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e5607-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5607-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5607-127">CommonParameters</span></span>
<span data-ttu-id="e5607-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5607-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5607-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5607-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5607-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5607-130">INPUTS</span></span>

### <span data-ttu-id="e5607-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e5607-131">System.String</span></span>

## <span data-ttu-id="e5607-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5607-132">OUTPUTS</span></span>

### <span data-ttu-id="e5607-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="e5607-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="e5607-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5607-134">NOTES</span></span>

## <span data-ttu-id="e5607-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5607-135">RELATED LINKS</span></span>

[<span data-ttu-id="e5607-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5607-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="e5607-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5607-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="e5607-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5607-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="e5607-139">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="e5607-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


