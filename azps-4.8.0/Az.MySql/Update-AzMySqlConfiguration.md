---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: c4eb244dd2d1a0d685bf18f39deedf9992b5597e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078977"
---
# <span data-ttu-id="02305-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="02305-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="02305-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02305-102">SYNOPSIS</span></span>
<span data-ttu-id="02305-103">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="02305-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="02305-104">Используйте Update-AzMySqlServer, если хотите обновить AdministratorLoginPassword, SKU и т. д.</span><span class="sxs-lookup"><span data-stu-id="02305-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="02305-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02305-105">SYNTAX</span></span>

### <span data-ttu-id="02305-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02305-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02305-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="02305-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02305-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02305-108">DESCRIPTION</span></span>
<span data-ttu-id="02305-109">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="02305-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="02305-110">Используйте Update-AzMySqlServer, если хотите обновить AdministratorLoginPassword, SKU и т. д.</span><span class="sxs-lookup"><span data-stu-id="02305-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="02305-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02305-111">EXAMPLES</span></span>

### <span data-ttu-id="02305-112">Пример 1: Обновление конфигурации MySql по имени</span><span class="sxs-lookup"><span data-stu-id="02305-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="02305-113">Этот командлет обновляет конфигурацию MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="02305-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="02305-114">Пример 2: Обновление конфигурации MySql по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="02305-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="02305-115">Эти командлеты обновляют конфигурацию MySql по идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="02305-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="02305-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02305-116">PARAMETERS</span></span>

### <span data-ttu-id="02305-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02305-117">-AsJob</span></span>
<span data-ttu-id="02305-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="02305-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02305-119">-DefaultProfile</span></span>
<span data-ttu-id="02305-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02305-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02305-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02305-121">-InputObject</span></span>
<span data-ttu-id="02305-122">Параметр удостоверения.</span><span class="sxs-lookup"><span data-stu-id="02305-122">Identity Parameter.</span></span>
<span data-ttu-id="02305-123">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="02305-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02305-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02305-124">-Name</span></span>
<span data-ttu-id="02305-125">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="02305-125">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-126">-Wait</span><span class="sxs-lookup"><span data-stu-id="02305-126">-NoWait</span></span>
<span data-ttu-id="02305-127">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="02305-127">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02305-128">-ResourceGroupName</span></span>
<span data-ttu-id="02305-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02305-129">The name of the resource group.</span></span>
<span data-ttu-id="02305-130">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="02305-130">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="02305-131">-ServerName</span></span>
<span data-ttu-id="02305-132">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="02305-132">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-133">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="02305-133">-Source</span></span>
<span data-ttu-id="02305-134">Источник конфигурации.</span><span class="sxs-lookup"><span data-stu-id="02305-134">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02305-135">-SubscriptionId</span></span>
<span data-ttu-id="02305-136">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="02305-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-137">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="02305-137">-Value</span></span>
<span data-ttu-id="02305-138">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="02305-138">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02305-139">-Confirm</span></span>
<span data-ttu-id="02305-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02305-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02305-141">-WhatIf</span></span>
<span data-ttu-id="02305-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02305-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02305-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02305-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02305-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02305-144">CommonParameters</span></span>
<span data-ttu-id="02305-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02305-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02305-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02305-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02305-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02305-147">INPUTS</span></span>

### <span data-ttu-id="02305-148">Microsoft. Azure. PowerShell. командлеты. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="02305-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="02305-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02305-149">OUTPUTS</span></span>

### <span data-ttu-id="02305-150">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="02305-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="02305-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="02305-151">NOTES</span></span>

<span data-ttu-id="02305-152">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="02305-152">ALIASES</span></span>

<span data-ttu-id="02305-153">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="02305-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02305-154">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="02305-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02305-155">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02305-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02305-156">INPUTOBJECT <IMySqlIdentity> : параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="02305-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="02305-157">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="02305-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="02305-158">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="02305-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="02305-159">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="02305-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="02305-160">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="02305-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02305-161">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="02305-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="02305-162">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02305-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="02305-163">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="02305-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="02305-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="02305-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="02305-165">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="02305-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="02305-166">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="02305-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="02305-167">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="02305-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="02305-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02305-168">RELATED LINKS</span></span>

