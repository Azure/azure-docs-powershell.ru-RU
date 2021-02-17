---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 7274eb30cd7a96e6cf3c46dd37ebab2ddb283c64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212436"
---
# <span data-ttu-id="8103c-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8103c-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="8103c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8103c-102">SYNOPSIS</span></span>
<span data-ttu-id="8103c-103">Создает правило брандмауэра для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="8103c-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="8103c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8103c-104">SYNTAX</span></span>

### <span data-ttu-id="8103c-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="8103c-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8103c-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="8103c-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8103c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8103c-107">DESCRIPTION</span></span>
<span data-ttu-id="8103c-108">Для указанного сервера базы данных Azure SQL создается правило брандмауэра **New-AzSqlServerFirewallRule.**</span><span class="sxs-lookup"><span data-stu-id="8103c-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="8103c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8103c-109">EXAMPLES</span></span>

### <span data-ttu-id="8103c-110">Пример 1. Создание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="8103c-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="8103c-111">Эта команда создает правило брандмауэра с именем Rule01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="8103c-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="8103c-112">Правило содержит указанные IP-адреса для начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="8103c-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="8103c-113">Пример 2. Создание правила брандмауэра, которое обеспечивает всем IP-адресам Azure доступ к серверу</span><span class="sxs-lookup"><span data-stu-id="8103c-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="8103c-114">Эта команда создает правило брандмауэра на сервере Server01, которое принадлежит к группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8103c-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="8103c-115">Так как *используется параметр AllowAllAzureIPs,* правило брандмауэра позволяет всем IP-адресам Azure получать доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="8103c-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="8103c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8103c-116">PARAMETERS</span></span>

### <span data-ttu-id="8103c-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="8103c-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="8103c-118">Указывает на то, что это правило брандмауэра позволяет всем IP-адресам Azure получать доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="8103c-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="8103c-119">Этот параметр нельзя использовать, если предполагается использовать параметры *FirewallRuleName,* *StartIpAddress* и *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="8103c-119">You cannot use this parameter if you intend to use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="8103c-120">Если вы хотите разрешить этим пользователям получать доступ к серверу, этот параметр следует использовать в отдельном вызове с помощью cmdlet, в который не используются параметры *FirewallRuleName,* *StartIpAddress* и *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="8103c-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8103c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8103c-121">-DefaultProfile</span></span>
<span data-ttu-id="8103c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8103c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8103c-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="8103c-123">-EndIpAddress</span></span>
<span data-ttu-id="8103c-124">Указывает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="8103c-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8103c-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="8103c-125">-FirewallRuleName</span></span>
<span data-ttu-id="8103c-126">Указывает имя нового правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8103c-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8103c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8103c-127">-ResourceGroupName</span></span>
<span data-ttu-id="8103c-128">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="8103c-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8103c-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8103c-129">-ServerName</span></span>
<span data-ttu-id="8103c-130">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="8103c-130">Specifies the name of a server.</span></span>
<span data-ttu-id="8103c-131">Укажите имя сервера, а не полное имя DNS.</span><span class="sxs-lookup"><span data-stu-id="8103c-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="8103c-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="8103c-132">-StartIpAddress</span></span>
<span data-ttu-id="8103c-133">Указывает начало диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8103c-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8103c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8103c-134">-Confirm</span></span>
<span data-ttu-id="8103c-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8103c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8103c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8103c-136">-WhatIf</span></span>
<span data-ttu-id="8103c-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8103c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8103c-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8103c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8103c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8103c-139">CommonParameters</span></span>
<span data-ttu-id="8103c-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8103c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8103c-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8103c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8103c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8103c-142">INPUTS</span></span>

### <span data-ttu-id="8103c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8103c-143">System.String</span></span>

## <span data-ttu-id="8103c-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8103c-144">OUTPUTS</span></span>

### <span data-ttu-id="8103c-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="8103c-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="8103c-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8103c-146">NOTES</span></span>

## <span data-ttu-id="8103c-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8103c-147">RELATED LINKS</span></span>

[<span data-ttu-id="8103c-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8103c-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="8103c-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8103c-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="8103c-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8103c-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="8103c-151">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="8103c-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


