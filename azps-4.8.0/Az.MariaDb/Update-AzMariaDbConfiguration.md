---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243526"
---
# <span data-ttu-id="c8bb7-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8bb7-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="c8bb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bb7-103">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="c8bb7-104">Используйте Update-AzMariaDbServer, если хотите обновить AdministratorLoginPassword, SKU и т. д.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="c8bb7-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8bb7-105">SYNTAX</span></span>

### <span data-ttu-id="c8bb7-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8bb7-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c8bb7-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c8bb7-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8bb7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8bb7-108">DESCRIPTION</span></span>
<span data-ttu-id="c8bb7-109">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="c8bb7-110">Используйте Update-AzMariaDberver, если хотите обновить AdministratorLoginPassword, SKU и т. д.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="c8bb7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8bb7-111">EXAMPLES</span></span>

### <span data-ttu-id="c8bb7-112">Пример 1: Обновление конфигурации MariaDB</span><span class="sxs-lookup"><span data-stu-id="c8bb7-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="c8bb7-113">Эта команда обновляет конфигурацию MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="c8bb7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8bb7-114">PARAMETERS</span></span>

### <span data-ttu-id="c8bb7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8bb7-115">-AsJob</span></span>
<span data-ttu-id="c8bb7-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c8bb7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c8bb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bb7-117">-DefaultProfile</span></span>
<span data-ttu-id="c8bb7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8bb7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8bb7-119">-InputObject</span></span>
<span data-ttu-id="c8bb7-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bb7-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8bb7-121">-Name</span></span>
<span data-ttu-id="c8bb7-122">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="c8bb7-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="c8bb7-123">-NoWait</span></span>
<span data-ttu-id="c8bb7-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="c8bb7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c8bb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8bb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="c8bb7-126">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c8bb7-127">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c8bb7-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c8bb7-128">-ServerName</span></span>
<span data-ttu-id="c8bb7-129">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-129">The name of the server.</span></span>

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

### <span data-ttu-id="c8bb7-130">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="c8bb7-130">-Source</span></span>
<span data-ttu-id="c8bb7-131">Источник конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="c8bb7-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8bb7-132">-SubscriptionId</span></span>
<span data-ttu-id="c8bb7-133">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c8bb7-134">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="c8bb7-134">-Value</span></span>
<span data-ttu-id="c8bb7-135">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="c8bb7-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8bb7-136">-Confirm</span></span>
<span data-ttu-id="c8bb7-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8bb7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8bb7-138">-WhatIf</span></span>
<span data-ttu-id="c8bb7-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8bb7-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8bb7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bb7-141">CommonParameters</span></span>
<span data-ttu-id="c8bb7-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bb7-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8bb7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bb7-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8bb7-144">INPUTS</span></span>

### <span data-ttu-id="c8bb7-145">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="c8bb7-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="c8bb7-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8bb7-146">OUTPUTS</span></span>

### <span data-ttu-id="c8bb7-147">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8bb7-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="c8bb7-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8bb7-148">NOTES</span></span>

<span data-ttu-id="c8bb7-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c8bb7-149">ALIASES</span></span>

<span data-ttu-id="c8bb7-150">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c8bb7-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8bb7-151">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8bb7-152">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8bb7-153">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="c8bb7-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8bb7-154">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c8bb7-155">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c8bb7-156">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c8bb7-157">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="c8bb7-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8bb7-158">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c8bb7-159">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c8bb7-160">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c8bb7-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c8bb7-162">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c8bb7-163">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="c8bb7-164">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c8bb7-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8bb7-165">RELATED LINKS</span></span>

