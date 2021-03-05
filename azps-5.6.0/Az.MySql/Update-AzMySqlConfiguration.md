---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: bff7f24ef88c8f6fc5022aae019a9c6f32bf95f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968803"
---
# <span data-ttu-id="61e2b-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="61e2b-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="61e2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="61e2b-103">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="61e2b-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="61e2b-104">Используйте Update-AzMySqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="61e2b-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="61e2b-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61e2b-105">SYNTAX</span></span>

### <span data-ttu-id="61e2b-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61e2b-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="61e2b-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="61e2b-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="61e2b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61e2b-108">DESCRIPTION</span></span>
<span data-ttu-id="61e2b-109">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="61e2b-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="61e2b-110">Используйте Update-AzMySqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="61e2b-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="61e2b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61e2b-111">EXAMPLES</span></span>

### <span data-ttu-id="61e2b-112">Пример 1. Обновление конфигурации MySql по имени</span><span class="sxs-lookup"><span data-stu-id="61e2b-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="61e2b-113">Этот cmdlet обновляет конфигурацию MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="61e2b-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="61e2b-114">Пример 2. Обновление конфигурации MySql с помощью удостоверения.</span><span class="sxs-lookup"><span data-stu-id="61e2b-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="61e2b-115">Эти cmdlets обновляют конфигурацию MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="61e2b-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="61e2b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61e2b-116">PARAMETERS</span></span>

### <span data-ttu-id="61e2b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61e2b-117">-AsJob</span></span>
<span data-ttu-id="61e2b-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="61e2b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="61e2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e2b-119">-DefaultProfile</span></span>
<span data-ttu-id="61e2b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61e2b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e2b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61e2b-121">-InputObject</span></span>
<span data-ttu-id="61e2b-122">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="61e2b-122">Identity Parameter.</span></span>
<span data-ttu-id="61e2b-123">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="61e2b-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="61e2b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="61e2b-124">-Name</span></span>
<span data-ttu-id="61e2b-125">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="61e2b-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="61e2b-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="61e2b-126">-NoWait</span></span>
<span data-ttu-id="61e2b-127">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="61e2b-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="61e2b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e2b-128">-ResourceGroupName</span></span>
<span data-ttu-id="61e2b-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61e2b-129">The name of the resource group.</span></span>
<span data-ttu-id="61e2b-130">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="61e2b-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="61e2b-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="61e2b-131">-ServerName</span></span>
<span data-ttu-id="61e2b-132">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="61e2b-132">The name of the server.</span></span>

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

### <span data-ttu-id="61e2b-133">-Source</span><span class="sxs-lookup"><span data-stu-id="61e2b-133">-Source</span></span>
<span data-ttu-id="61e2b-134">Источник конфигурации.</span><span class="sxs-lookup"><span data-stu-id="61e2b-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="61e2b-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61e2b-135">-SubscriptionId</span></span>
<span data-ttu-id="61e2b-136">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="61e2b-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="61e2b-137">-Value</span><span class="sxs-lookup"><span data-stu-id="61e2b-137">-Value</span></span>
<span data-ttu-id="61e2b-138">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="61e2b-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="61e2b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61e2b-139">-Confirm</span></span>
<span data-ttu-id="61e2b-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61e2b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e2b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e2b-141">-WhatIf</span></span>
<span data-ttu-id="61e2b-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61e2b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61e2b-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61e2b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61e2b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e2b-144">CommonParameters</span></span>
<span data-ttu-id="61e2b-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e2b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e2b-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61e2b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e2b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61e2b-147">INPUTS</span></span>

### <span data-ttu-id="61e2b-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="61e2b-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="61e2b-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61e2b-149">OUTPUTS</span></span>

### <span data-ttu-id="61e2b-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="61e2b-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="61e2b-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61e2b-151">NOTES</span></span>

<span data-ttu-id="61e2b-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="61e2b-152">ALIASES</span></span>

<span data-ttu-id="61e2b-153">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="61e2b-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61e2b-154">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="61e2b-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61e2b-155">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="61e2b-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61e2b-156">INPUTOBJECT <IMySqlIdentity> : Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="61e2b-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="61e2b-157">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="61e2b-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="61e2b-158">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="61e2b-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="61e2b-159">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="61e2b-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="61e2b-160">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="61e2b-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61e2b-161">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="61e2b-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="61e2b-162">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="61e2b-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="61e2b-163">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61e2b-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="61e2b-164">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="61e2b-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="61e2b-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="61e2b-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="61e2b-166">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="61e2b-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="61e2b-167">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="61e2b-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="61e2b-168">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="61e2b-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="61e2b-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61e2b-169">RELATED LINKS</span></span>

