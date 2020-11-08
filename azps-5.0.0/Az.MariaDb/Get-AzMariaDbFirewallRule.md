---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248909"
---
# <span data-ttu-id="460e4-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="460e4-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="460e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="460e4-102">SYNOPSIS</span></span>
<span data-ttu-id="460e4-103">Получает сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="460e4-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="460e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="460e4-104">SYNTAX</span></span>

### <span data-ttu-id="460e4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="460e4-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="460e4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="460e4-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="460e4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="460e4-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="460e4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="460e4-108">DESCRIPTION</span></span>
<span data-ttu-id="460e4-109">Получает сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="460e4-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="460e4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="460e4-110">EXAMPLES</span></span>

### <span data-ttu-id="460e4-111">Пример 1: список всех правил брандмауэра в MariaDB</span><span class="sxs-lookup"><span data-stu-id="460e4-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="460e4-112">В этой команде перечислены все правила girewall в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="460e4-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="460e4-113">Пример 2: получение правила брандмауэра для MariaDB</span><span class="sxs-lookup"><span data-stu-id="460e4-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="460e4-114">Эта команда получает правило брандмауэра в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="460e4-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="460e4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="460e4-115">PARAMETERS</span></span>

### <span data-ttu-id="460e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460e4-116">-DefaultProfile</span></span>
<span data-ttu-id="460e4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="460e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="460e4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="460e4-118">-InputObject</span></span>
<span data-ttu-id="460e4-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="460e4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="460e4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="460e4-120">-Name</span></span>
<span data-ttu-id="460e4-121">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="460e4-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="460e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="460e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="460e4-123">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="460e4-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="460e4-124">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="460e4-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="460e4-125">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="460e4-125">-ServerName</span></span>
<span data-ttu-id="460e4-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="460e4-126">The name of the server.</span></span>

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

### <span data-ttu-id="460e4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="460e4-127">-SubscriptionId</span></span>
<span data-ttu-id="460e4-128">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="460e4-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="460e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460e4-129">CommonParameters</span></span>
<span data-ttu-id="460e4-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="460e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460e4-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="460e4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460e4-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="460e4-132">INPUTS</span></span>

### <span data-ttu-id="460e4-133">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="460e4-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="460e4-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="460e4-134">OUTPUTS</span></span>

### <span data-ttu-id="460e4-135">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="460e4-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="460e4-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="460e4-136">NOTES</span></span>

<span data-ttu-id="460e4-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="460e4-137">ALIASES</span></span>

<span data-ttu-id="460e4-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="460e4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="460e4-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="460e4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="460e4-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="460e4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="460e4-141">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="460e4-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="460e4-142">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="460e4-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="460e4-143">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="460e4-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="460e4-144">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="460e4-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="460e4-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="460e4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="460e4-146">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="460e4-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="460e4-147">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="460e4-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="460e4-148">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="460e4-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="460e4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="460e4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="460e4-150">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="460e4-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="460e4-151">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="460e4-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="460e4-152">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="460e4-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="460e4-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="460e4-153">RELATED LINKS</span></span>

