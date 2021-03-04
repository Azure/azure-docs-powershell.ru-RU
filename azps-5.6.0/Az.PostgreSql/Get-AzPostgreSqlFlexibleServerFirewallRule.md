---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: c6197ff97191c50f7f85acbee0a8ce51b54d8211
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955688"
---
# <span data-ttu-id="62724-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="62724-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="62724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62724-102">SYNOPSIS</span></span>
<span data-ttu-id="62724-103">Перечислить все правила брандмауэра на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="62724-103">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="62724-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62724-104">SYNTAX</span></span>

### <span data-ttu-id="62724-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62724-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="62724-106">Получить</span><span class="sxs-lookup"><span data-stu-id="62724-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="62724-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="62724-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="62724-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62724-108">DESCRIPTION</span></span>
<span data-ttu-id="62724-109">Перечислить все правила брандмауэра на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="62724-109">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="62724-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62724-110">EXAMPLES</span></span>

### <span data-ttu-id="62724-111">Пример 1. Получить правила брандмауэра по имени</span><span class="sxs-lookup"><span data-stu-id="62724-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="62724-112">Этот cmdlet получает правила брандмауэра по имени.</span><span class="sxs-lookup"><span data-stu-id="62724-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="62724-113">Пример 2. Получить правила брандмауэра по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="62724-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/servers/postgresql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="62724-114">Этот cmdlet получает правила брандмауэра по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="62724-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="62724-115">Пример 3. Список всех правил брандмауэра на указанном сервере PostgreSql</span><span class="sxs-lookup"><span data-stu-id="62724-115">Example 3: Lists all the firewall rules in the specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="62724-116">Этот cmdlet перечисляет все правило брандмауэра на указанном сервере PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="62724-116">This cmdlet lists all the firewall rule in specified PostgreSql server.</span></span>

## <span data-ttu-id="62724-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62724-117">PARAMETERS</span></span>

### <span data-ttu-id="62724-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62724-118">-DefaultProfile</span></span>
<span data-ttu-id="62724-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62724-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62724-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62724-120">-InputObject</span></span>
<span data-ttu-id="62724-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="62724-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62724-122">-Name</span><span class="sxs-lookup"><span data-stu-id="62724-122">-Name</span></span>
<span data-ttu-id="62724-123">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="62724-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="62724-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62724-124">-ResourceGroupName</span></span>
<span data-ttu-id="62724-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62724-125">The name of the resource group.</span></span>
<span data-ttu-id="62724-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="62724-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="62724-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62724-127">-ServerName</span></span>
<span data-ttu-id="62724-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="62724-128">The name of the server.</span></span>

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

### <span data-ttu-id="62724-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62724-129">-SubscriptionId</span></span>
<span data-ttu-id="62724-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="62724-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="62724-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62724-131">CommonParameters</span></span>
<span data-ttu-id="62724-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62724-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62724-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62724-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62724-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62724-134">INPUTS</span></span>

### <span data-ttu-id="62724-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="62724-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="62724-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62724-136">OUTPUTS</span></span>

### <span data-ttu-id="62724-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="62724-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="62724-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62724-138">NOTES</span></span>

<span data-ttu-id="62724-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="62724-139">ALIASES</span></span>

<span data-ttu-id="62724-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="62724-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62724-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="62724-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62724-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62724-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62724-143">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="62724-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="62724-144">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="62724-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="62724-145">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="62724-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="62724-146">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="62724-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="62724-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="62724-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="62724-148">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="62724-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="62724-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62724-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="62724-150">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="62724-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="62724-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="62724-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="62724-152">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="62724-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="62724-153">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="62724-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="62724-154">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="62724-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="62724-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62724-155">RELATED LINKS</span></span>

