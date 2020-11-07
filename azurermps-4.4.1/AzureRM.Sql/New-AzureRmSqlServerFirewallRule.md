---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: b40ac97f5658758fa77900dfc31da5f77fb5d0e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732187"
---
# <span data-ttu-id="0ad28-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ad28-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="0ad28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ad28-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad28-103">Создает правило брандмауэра для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="0ad28-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ad28-104">SYNTAX</span></span>

### <span data-ttu-id="0ad28-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0ad28-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad28-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="0ad28-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ad28-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ad28-107">DESCRIPTION</span></span>
<span data-ttu-id="0ad28-108">Командлет **New-AzureRmSqlServerFirewallRule** создает правило брандмауэра для указанного сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad28-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="0ad28-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ad28-109">EXAMPLES</span></span>

### <span data-ttu-id="0ad28-110">Пример 1: Создание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="0ad28-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="0ad28-111">Эта команда создает правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="0ad28-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="0ad28-112">Правило включает указанные начальные и конечные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="0ad28-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="0ad28-113">Пример 2: Создание правила брандмауэра, позволяющего всем IP-адресам Azure получить доступ к серверу</span><span class="sxs-lookup"><span data-stu-id="0ad28-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="0ad28-114">Эта команда создает правило брандмауэра на сервере с именем Server01, которое принадлежит к группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0ad28-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="0ad28-115">Поскольку используется параметр *AllowAllAzureIPs* , правило брандмауэра разрешает всем IP-адресам Azure доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="0ad28-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="0ad28-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ad28-116">PARAMETERS</span></span>

### <span data-ttu-id="0ad28-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="0ad28-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="0ad28-118">Указывает на то, что это правило брандмауэра разрешает всем IP-адресам Azure доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="0ad28-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="0ad28-119">Вы не можете использовать этот параметр, если вы планируете использовать параметры *FirewallRuleName* , *StartIpAddress* и *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="0ad28-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="0ad28-120">Если вы хотите разрешить IP-адресам службы Azure доступ к серверу, этот параметр следует использовать в отдельном вызове командлета, который не использует параметры *FirewallRuleName* , *StartIpAddress* и *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="0ad28-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

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

### <span data-ttu-id="0ad28-121">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="0ad28-121">-EndIpAddress</span></span>
<span data-ttu-id="0ad28-122">Задает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="0ad28-122">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="0ad28-123">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="0ad28-123">-FirewallRuleName</span></span>
<span data-ttu-id="0ad28-124">Задает имя нового правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="0ad28-124">Specifies the name of the new firewall rule.</span></span>

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

### <span data-ttu-id="0ad28-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad28-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ad28-126">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="0ad28-126">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0ad28-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0ad28-127">-ServerName</span></span>
<span data-ttu-id="0ad28-128">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="0ad28-128">Specifies the name of a server.</span></span>
<span data-ttu-id="0ad28-129">Укажите имя сервера, а не полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="0ad28-129">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="0ad28-130">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="0ad28-130">-StartIpAddress</span></span>
<span data-ttu-id="0ad28-131">Задает начальное значение диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="0ad28-131">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="0ad28-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ad28-132">-Confirm</span></span>
<span data-ttu-id="0ad28-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ad28-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad28-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad28-134">-WhatIf</span></span>
<span data-ttu-id="0ad28-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ad28-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ad28-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ad28-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad28-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad28-137">-DefaultProfile</span></span>
<span data-ttu-id="0ad28-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad28-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad28-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad28-139">CommonParameters</span></span>
<span data-ttu-id="0ad28-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ad28-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad28-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad28-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad28-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ad28-142">INPUTS</span></span>

## <span data-ttu-id="0ad28-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ad28-143">OUTPUTS</span></span>

### <span data-ttu-id="0ad28-144">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="0ad28-144">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="0ad28-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ad28-145">NOTES</span></span>

## <span data-ttu-id="0ad28-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ad28-146">RELATED LINKS</span></span>

[<span data-ttu-id="0ad28-147">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ad28-147">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="0ad28-148">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ad28-148">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="0ad28-149">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ad28-149">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="0ad28-150">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="0ad28-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


