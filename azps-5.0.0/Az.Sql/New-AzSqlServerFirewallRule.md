---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 7274eb30cd7a96e6cf3c46dd37ebab2ddb283c64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246656"
---
# <span data-ttu-id="90666-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90666-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="90666-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90666-102">SYNOPSIS</span></span>
<span data-ttu-id="90666-103">Создает правило брандмауэра для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="90666-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="90666-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90666-104">SYNTAX</span></span>

### <span data-ttu-id="90666-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="90666-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90666-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="90666-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90666-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90666-107">DESCRIPTION</span></span>
<span data-ttu-id="90666-108">Командлет **New-AzSqlServerFirewallRule** создает правило брандмауэра для указанного сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="90666-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="90666-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90666-109">EXAMPLES</span></span>

### <span data-ttu-id="90666-110">Пример 1: Создание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="90666-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="90666-111">Эта команда создает правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="90666-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="90666-112">Правило включает указанные начальные и конечные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="90666-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="90666-113">Пример 2: Создание правила брандмауэра, позволяющего всем IP-адресам Azure получить доступ к серверу</span><span class="sxs-lookup"><span data-stu-id="90666-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="90666-114">Эта команда создает правило брандмауэра на сервере с именем Server01, которое принадлежит к группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="90666-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="90666-115">Поскольку используется параметр *AllowAllAzureIPs* , правило брандмауэра разрешает всем IP-адресам Azure доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="90666-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="90666-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90666-116">PARAMETERS</span></span>

### <span data-ttu-id="90666-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="90666-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="90666-118">Указывает на то, что это правило брандмауэра разрешает всем IP-адресам Azure доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="90666-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="90666-119">Вы не можете использовать этот параметр, если вы планируете использовать параметры *FirewallRuleName* , *StartIpAddress* и *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="90666-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="90666-120">Если вы хотите разрешить IP-адресам службы Azure доступ к серверу, этот параметр следует использовать в отдельном вызове командлета, который не использует параметры *FirewallRuleName* , *StartIpAddress* и *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="90666-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

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

### <span data-ttu-id="90666-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90666-121">-DefaultProfile</span></span>
<span data-ttu-id="90666-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="90666-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90666-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="90666-123">-EndIpAddress</span></span>
<span data-ttu-id="90666-124">Задает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="90666-124">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="90666-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="90666-125">-FirewallRuleName</span></span>
<span data-ttu-id="90666-126">Задает имя нового правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="90666-126">Specifies the name of the new firewall rule.</span></span>

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

### <span data-ttu-id="90666-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90666-127">-ResourceGroupName</span></span>
<span data-ttu-id="90666-128">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="90666-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="90666-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="90666-129">-ServerName</span></span>
<span data-ttu-id="90666-130">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="90666-130">Specifies the name of a server.</span></span>
<span data-ttu-id="90666-131">Укажите имя сервера, а не полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="90666-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="90666-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="90666-132">-StartIpAddress</span></span>
<span data-ttu-id="90666-133">Задает начальное значение диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="90666-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="90666-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90666-134">-Confirm</span></span>
<span data-ttu-id="90666-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90666-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90666-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90666-136">-WhatIf</span></span>
<span data-ttu-id="90666-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90666-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90666-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90666-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90666-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90666-139">CommonParameters</span></span>
<span data-ttu-id="90666-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90666-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90666-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90666-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90666-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90666-142">INPUTS</span></span>

### <span data-ttu-id="90666-143">System. String</span><span class="sxs-lookup"><span data-stu-id="90666-143">System.String</span></span>

## <span data-ttu-id="90666-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90666-144">OUTPUTS</span></span>

### <span data-ttu-id="90666-145">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="90666-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="90666-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="90666-146">NOTES</span></span>

## <span data-ttu-id="90666-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90666-147">RELATED LINKS</span></span>

[<span data-ttu-id="90666-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90666-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="90666-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90666-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="90666-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90666-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="90666-151">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="90666-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


