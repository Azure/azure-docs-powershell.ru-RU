---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234811"
---
# <span data-ttu-id="6512d-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6512d-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="6512d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6512d-102">SYNOPSIS</span></span>
<span data-ttu-id="6512d-103">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="6512d-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="6512d-104">Используйте Update-AzPostgreSqlServer, если хотите обновить AdministratorLoginPassword, SKU и т. д.</span><span class="sxs-lookup"><span data-stu-id="6512d-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6512d-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6512d-105">SYNTAX</span></span>

### <span data-ttu-id="6512d-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6512d-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6512d-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6512d-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6512d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6512d-108">DESCRIPTION</span></span>
<span data-ttu-id="6512d-109">Обновляет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="6512d-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="6512d-110">Используйте Update-AzPostgreSqlServer, если хотите обновить AdministratorLoginPassword, SKU и т. д.</span><span class="sxs-lookup"><span data-stu-id="6512d-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6512d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6512d-111">EXAMPLES</span></span>

### <span data-ttu-id="6512d-112">Пример 1: Обновление конфигурации PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="6512d-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="6512d-113">Этот командлет обновляет конфигурацию PostgreSql по имени.</span><span class="sxs-lookup"><span data-stu-id="6512d-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="6512d-114">Пример 2: Обновление конфигурации PostgreSql по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="6512d-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="6512d-115">Эти командлеты обновляют конфигурацию PostgreSql по идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="6512d-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="6512d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6512d-116">PARAMETERS</span></span>

### <span data-ttu-id="6512d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6512d-117">-AsJob</span></span>
<span data-ttu-id="6512d-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="6512d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6512d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6512d-119">-DefaultProfile</span></span>
<span data-ttu-id="6512d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6512d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6512d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6512d-121">-InputObject</span></span>
<span data-ttu-id="6512d-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="6512d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6512d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6512d-123">-Name</span></span>
<span data-ttu-id="6512d-124">Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="6512d-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="6512d-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="6512d-125">-NoWait</span></span>
<span data-ttu-id="6512d-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="6512d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6512d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6512d-127">-ResourceGroupName</span></span>
<span data-ttu-id="6512d-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6512d-128">The name of the resource group.</span></span>
<span data-ttu-id="6512d-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6512d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6512d-130">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6512d-130">-ServerName</span></span>
<span data-ttu-id="6512d-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6512d-131">The name of the server.</span></span>

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

### <span data-ttu-id="6512d-132">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="6512d-132">-Source</span></span>
<span data-ttu-id="6512d-133">Источник конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6512d-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="6512d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6512d-134">-SubscriptionId</span></span>
<span data-ttu-id="6512d-135">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6512d-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6512d-136">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="6512d-136">-Value</span></span>
<span data-ttu-id="6512d-137">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6512d-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="6512d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6512d-138">-Confirm</span></span>
<span data-ttu-id="6512d-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6512d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6512d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6512d-140">-WhatIf</span></span>
<span data-ttu-id="6512d-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6512d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6512d-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6512d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6512d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6512d-143">CommonParameters</span></span>
<span data-ttu-id="6512d-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6512d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6512d-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6512d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6512d-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6512d-146">INPUTS</span></span>

### <span data-ttu-id="6512d-147">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6512d-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6512d-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6512d-148">OUTPUTS</span></span>

### <span data-ttu-id="6512d-149">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="6512d-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="6512d-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="6512d-150">NOTES</span></span>

<span data-ttu-id="6512d-151">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="6512d-151">ALIASES</span></span>

<span data-ttu-id="6512d-152">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6512d-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6512d-153">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6512d-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6512d-154">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6512d-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6512d-155">INPUTOBJECT <IPostgreSqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="6512d-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6512d-156">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="6512d-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6512d-157">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="6512d-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6512d-158">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="6512d-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6512d-159">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="6512d-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6512d-160">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="6512d-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6512d-161">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6512d-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6512d-162">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6512d-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="6512d-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6512d-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6512d-164">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6512d-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6512d-165">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6512d-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6512d-166">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6512d-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6512d-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6512d-167">RELATED LINKS</span></span>

