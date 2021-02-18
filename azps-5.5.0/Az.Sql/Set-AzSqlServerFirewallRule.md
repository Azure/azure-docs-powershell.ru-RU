---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231692"
---
# <span data-ttu-id="08a83-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="08a83-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="08a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08a83-102">SYNOPSIS</span></span>
<span data-ttu-id="08a83-103">Изменяет правило брандмауэра в Azure SQL database server.</span><span class="sxs-lookup"><span data-stu-id="08a83-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="08a83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="08a83-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08a83-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08a83-105">DESCRIPTION</span></span>
<span data-ttu-id="08a83-106">Cmdlet **Set-AzSqlServerFirewallRule** изменяет правило брандмауэра на сервере базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="08a83-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="08a83-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="08a83-107">EXAMPLES</span></span>

### <span data-ttu-id="08a83-108">Пример 1. Изменение правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="08a83-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="08a83-109">Эта команда изменяет правило брандмауэра с именем Rule01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="08a83-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="08a83-110">Команда изменяет IP-адреса начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="08a83-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="08a83-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08a83-111">PARAMETERS</span></span>

### <span data-ttu-id="08a83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08a83-112">-DefaultProfile</span></span>
<span data-ttu-id="08a83-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="08a83-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08a83-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="08a83-114">-EndIpAddress</span></span>
<span data-ttu-id="08a83-115">Указывает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="08a83-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a83-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="08a83-116">-FirewallRuleName</span></span>
<span data-ttu-id="08a83-117">Указывает имя правила брандмауэра, которое изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08a83-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="08a83-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08a83-118">-ResourceGroupName</span></span>
<span data-ttu-id="08a83-119">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="08a83-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="08a83-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08a83-120">-ServerName</span></span>
<span data-ttu-id="08a83-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="08a83-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="08a83-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="08a83-122">-StartIpAddress</span></span>
<span data-ttu-id="08a83-123">Указывает начало диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="08a83-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a83-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08a83-124">-Confirm</span></span>
<span data-ttu-id="08a83-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="08a83-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08a83-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08a83-126">-WhatIf</span></span>
<span data-ttu-id="08a83-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08a83-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08a83-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="08a83-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08a83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a83-129">CommonParameters</span></span>
<span data-ttu-id="08a83-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08a83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a83-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08a83-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a83-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08a83-132">INPUTS</span></span>

### <span data-ttu-id="08a83-133">System.String</span><span class="sxs-lookup"><span data-stu-id="08a83-133">System.String</span></span>

## <span data-ttu-id="08a83-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="08a83-134">OUTPUTS</span></span>

### <span data-ttu-id="08a83-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="08a83-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="08a83-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="08a83-136">NOTES</span></span>

## <span data-ttu-id="08a83-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08a83-137">RELATED LINKS</span></span>

[<span data-ttu-id="08a83-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="08a83-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="08a83-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="08a83-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="08a83-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="08a83-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="08a83-141">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="08a83-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


