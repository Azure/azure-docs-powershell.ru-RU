---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421335"
---
# <span data-ttu-id="d7910-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d7910-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="d7910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7910-102">SYNOPSIS</span></span>
<span data-ttu-id="d7910-103">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d7910-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="d7910-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7910-104">SYNTAX</span></span>

### <span data-ttu-id="d7910-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7910-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7910-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d7910-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7910-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d7910-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7910-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7910-108">DESCRIPTION</span></span>
<span data-ttu-id="d7910-109">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d7910-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="d7910-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7910-110">EXAMPLES</span></span>

### <span data-ttu-id="d7910-111">Пример 1. Список всех правил брандмауэра на указанном сервере PostgreSql</span><span class="sxs-lookup"><span data-stu-id="d7910-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="d7910-112">Этот cmdlet перечисляет все правило брандмауэра на указанном сервере PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="d7910-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="d7910-113">Пример 2. Получить правило брандмауэра по имени</span><span class="sxs-lookup"><span data-stu-id="d7910-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="d7910-114">Этот cmdlet получает правило брандмауэра по имени.</span><span class="sxs-lookup"><span data-stu-id="d7910-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="d7910-115">Пример 3. Получить правило брандмауэра по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="d7910-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="d7910-116">Этот cmdlet получает правило брандмауэра по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="d7910-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="d7910-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7910-117">PARAMETERS</span></span>

### <span data-ttu-id="d7910-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7910-118">-DefaultProfile</span></span>
<span data-ttu-id="d7910-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7910-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7910-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7910-120">-InputObject</span></span>
<span data-ttu-id="d7910-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d7910-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d7910-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d7910-122">-Name</span></span>
<span data-ttu-id="d7910-123">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d7910-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="d7910-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7910-124">-ResourceGroupName</span></span>
<span data-ttu-id="d7910-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7910-125">The name of the resource group.</span></span>
<span data-ttu-id="d7910-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d7910-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d7910-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d7910-127">-ServerName</span></span>
<span data-ttu-id="d7910-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d7910-128">The name of the server.</span></span>

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

### <span data-ttu-id="d7910-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7910-129">-SubscriptionId</span></span>
<span data-ttu-id="d7910-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d7910-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d7910-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7910-131">CommonParameters</span></span>
<span data-ttu-id="d7910-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7910-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7910-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7910-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7910-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7910-134">INPUTS</span></span>

### <span data-ttu-id="d7910-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d7910-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d7910-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7910-136">OUTPUTS</span></span>

### <span data-ttu-id="d7910-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d7910-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="d7910-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7910-138">NOTES</span></span>

<span data-ttu-id="d7910-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d7910-139">ALIASES</span></span>

<span data-ttu-id="d7910-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d7910-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7910-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d7910-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7910-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7910-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7910-143">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d7910-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7910-144">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d7910-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d7910-145">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d7910-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d7910-146">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d7910-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d7910-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d7910-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7910-148">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="d7910-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d7910-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7910-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d7910-150">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d7910-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="d7910-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d7910-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d7910-152">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d7910-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d7910-153">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d7910-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d7910-154">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="d7910-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d7910-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7910-155">RELATED LINKS</span></span>

