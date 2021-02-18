---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 7f2a3e567da4df9a004c5dac642f480a4cd7388a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224113"
---
# <span data-ttu-id="54bfa-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="54bfa-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="54bfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="54bfa-103">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="54bfa-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="54bfa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54bfa-104">SYNTAX</span></span>

### <span data-ttu-id="54bfa-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54bfa-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54bfa-106">Получить</span><span class="sxs-lookup"><span data-stu-id="54bfa-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54bfa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="54bfa-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="54bfa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54bfa-108">DESCRIPTION</span></span>
<span data-ttu-id="54bfa-109">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="54bfa-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="54bfa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54bfa-110">EXAMPLES</span></span>

### <span data-ttu-id="54bfa-111">Пример 1. Получить правила брандмауэра по имени</span><span class="sxs-lookup"><span data-stu-id="54bfa-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="54bfa-112">Этот cmdlet получает правила брандмауэра по имени.</span><span class="sxs-lookup"><span data-stu-id="54bfa-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="54bfa-113">Пример 2. Получить правила брандмауэра по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="54bfa-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="54bfa-114">Этот cmdlet получает правила брандмауэра по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="54bfa-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="54bfa-115">Пример 3. Список всех правил брандмауэра для указанного сервера MySql</span><span class="sxs-lookup"><span data-stu-id="54bfa-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="54bfa-116">Этот cmdlet перечисляет все правило брандмауэра на указанном сервере MySql.</span><span class="sxs-lookup"><span data-stu-id="54bfa-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="54bfa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54bfa-117">PARAMETERS</span></span>

### <span data-ttu-id="54bfa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54bfa-118">-DefaultProfile</span></span>
<span data-ttu-id="54bfa-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54bfa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54bfa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54bfa-120">-InputObject</span></span>
<span data-ttu-id="54bfa-121">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="54bfa-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="54bfa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="54bfa-122">-Name</span></span>
<span data-ttu-id="54bfa-123">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="54bfa-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="54bfa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54bfa-124">-ResourceGroupName</span></span>
<span data-ttu-id="54bfa-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54bfa-125">The name of the resource group.</span></span>
<span data-ttu-id="54bfa-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="54bfa-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="54bfa-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="54bfa-127">-ServerName</span></span>
<span data-ttu-id="54bfa-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="54bfa-128">The name of the server.</span></span>

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

### <span data-ttu-id="54bfa-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54bfa-129">-SubscriptionId</span></span>
<span data-ttu-id="54bfa-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="54bfa-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="54bfa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54bfa-131">CommonParameters</span></span>
<span data-ttu-id="54bfa-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54bfa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54bfa-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54bfa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54bfa-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54bfa-134">INPUTS</span></span>

### <span data-ttu-id="54bfa-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="54bfa-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="54bfa-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54bfa-136">OUTPUTS</span></span>

### <span data-ttu-id="54bfa-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="54bfa-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="54bfa-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54bfa-138">NOTES</span></span>

<span data-ttu-id="54bfa-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="54bfa-139">ALIASES</span></span>

<span data-ttu-id="54bfa-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="54bfa-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54bfa-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="54bfa-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54bfa-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54bfa-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54bfa-143">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="54bfa-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54bfa-144">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="54bfa-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="54bfa-145">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="54bfa-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="54bfa-146">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="54bfa-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="54bfa-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="54bfa-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54bfa-148">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="54bfa-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="54bfa-149">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="54bfa-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="54bfa-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54bfa-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="54bfa-151">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="54bfa-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="54bfa-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="54bfa-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="54bfa-153">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="54bfa-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="54bfa-154">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="54bfa-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="54bfa-155">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="54bfa-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="54bfa-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54bfa-156">RELATED LINKS</span></span>

