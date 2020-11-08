---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: b92390969c4650d60d5c4a6954520fbbf3f26c71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244413"
---
# <span data-ttu-id="adb61-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb61-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="adb61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="adb61-102">SYNOPSIS</span></span>
<span data-ttu-id="adb61-103">Получает сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="adb61-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="adb61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="adb61-104">SYNTAX</span></span>

### <span data-ttu-id="adb61-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adb61-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="adb61-106">Получить</span><span class="sxs-lookup"><span data-stu-id="adb61-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="adb61-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="adb61-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="adb61-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adb61-108">DESCRIPTION</span></span>
<span data-ttu-id="adb61-109">Получает сведения о конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="adb61-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="adb61-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="adb61-110">EXAMPLES</span></span>

### <span data-ttu-id="adb61-111">Пример 1: список всех конфигураций на указанном сервере MySql</span><span class="sxs-lookup"><span data-stu-id="adb61-111">Example 1: List all configurations in specified MySql server</span></span>
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

<span data-ttu-id="adb61-112">Этот командлет выводит список всех конфигураций на указанном сервере MySql.</span><span class="sxs-lookup"><span data-stu-id="adb61-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="adb61-113">Пример 2: получение указанной конфигурации MySql по имени</span><span class="sxs-lookup"><span data-stu-id="adb61-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="adb61-114">Этот командлет получает указанную конфигурацию MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="adb61-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="adb61-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="adb61-115">PARAMETERS</span></span>

### <span data-ttu-id="adb61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb61-116">-DefaultProfile</span></span>
<span data-ttu-id="adb61-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adb61-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb61-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adb61-118">-InputObject</span></span>
<span data-ttu-id="adb61-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="adb61-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="adb61-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="adb61-120">-Name</span></span>
<span data-ttu-id="adb61-121">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="adb61-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="adb61-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb61-122">-ResourceGroupName</span></span>
<span data-ttu-id="adb61-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="adb61-123">The name of the resource group.</span></span>
<span data-ttu-id="adb61-124">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="adb61-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="adb61-125">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="adb61-125">-ServerName</span></span>
<span data-ttu-id="adb61-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="adb61-126">The name of the server.</span></span>

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

### <span data-ttu-id="adb61-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="adb61-127">-SubscriptionId</span></span>
<span data-ttu-id="adb61-128">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="adb61-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="adb61-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb61-129">CommonParameters</span></span>
<span data-ttu-id="adb61-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="adb61-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb61-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adb61-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb61-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="adb61-132">INPUTS</span></span>

### <span data-ttu-id="adb61-133">Microsoft. Azure. PowerShell. командлеты. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="adb61-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="adb61-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="adb61-134">OUTPUTS</span></span>

### <span data-ttu-id="adb61-135">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb61-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="adb61-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="adb61-136">NOTES</span></span>

<span data-ttu-id="adb61-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="adb61-137">ALIASES</span></span>

<span data-ttu-id="adb61-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="adb61-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="adb61-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="adb61-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="adb61-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="adb61-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="adb61-141">INPUTOBJECT <IMySqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="adb61-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="adb61-142">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="adb61-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="adb61-143">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="adb61-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="adb61-144">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="adb61-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="adb61-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="adb61-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="adb61-146">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="adb61-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="adb61-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="adb61-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="adb61-148">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="adb61-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="adb61-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="adb61-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="adb61-150">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="adb61-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="adb61-151">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="adb61-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="adb61-152">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="adb61-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="adb61-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adb61-153">RELATED LINKS</span></span>

