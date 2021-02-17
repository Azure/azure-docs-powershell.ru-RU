---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: 6c7576023e4902caacd204edc97feba0a378f63b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226148"
---
# <span data-ttu-id="4afa1-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4afa1-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="4afa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4afa1-102">SYNOPSIS</span></span>
<span data-ttu-id="4afa1-103">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="4afa1-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="4afa1-104">Используйте Update-AzMySqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="4afa1-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4afa1-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4afa1-105">SYNTAX</span></span>

### <span data-ttu-id="4afa1-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4afa1-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4afa1-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4afa1-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4afa1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4afa1-108">DESCRIPTION</span></span>
<span data-ttu-id="4afa1-109">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="4afa1-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="4afa1-110">Используйте Update-AzMySqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="4afa1-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4afa1-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4afa1-111">EXAMPLES</span></span>

### <span data-ttu-id="4afa1-112">Пример 1. Обновление конфигурации MySql по имени</span><span class="sxs-lookup"><span data-stu-id="4afa1-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="4afa1-113">Этот cmdlet обновляет конфигурацию MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="4afa1-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="4afa1-114">Пример 2. Обновление конфигурации MySql с помощью удостоверения.</span><span class="sxs-lookup"><span data-stu-id="4afa1-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="4afa1-115">Эти cmdlets обновляют конфигурацию MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="4afa1-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="4afa1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4afa1-116">PARAMETERS</span></span>

### <span data-ttu-id="4afa1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4afa1-117">-AsJob</span></span>
<span data-ttu-id="4afa1-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4afa1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="4afa1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afa1-119">-DefaultProfile</span></span>
<span data-ttu-id="4afa1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4afa1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4afa1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4afa1-121">-InputObject</span></span>
<span data-ttu-id="4afa1-122">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="4afa1-122">Identity Parameter.</span></span>
<span data-ttu-id="4afa1-123">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="4afa1-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4afa1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4afa1-124">-Name</span></span>
<span data-ttu-id="4afa1-125">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="4afa1-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="4afa1-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4afa1-126">-NoWait</span></span>
<span data-ttu-id="4afa1-127">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="4afa1-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4afa1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4afa1-128">-ResourceGroupName</span></span>
<span data-ttu-id="4afa1-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4afa1-129">The name of the resource group.</span></span>
<span data-ttu-id="4afa1-130">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="4afa1-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4afa1-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4afa1-131">-ServerName</span></span>
<span data-ttu-id="4afa1-132">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4afa1-132">The name of the server.</span></span>

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

### <span data-ttu-id="4afa1-133">-Source</span><span class="sxs-lookup"><span data-stu-id="4afa1-133">-Source</span></span>
<span data-ttu-id="4afa1-134">Источник конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4afa1-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="4afa1-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4afa1-135">-SubscriptionId</span></span>
<span data-ttu-id="4afa1-136">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="4afa1-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4afa1-137">-Value</span><span class="sxs-lookup"><span data-stu-id="4afa1-137">-Value</span></span>
<span data-ttu-id="4afa1-138">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4afa1-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="4afa1-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4afa1-139">-Confirm</span></span>
<span data-ttu-id="4afa1-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4afa1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4afa1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4afa1-141">-WhatIf</span></span>
<span data-ttu-id="4afa1-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4afa1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4afa1-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4afa1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4afa1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afa1-144">CommonParameters</span></span>
<span data-ttu-id="4afa1-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4afa1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afa1-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4afa1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afa1-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4afa1-147">INPUTS</span></span>

### <span data-ttu-id="4afa1-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4afa1-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4afa1-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4afa1-149">OUTPUTS</span></span>

### <span data-ttu-id="4afa1-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="4afa1-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="4afa1-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4afa1-151">NOTES</span></span>

<span data-ttu-id="4afa1-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4afa1-152">ALIASES</span></span>

<span data-ttu-id="4afa1-153">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4afa1-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4afa1-154">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4afa1-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4afa1-155">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4afa1-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4afa1-156">INPUTOBJECT <IMySqlIdentity> : Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="4afa1-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="4afa1-157">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="4afa1-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4afa1-158">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="4afa1-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4afa1-159">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="4afa1-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4afa1-160">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="4afa1-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4afa1-161">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="4afa1-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="4afa1-162">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="4afa1-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4afa1-163">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4afa1-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4afa1-164">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="4afa1-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="4afa1-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="4afa1-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4afa1-166">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4afa1-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4afa1-167">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="4afa1-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4afa1-168">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="4afa1-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4afa1-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4afa1-169">RELATED LINKS</span></span>

