---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: 6c7576023e4902caacd204edc97feba0a378f63b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410927"
---
# <span data-ttu-id="18cde-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="18cde-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="18cde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18cde-102">SYNOPSIS</span></span>
<span data-ttu-id="18cde-103">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="18cde-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="18cde-104">Используйте Update-AzMySqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="18cde-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="18cde-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18cde-105">SYNTAX</span></span>

### <span data-ttu-id="18cde-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18cde-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18cde-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="18cde-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18cde-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18cde-108">DESCRIPTION</span></span>
<span data-ttu-id="18cde-109">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="18cde-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="18cde-110">Используйте Update-AzMySqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="18cde-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="18cde-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18cde-111">EXAMPLES</span></span>

### <span data-ttu-id="18cde-112">Пример 1. Обновление конфигурации MySql по имени</span><span class="sxs-lookup"><span data-stu-id="18cde-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="18cde-113">Этот cmdlet обновляет конфигурацию MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="18cde-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="18cde-114">Пример 2. Обновление конфигурации MySql с помощью удостоверения.</span><span class="sxs-lookup"><span data-stu-id="18cde-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="18cde-115">Эти cmdlets обновляют конфигурацию MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="18cde-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="18cde-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18cde-116">PARAMETERS</span></span>

### <span data-ttu-id="18cde-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18cde-117">-AsJob</span></span>
<span data-ttu-id="18cde-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="18cde-118">Run the command as a job</span></span>

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

### <span data-ttu-id="18cde-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cde-119">-DefaultProfile</span></span>
<span data-ttu-id="18cde-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18cde-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18cde-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18cde-121">-InputObject</span></span>
<span data-ttu-id="18cde-122">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="18cde-122">Identity Parameter.</span></span>
<span data-ttu-id="18cde-123">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="18cde-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="18cde-124">-Name</span><span class="sxs-lookup"><span data-stu-id="18cde-124">-Name</span></span>
<span data-ttu-id="18cde-125">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="18cde-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="18cde-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="18cde-126">-NoWait</span></span>
<span data-ttu-id="18cde-127">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="18cde-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="18cde-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18cde-128">-ResourceGroupName</span></span>
<span data-ttu-id="18cde-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18cde-129">The name of the resource group.</span></span>
<span data-ttu-id="18cde-130">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="18cde-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="18cde-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="18cde-131">-ServerName</span></span>
<span data-ttu-id="18cde-132">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="18cde-132">The name of the server.</span></span>

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

### <span data-ttu-id="18cde-133">-Source</span><span class="sxs-lookup"><span data-stu-id="18cde-133">-Source</span></span>
<span data-ttu-id="18cde-134">Источник конфигурации.</span><span class="sxs-lookup"><span data-stu-id="18cde-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="18cde-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18cde-135">-SubscriptionId</span></span>
<span data-ttu-id="18cde-136">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="18cde-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="18cde-137">-Value</span><span class="sxs-lookup"><span data-stu-id="18cde-137">-Value</span></span>
<span data-ttu-id="18cde-138">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="18cde-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="18cde-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18cde-139">-Confirm</span></span>
<span data-ttu-id="18cde-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18cde-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18cde-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18cde-141">-WhatIf</span></span>
<span data-ttu-id="18cde-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18cde-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18cde-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="18cde-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18cde-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cde-144">CommonParameters</span></span>
<span data-ttu-id="18cde-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18cde-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cde-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18cde-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cde-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18cde-147">INPUTS</span></span>

### <span data-ttu-id="18cde-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="18cde-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="18cde-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18cde-149">OUTPUTS</span></span>

### <span data-ttu-id="18cde-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="18cde-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="18cde-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18cde-151">NOTES</span></span>

<span data-ttu-id="18cde-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="18cde-152">ALIASES</span></span>

<span data-ttu-id="18cde-153">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="18cde-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18cde-154">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="18cde-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18cde-155">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18cde-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18cde-156">INPUTOBJECT <IMySqlIdentity> : Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="18cde-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="18cde-157">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="18cde-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="18cde-158">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="18cde-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="18cde-159">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="18cde-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="18cde-160">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="18cde-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18cde-161">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="18cde-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="18cde-162">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="18cde-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="18cde-163">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18cde-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="18cde-164">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="18cde-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="18cde-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="18cde-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="18cde-166">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="18cde-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="18cde-167">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="18cde-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="18cde-168">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="18cde-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="18cde-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18cde-169">RELATED LINKS</span></span>

