---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391895"
---
# <span data-ttu-id="95a49-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="95a49-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="95a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95a49-102">SYNOPSIS</span></span>
<span data-ttu-id="95a49-103">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="95a49-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="95a49-104">Используйте Update-AzPostgreSqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="95a49-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="95a49-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95a49-105">SYNTAX</span></span>

### <span data-ttu-id="95a49-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95a49-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="95a49-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="95a49-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="95a49-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95a49-108">DESCRIPTION</span></span>
<span data-ttu-id="95a49-109">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="95a49-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="95a49-110">Используйте Update-AzPostgreSqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.</span><span class="sxs-lookup"><span data-stu-id="95a49-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="95a49-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95a49-111">EXAMPLES</span></span>

### <span data-ttu-id="95a49-112">Пример 1. Обновление конфигурации PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="95a49-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="95a49-113">Этот cmdlet обновляет конфигурацию PostgreSql по имени.</span><span class="sxs-lookup"><span data-stu-id="95a49-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="95a49-114">Пример 2. Обновление конфигурации PostgreSql с помощью удостоверения.</span><span class="sxs-lookup"><span data-stu-id="95a49-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="95a49-115">Эти cmdlets update PostgreSql configuration by identity.</span><span class="sxs-lookup"><span data-stu-id="95a49-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="95a49-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95a49-116">PARAMETERS</span></span>

### <span data-ttu-id="95a49-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95a49-117">-AsJob</span></span>
<span data-ttu-id="95a49-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="95a49-118">Run the command as a job</span></span>

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

### <span data-ttu-id="95a49-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a49-119">-DefaultProfile</span></span>
<span data-ttu-id="95a49-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95a49-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95a49-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95a49-121">-InputObject</span></span>
<span data-ttu-id="95a49-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="95a49-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95a49-123">-Name</span><span class="sxs-lookup"><span data-stu-id="95a49-123">-Name</span></span>
<span data-ttu-id="95a49-124">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="95a49-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="95a49-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="95a49-125">-NoWait</span></span>
<span data-ttu-id="95a49-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="95a49-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="95a49-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a49-127">-ResourceGroupName</span></span>
<span data-ttu-id="95a49-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95a49-128">The name of the resource group.</span></span>
<span data-ttu-id="95a49-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="95a49-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="95a49-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="95a49-130">-ServerName</span></span>
<span data-ttu-id="95a49-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="95a49-131">The name of the server.</span></span>

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

### <span data-ttu-id="95a49-132">-Source</span><span class="sxs-lookup"><span data-stu-id="95a49-132">-Source</span></span>
<span data-ttu-id="95a49-133">Источник конфигурации.</span><span class="sxs-lookup"><span data-stu-id="95a49-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="95a49-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95a49-134">-SubscriptionId</span></span>
<span data-ttu-id="95a49-135">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="95a49-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="95a49-136">-Value</span><span class="sxs-lookup"><span data-stu-id="95a49-136">-Value</span></span>
<span data-ttu-id="95a49-137">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="95a49-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="95a49-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95a49-138">-Confirm</span></span>
<span data-ttu-id="95a49-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="95a49-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a49-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a49-140">-WhatIf</span></span>
<span data-ttu-id="95a49-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95a49-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95a49-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="95a49-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a49-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a49-143">CommonParameters</span></span>
<span data-ttu-id="95a49-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a49-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a49-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95a49-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a49-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95a49-146">INPUTS</span></span>

### <span data-ttu-id="95a49-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="95a49-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="95a49-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95a49-148">OUTPUTS</span></span>

### <span data-ttu-id="95a49-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="95a49-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="95a49-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95a49-150">NOTES</span></span>

<span data-ttu-id="95a49-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="95a49-151">ALIASES</span></span>

<span data-ttu-id="95a49-152">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="95a49-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="95a49-153">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="95a49-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="95a49-154">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="95a49-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="95a49-155">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="95a49-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="95a49-156">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="95a49-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="95a49-157">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="95a49-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="95a49-158">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="95a49-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="95a49-159">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="95a49-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="95a49-160">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="95a49-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="95a49-161">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95a49-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="95a49-162">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="95a49-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="95a49-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="95a49-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="95a49-164">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="95a49-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="95a49-165">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="95a49-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="95a49-166">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="95a49-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="95a49-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95a49-167">RELATED LINKS</span></span>

