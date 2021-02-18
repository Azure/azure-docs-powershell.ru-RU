---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224321"
---
# <span data-ttu-id="e6ad3-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e6ad3-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="e6ad3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ad3-103">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="e6ad3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6ad3-104">SYNTAX</span></span>

### <span data-ttu-id="e6ad3-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6ad3-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e6ad3-106">Получить</span><span class="sxs-lookup"><span data-stu-id="e6ad3-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e6ad3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e6ad3-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e6ad3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6ad3-108">DESCRIPTION</span></span>
<span data-ttu-id="e6ad3-109">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="e6ad3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6ad3-110">EXAMPLES</span></span>

### <span data-ttu-id="e6ad3-111">Пример 1. Список всех правил брандмауэра для MariaDB</span><span class="sxs-lookup"><span data-stu-id="e6ad3-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="e6ad3-112">В этой команде перечислены все правила girewall для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="e6ad3-113">Пример 2. Получите правило брандмауэра для MariaDB</span><span class="sxs-lookup"><span data-stu-id="e6ad3-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="e6ad3-114">Эта команда получает правило брандмауэра в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="e6ad3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6ad3-115">PARAMETERS</span></span>

### <span data-ttu-id="e6ad3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ad3-116">-DefaultProfile</span></span>
<span data-ttu-id="e6ad3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6ad3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6ad3-118">-InputObject</span></span>
<span data-ttu-id="e6ad3-119">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ad3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e6ad3-120">-Name</span></span>
<span data-ttu-id="e6ad3-121">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="e6ad3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ad3-122">-ResourceGroupName</span></span>
<span data-ttu-id="e6ad3-123">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e6ad3-124">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e6ad3-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6ad3-125">-ServerName</span></span>
<span data-ttu-id="e6ad3-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-126">The name of the server.</span></span>

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

### <span data-ttu-id="e6ad3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6ad3-127">-SubscriptionId</span></span>
<span data-ttu-id="e6ad3-128">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e6ad3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ad3-129">CommonParameters</span></span>
<span data-ttu-id="e6ad3-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ad3-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6ad3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ad3-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6ad3-132">INPUTS</span></span>

### <span data-ttu-id="e6ad3-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="e6ad3-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="e6ad3-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6ad3-134">OUTPUTS</span></span>

### <span data-ttu-id="e6ad3-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e6ad3-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="e6ad3-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6ad3-136">NOTES</span></span>

<span data-ttu-id="e6ad3-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e6ad3-137">ALIASES</span></span>

<span data-ttu-id="e6ad3-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e6ad3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6ad3-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6ad3-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6ad3-141">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="e6ad3-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6ad3-142">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e6ad3-143">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e6ad3-144">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e6ad3-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="e6ad3-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6ad3-146">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e6ad3-147">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e6ad3-148">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e6ad3-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e6ad3-150">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e6ad3-151">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="e6ad3-152">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="e6ad3-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e6ad3-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6ad3-153">RELATED LINKS</span></span>

