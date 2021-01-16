---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: fae355df0b33fa648be1d9043f140123cf9d79a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410215"
---
# <span data-ttu-id="5eacc-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="5eacc-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="5eacc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eacc-102">SYNOPSIS</span></span>
<span data-ttu-id="5eacc-103">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="5eacc-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="5eacc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5eacc-104">SYNTAX</span></span>

### <span data-ttu-id="5eacc-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5eacc-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5eacc-106">Получить</span><span class="sxs-lookup"><span data-stu-id="5eacc-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5eacc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5eacc-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5eacc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5eacc-108">DESCRIPTION</span></span>
<span data-ttu-id="5eacc-109">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="5eacc-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="5eacc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5eacc-110">EXAMPLES</span></span>

### <span data-ttu-id="5eacc-111">Пример 1. Список всех конфигураций в указанном сервере MySql</span><span class="sxs-lookup"><span data-stu-id="5eacc-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="5eacc-112">Этот cmdlet перечисляет все конфигурации указанного сервера MySql.</span><span class="sxs-lookup"><span data-stu-id="5eacc-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="5eacc-113">Пример 2. Настройка mySql по имени</span><span class="sxs-lookup"><span data-stu-id="5eacc-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="5eacc-114">Этот cmdlet получает заданную конфигурацию MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="5eacc-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="5eacc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5eacc-115">PARAMETERS</span></span>

### <span data-ttu-id="5eacc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eacc-116">-DefaultProfile</span></span>
<span data-ttu-id="5eacc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5eacc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eacc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eacc-118">-InputObject</span></span>
<span data-ttu-id="5eacc-119">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5eacc-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5eacc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5eacc-120">-Name</span></span>
<span data-ttu-id="5eacc-121">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="5eacc-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eacc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eacc-122">-ResourceGroupName</span></span>
<span data-ttu-id="5eacc-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5eacc-123">The name of the resource group.</span></span>
<span data-ttu-id="5eacc-124">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5eacc-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5eacc-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5eacc-125">-ServerName</span></span>
<span data-ttu-id="5eacc-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5eacc-126">The name of the server.</span></span>

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

### <span data-ttu-id="5eacc-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5eacc-127">-SubscriptionId</span></span>
<span data-ttu-id="5eacc-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5eacc-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5eacc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eacc-129">CommonParameters</span></span>
<span data-ttu-id="5eacc-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eacc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eacc-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5eacc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eacc-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5eacc-132">INPUTS</span></span>

### <span data-ttu-id="5eacc-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5eacc-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5eacc-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5eacc-134">OUTPUTS</span></span>

### <span data-ttu-id="5eacc-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="5eacc-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="5eacc-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5eacc-136">NOTES</span></span>

<span data-ttu-id="5eacc-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5eacc-137">ALIASES</span></span>

<span data-ttu-id="5eacc-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5eacc-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5eacc-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5eacc-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5eacc-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5eacc-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5eacc-141">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="5eacc-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5eacc-142">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="5eacc-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5eacc-143">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5eacc-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5eacc-144">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="5eacc-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5eacc-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="5eacc-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5eacc-146">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="5eacc-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="5eacc-147">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="5eacc-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5eacc-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5eacc-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5eacc-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5eacc-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="5eacc-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="5eacc-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5eacc-151">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5eacc-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5eacc-152">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5eacc-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5eacc-153">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="5eacc-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5eacc-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5eacc-154">RELATED LINKS</span></span>
