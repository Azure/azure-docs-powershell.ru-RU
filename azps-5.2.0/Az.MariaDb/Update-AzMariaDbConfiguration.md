---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415175"
---
# <span data-ttu-id="d2c65-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2c65-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="d2c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c65-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c65-103">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="d2c65-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="d2c65-104">Используйте Update-AzMariaDbServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="d2c65-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="d2c65-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2c65-105">SYNTAX</span></span>

### <span data-ttu-id="d2c65-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2c65-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2c65-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d2c65-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2c65-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2c65-108">DESCRIPTION</span></span>
<span data-ttu-id="d2c65-109">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="d2c65-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="d2c65-110">Используйте Update-AzMariaDberver если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="d2c65-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="d2c65-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2c65-111">EXAMPLES</span></span>

### <span data-ttu-id="d2c65-112">Пример 1. Обновление конфигурации MariaDB</span><span class="sxs-lookup"><span data-stu-id="d2c65-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="d2c65-113">Эта команда обновляет конфигурацию MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d2c65-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="d2c65-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2c65-114">PARAMETERS</span></span>

### <span data-ttu-id="d2c65-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2c65-115">-AsJob</span></span>
<span data-ttu-id="d2c65-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d2c65-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d2c65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c65-117">-DefaultProfile</span></span>
<span data-ttu-id="d2c65-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c65-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2c65-119">-InputObject</span></span>
<span data-ttu-id="d2c65-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d2c65-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2c65-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d2c65-121">-Name</span></span>
<span data-ttu-id="d2c65-122">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d2c65-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="d2c65-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d2c65-123">-NoWait</span></span>
<span data-ttu-id="d2c65-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="d2c65-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2c65-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c65-125">-ResourceGroupName</span></span>
<span data-ttu-id="d2c65-126">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="d2c65-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d2c65-127">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d2c65-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d2c65-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d2c65-128">-ServerName</span></span>
<span data-ttu-id="d2c65-129">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d2c65-129">The name of the server.</span></span>

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

### <span data-ttu-id="d2c65-130">-Source</span><span class="sxs-lookup"><span data-stu-id="d2c65-130">-Source</span></span>
<span data-ttu-id="d2c65-131">Источник конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d2c65-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="d2c65-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2c65-132">-SubscriptionId</span></span>
<span data-ttu-id="d2c65-133">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c65-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d2c65-134">-Value</span><span class="sxs-lookup"><span data-stu-id="d2c65-134">-Value</span></span>
<span data-ttu-id="d2c65-135">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d2c65-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="d2c65-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2c65-136">-Confirm</span></span>
<span data-ttu-id="d2c65-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c65-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c65-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c65-138">-WhatIf</span></span>
<span data-ttu-id="d2c65-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c65-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2c65-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d2c65-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c65-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c65-141">CommonParameters</span></span>
<span data-ttu-id="d2c65-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c65-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c65-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2c65-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c65-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2c65-144">INPUTS</span></span>

### <span data-ttu-id="d2c65-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d2c65-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d2c65-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2c65-146">OUTPUTS</span></span>

### <span data-ttu-id="d2c65-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2c65-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="d2c65-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2c65-148">NOTES</span></span>

<span data-ttu-id="d2c65-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d2c65-149">ALIASES</span></span>

<span data-ttu-id="d2c65-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d2c65-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2c65-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d2c65-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2c65-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2c65-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2c65-153">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d2c65-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2c65-154">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d2c65-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d2c65-155">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d2c65-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d2c65-156">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d2c65-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d2c65-157">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d2c65-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2c65-158">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="d2c65-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d2c65-159">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="d2c65-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d2c65-160">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d2c65-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d2c65-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d2c65-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d2c65-162">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d2c65-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d2c65-163">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c65-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d2c65-164">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="d2c65-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d2c65-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2c65-165">RELATED LINKS</span></span>

