---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: 7991f63e9deb6dcbcf3366a28a8c2159872c9da0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991038"
---
# <span data-ttu-id="52343-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="52343-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="52343-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52343-102">SYNOPSIS</span></span>
<span data-ttu-id="52343-103">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="52343-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="52343-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="52343-104">SYNTAX</span></span>

### <span data-ttu-id="52343-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52343-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="52343-106">Получить</span><span class="sxs-lookup"><span data-stu-id="52343-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="52343-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="52343-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="52343-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52343-108">DESCRIPTION</span></span>
<span data-ttu-id="52343-109">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="52343-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="52343-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="52343-110">EXAMPLES</span></span>

### <span data-ttu-id="52343-111">Пример 1. Список всех правил брандмауэра на указанном сервере MySql</span><span class="sxs-lookup"><span data-stu-id="52343-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="52343-112">Этот cmdlet перечисляет все правило брандмауэра на указанном сервере MySql.</span><span class="sxs-lookup"><span data-stu-id="52343-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="52343-113">Пример 2. Получить правило брандмауэра по имени</span><span class="sxs-lookup"><span data-stu-id="52343-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="52343-114">Этот cmdlet получает правило брандмауэра по имени.</span><span class="sxs-lookup"><span data-stu-id="52343-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="52343-115">Пример 3. Получить правило брандмауэра по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="52343-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="52343-116">Этот cmdlet получает правило брандмауэра по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="52343-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="52343-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52343-117">PARAMETERS</span></span>

### <span data-ttu-id="52343-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52343-118">-DefaultProfile</span></span>
<span data-ttu-id="52343-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52343-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52343-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52343-120">-InputObject</span></span>
<span data-ttu-id="52343-121">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="52343-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52343-122">-Name</span><span class="sxs-lookup"><span data-stu-id="52343-122">-Name</span></span>
<span data-ttu-id="52343-123">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="52343-123">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52343-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52343-124">-ResourceGroupName</span></span>
<span data-ttu-id="52343-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52343-125">The name of the resource group.</span></span>
<span data-ttu-id="52343-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="52343-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52343-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52343-127">-ServerName</span></span>
<span data-ttu-id="52343-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="52343-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52343-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52343-129">-SubscriptionId</span></span>
<span data-ttu-id="52343-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="52343-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52343-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52343-131">CommonParameters</span></span>
<span data-ttu-id="52343-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52343-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52343-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52343-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52343-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52343-134">INPUTS</span></span>

### <span data-ttu-id="52343-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="52343-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="52343-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52343-136">OUTPUTS</span></span>

### <span data-ttu-id="52343-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="52343-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="52343-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="52343-138">NOTES</span></span>

<span data-ttu-id="52343-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="52343-139">ALIASES</span></span>

<span data-ttu-id="52343-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="52343-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52343-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="52343-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52343-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52343-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52343-143">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="52343-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52343-144">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="52343-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="52343-145">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="52343-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="52343-146">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="52343-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="52343-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="52343-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52343-148">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="52343-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="52343-149">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="52343-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="52343-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52343-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="52343-151">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="52343-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="52343-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="52343-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="52343-153">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="52343-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="52343-154">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="52343-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="52343-155">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="52343-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="52343-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52343-156">RELATED LINKS</span></span>

