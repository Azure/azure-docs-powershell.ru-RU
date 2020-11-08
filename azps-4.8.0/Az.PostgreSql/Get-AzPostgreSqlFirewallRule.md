---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235948"
---
# <span data-ttu-id="e7d7d-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7d7d-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="e7d7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d7d-103">Получает сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="e7d7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7d7d-104">SYNTAX</span></span>

### <span data-ttu-id="e7d7d-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7d7d-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e7d7d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="e7d7d-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e7d7d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e7d7d-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7d7d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7d7d-108">DESCRIPTION</span></span>
<span data-ttu-id="e7d7d-109">Получает сведения о правиле брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="e7d7d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7d7d-110">EXAMPLES</span></span>

### <span data-ttu-id="e7d7d-111">Пример 1: список всех правил брандмауэра на указанном сервере PostgreSql</span><span class="sxs-lookup"><span data-stu-id="e7d7d-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="e7d7d-112">Этот командлет перечисляет все правила брандмауэра на указанном сервере PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="e7d7d-113">Пример 2: получение правила брандмауэра по имени</span><span class="sxs-lookup"><span data-stu-id="e7d7d-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="e7d7d-114">Этот командлет получает правило брандмауэра по имени.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="e7d7d-115">Пример 3: получение правила брандмауэра по удостоверению</span><span class="sxs-lookup"><span data-stu-id="e7d7d-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="e7d7d-116">Этот командлет получает правило брандмауэра по удостоверению.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="e7d7d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7d7d-117">PARAMETERS</span></span>

### <span data-ttu-id="e7d7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d7d-118">-DefaultProfile</span></span>
<span data-ttu-id="e7d7d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7d7d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7d7d-120">-InputObject</span></span>
<span data-ttu-id="e7d7d-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e7d7d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7d7d-122">-Name</span></span>
<span data-ttu-id="e7d7d-123">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="e7d7d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d7d-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7d7d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-125">The name of the resource group.</span></span>
<span data-ttu-id="e7d7d-126">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e7d7d-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e7d7d-127">-ServerName</span></span>
<span data-ttu-id="e7d7d-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-128">The name of the server.</span></span>

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

### <span data-ttu-id="e7d7d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7d7d-129">-SubscriptionId</span></span>
<span data-ttu-id="e7d7d-130">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e7d7d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d7d-131">CommonParameters</span></span>
<span data-ttu-id="e7d7d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d7d-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7d7d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d7d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7d7d-134">INPUTS</span></span>

### <span data-ttu-id="e7d7d-135">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e7d7d-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e7d7d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7d7d-136">OUTPUTS</span></span>

### <span data-ttu-id="e7d7d-137">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7d7d-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="e7d7d-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7d7d-138">NOTES</span></span>

<span data-ttu-id="e7d7d-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e7d7d-139">ALIASES</span></span>

<span data-ttu-id="e7d7d-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e7d7d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e7d7d-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7d7d-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e7d7d-143">INPUTOBJECT <IPostgreSqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e7d7d-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e7d7d-144">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e7d7d-145">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e7d7d-146">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e7d7d-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e7d7d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e7d7d-148">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e7d7d-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e7d7d-150">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="e7d7d-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e7d7d-152">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e7d7d-153">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e7d7d-154">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e7d7d-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e7d7d-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7d7d-155">RELATED LINKS</span></span>
