---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416468"
---
# <span data-ttu-id="24856-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="24856-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="24856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24856-102">SYNOPSIS</span></span>
<span data-ttu-id="24856-103">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="24856-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="24856-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24856-104">SYNTAX</span></span>

### <span data-ttu-id="24856-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24856-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="24856-106">Получить</span><span class="sxs-lookup"><span data-stu-id="24856-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="24856-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24856-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="24856-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24856-108">DESCRIPTION</span></span>
<span data-ttu-id="24856-109">Сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="24856-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="24856-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24856-110">EXAMPLES</span></span>

### <span data-ttu-id="24856-111">Пример 1. Список всех правил брандмауэра для MariaDB</span><span class="sxs-lookup"><span data-stu-id="24856-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="24856-112">В этой команде перечислены все правила girewall для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="24856-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="24856-113">Пример 2. Получите правило брандмауэра для MariaDB</span><span class="sxs-lookup"><span data-stu-id="24856-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="24856-114">Эта команда получает правило брандмауэра для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="24856-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="24856-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24856-115">PARAMETERS</span></span>

### <span data-ttu-id="24856-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24856-116">-DefaultProfile</span></span>
<span data-ttu-id="24856-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24856-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24856-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24856-118">-InputObject</span></span>
<span data-ttu-id="24856-119">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="24856-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="24856-120">-Name</span><span class="sxs-lookup"><span data-stu-id="24856-120">-Name</span></span>
<span data-ttu-id="24856-121">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="24856-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="24856-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24856-122">-ResourceGroupName</span></span>
<span data-ttu-id="24856-123">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="24856-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="24856-124">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="24856-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="24856-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="24856-125">-ServerName</span></span>
<span data-ttu-id="24856-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="24856-126">The name of the server.</span></span>

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

### <span data-ttu-id="24856-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24856-127">-SubscriptionId</span></span>
<span data-ttu-id="24856-128">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="24856-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="24856-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24856-129">CommonParameters</span></span>
<span data-ttu-id="24856-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24856-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24856-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24856-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24856-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24856-132">INPUTS</span></span>

### <span data-ttu-id="24856-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="24856-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="24856-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24856-134">OUTPUTS</span></span>

### <span data-ttu-id="24856-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="24856-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="24856-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24856-136">NOTES</span></span>

<span data-ttu-id="24856-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="24856-137">ALIASES</span></span>

<span data-ttu-id="24856-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="24856-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24856-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="24856-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24856-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24856-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24856-141">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="24856-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24856-142">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="24856-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="24856-143">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="24856-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="24856-144">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="24856-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="24856-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="24856-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24856-146">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="24856-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="24856-147">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="24856-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="24856-148">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="24856-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="24856-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="24856-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="24856-150">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="24856-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="24856-151">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="24856-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="24856-152">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="24856-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="24856-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24856-153">RELATED LINKS</span></span>

