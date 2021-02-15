---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237233"
---
# <span data-ttu-id="a4884-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4884-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="a4884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4884-102">SYNOPSIS</span></span>
<span data-ttu-id="a4884-103">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="a4884-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a4884-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4884-104">SYNTAX</span></span>

### <span data-ttu-id="a4884-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4884-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4884-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a4884-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4884-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4884-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4884-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4884-108">DESCRIPTION</span></span>
<span data-ttu-id="a4884-109">Сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="a4884-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a4884-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4884-110">EXAMPLES</span></span>

### <span data-ttu-id="a4884-111">Пример 1. Список всех конфигураций в указанном сервере MySql</span><span class="sxs-lookup"><span data-stu-id="a4884-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a4884-112">Этот cmdlet перечисляет все конфигурации на указанном сервере MySql.</span><span class="sxs-lookup"><span data-stu-id="a4884-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="a4884-113">Пример 2. Получить указанную конфигурацию MySql по имени</span><span class="sxs-lookup"><span data-stu-id="a4884-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a4884-114">Этот cmdlet получает заданную конфигурацию MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="a4884-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="a4884-115">Пример 3. Настройка списка по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="a4884-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a4884-116">Этот cmdlet получает заданную конфигурацию MySql по удостоверению.</span><span class="sxs-lookup"><span data-stu-id="a4884-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="a4884-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4884-117">PARAMETERS</span></span>

### <span data-ttu-id="a4884-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4884-118">-DefaultProfile</span></span>
<span data-ttu-id="a4884-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4884-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4884-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4884-120">-InputObject</span></span>
<span data-ttu-id="a4884-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a4884-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4884-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a4884-122">-Name</span></span>
<span data-ttu-id="a4884-123">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="a4884-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="a4884-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4884-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4884-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4884-125">The name of the resource group.</span></span>
<span data-ttu-id="a4884-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="a4884-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a4884-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4884-127">-ServerName</span></span>
<span data-ttu-id="a4884-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a4884-128">The name of the server.</span></span>

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

### <span data-ttu-id="a4884-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4884-129">-SubscriptionId</span></span>
<span data-ttu-id="a4884-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a4884-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a4884-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4884-131">CommonParameters</span></span>
<span data-ttu-id="a4884-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4884-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4884-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4884-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4884-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4884-134">INPUTS</span></span>

### <span data-ttu-id="a4884-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a4884-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a4884-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4884-136">OUTPUTS</span></span>

### <span data-ttu-id="a4884-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="a4884-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="a4884-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4884-138">NOTES</span></span>

<span data-ttu-id="a4884-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a4884-139">ALIASES</span></span>

<span data-ttu-id="a4884-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a4884-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4884-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a4884-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4884-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4884-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4884-143">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a4884-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4884-144">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="a4884-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a4884-145">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="a4884-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a4884-146">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="a4884-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a4884-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a4884-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4884-148">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="a4884-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a4884-149">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="a4884-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a4884-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4884-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a4884-151">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="a4884-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="a4884-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="a4884-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a4884-153">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a4884-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a4884-154">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a4884-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a4884-155">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="a4884-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a4884-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4884-156">RELATED LINKS</span></span>

