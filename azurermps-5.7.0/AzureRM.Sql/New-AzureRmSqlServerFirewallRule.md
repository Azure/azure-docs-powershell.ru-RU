---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: cc0d7163b9251037f4127d8fc6894f74f103436b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566064"
---
# <span data-ttu-id="bb658-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb658-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="bb658-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb658-102">SYNOPSIS</span></span>
<span data-ttu-id="bb658-103">Создает правило брандмауэра для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bb658-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb658-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb658-104">SYNTAX</span></span>

### <span data-ttu-id="bb658-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="bb658-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb658-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="bb658-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb658-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb658-107">DESCRIPTION</span></span>
<span data-ttu-id="bb658-108">Командлет **New-AzureRmSqlServerFirewallRule** создает правило брандмауэра для указанного сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bb658-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="bb658-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb658-109">EXAMPLES</span></span>

### <span data-ttu-id="bb658-110">Пример 1: Создание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="bb658-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="bb658-111">Эта команда создает правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="bb658-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="bb658-112">Правило включает указанные начальные и конечные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="bb658-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="bb658-113">Пример 2: Создание правила брандмауэра, позволяющего всем IP-адресам Azure получить доступ к серверу</span><span class="sxs-lookup"><span data-stu-id="bb658-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="bb658-114">Эта команда создает правило брандмауэра на сервере с именем Server01, которое принадлежит к группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="bb658-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="bb658-115">Поскольку используется параметр *AllowAllAzureIPs* , правило брандмауэра разрешает всем IP-адресам Azure доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="bb658-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="bb658-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb658-116">PARAMETERS</span></span>

### <span data-ttu-id="bb658-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="bb658-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="bb658-118">Указывает на то, что это правило брандмауэра разрешает всем IP-адресам Azure доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="bb658-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="bb658-119">Вы не можете использовать этот параметр, если вы планируете использовать параметры *FirewallRuleName* , *StartIpAddress* и *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="bb658-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="bb658-120">Если вы хотите разрешить IP-адресам службы Azure доступ к серверу, этот параметр следует использовать в отдельном вызове командлета, который не использует параметры *FirewallRuleName* , *StartIpAddress* и *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="bb658-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb658-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb658-121">-DefaultProfile</span></span>
<span data-ttu-id="bb658-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb658-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb658-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb658-123">-EndIpAddress</span></span>
<span data-ttu-id="bb658-124">Задает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="bb658-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb658-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="bb658-125">-FirewallRuleName</span></span>
<span data-ttu-id="bb658-126">Задает имя нового правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="bb658-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb658-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb658-127">-ResourceGroupName</span></span>
<span data-ttu-id="bb658-128">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="bb658-128">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb658-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bb658-129">-ServerName</span></span>
<span data-ttu-id="bb658-130">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="bb658-130">Specifies the name of a server.</span></span>
<span data-ttu-id="bb658-131">Укажите имя сервера, а не полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="bb658-131">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb658-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb658-132">-StartIpAddress</span></span>
<span data-ttu-id="bb658-133">Задает начальное значение диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="bb658-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb658-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb658-134">-Confirm</span></span>
<span data-ttu-id="bb658-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb658-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb658-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb658-136">-WhatIf</span></span>
<span data-ttu-id="bb658-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb658-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb658-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb658-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb658-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb658-139">CommonParameters</span></span>
<span data-ttu-id="bb658-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb658-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb658-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb658-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb658-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb658-142">INPUTS</span></span>

### <span data-ttu-id="bb658-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="bb658-143">None</span></span>
<span data-ttu-id="bb658-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bb658-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb658-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb658-145">OUTPUTS</span></span>

### <span data-ttu-id="bb658-146">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="bb658-146">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="bb658-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb658-147">NOTES</span></span>

## <span data-ttu-id="bb658-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb658-148">RELATED LINKS</span></span>

[<span data-ttu-id="bb658-149">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb658-149">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="bb658-150">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb658-150">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="bb658-151">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb658-151">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="bb658-152">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="bb658-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


