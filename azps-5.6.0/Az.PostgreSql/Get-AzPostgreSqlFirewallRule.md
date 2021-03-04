---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: ecd254c26aba19b99e046efb88c7651d007ae05f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967763"
---
# <span data-ttu-id="a4a0f-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a4a0f-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="a4a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a0f-103">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="a4a0f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4a0f-104">SYNTAX</span></span>

### <span data-ttu-id="a4a0f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4a0f-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4a0f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a4a0f-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4a0f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4a0f-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4a0f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4a0f-108">DESCRIPTION</span></span>
<span data-ttu-id="a4a0f-109">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="a4a0f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4a0f-110">EXAMPLES</span></span>

### <span data-ttu-id="a4a0f-111">Пример 1. Список всех правил брандмауэра на указанном сервере PostgreSql</span><span class="sxs-lookup"><span data-stu-id="a4a0f-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="a4a0f-112">Этот cmdlet перечисляет все правило брандмауэра на указанном сервере PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="a4a0f-113">Пример 2. Получить правило брандмауэра по имени</span><span class="sxs-lookup"><span data-stu-id="a4a0f-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="a4a0f-114">Этот cmdlet получает правило брандмауэра по имени.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="a4a0f-115">Пример 3. Получить правило брандмауэра по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="a4a0f-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="a4a0f-116">Этот cmdlet получает правило брандмауэра по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="a4a0f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4a0f-117">PARAMETERS</span></span>

### <span data-ttu-id="a4a0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a0f-118">-DefaultProfile</span></span>
<span data-ttu-id="a4a0f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a0f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4a0f-120">-InputObject</span></span>
<span data-ttu-id="a4a0f-121">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4a0f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a4a0f-122">-Name</span></span>
<span data-ttu-id="a4a0f-123">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="a4a0f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a0f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4a0f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-125">The name of the resource group.</span></span>
<span data-ttu-id="a4a0f-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a4a0f-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4a0f-127">-ServerName</span></span>
<span data-ttu-id="a4a0f-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-128">The name of the server.</span></span>

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

### <span data-ttu-id="a4a0f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4a0f-129">-SubscriptionId</span></span>
<span data-ttu-id="a4a0f-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a4a0f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a0f-131">CommonParameters</span></span>
<span data-ttu-id="a4a0f-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a0f-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4a0f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a0f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4a0f-134">INPUTS</span></span>

### <span data-ttu-id="a4a0f-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a4a0f-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="a4a0f-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4a0f-136">OUTPUTS</span></span>

### <span data-ttu-id="a4a0f-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a4a0f-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="a4a0f-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4a0f-138">NOTES</span></span>

<span data-ttu-id="a4a0f-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a4a0f-139">ALIASES</span></span>

<span data-ttu-id="a4a0f-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a4a0f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4a0f-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4a0f-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4a0f-143">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a4a0f-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4a0f-144">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a4a0f-145">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a4a0f-146">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a4a0f-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a4a0f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4a0f-148">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a4a0f-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a4a0f-150">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="a4a0f-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a4a0f-152">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a4a0f-153">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a4a0f-154">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="a4a0f-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a4a0f-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4a0f-155">RELATED LINKS</span></span>

