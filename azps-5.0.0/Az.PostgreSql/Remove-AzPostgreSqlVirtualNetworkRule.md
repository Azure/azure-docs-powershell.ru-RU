---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247566"
---
# <span data-ttu-id="49e3a-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="49e3a-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="49e3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="49e3a-103">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="49e3a-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="49e3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49e3a-104">SYNTAX</span></span>

### <span data-ttu-id="49e3a-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49e3a-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="49e3a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49e3a-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49e3a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="49e3a-108">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="49e3a-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="49e3a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49e3a-109">EXAMPLES</span></span>

### <span data-ttu-id="49e3a-110">Пример 1: Удаление правила виртуальной сети PostgreSql Server по имени</span><span class="sxs-lookup"><span data-stu-id="49e3a-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="49e3a-111">Этот командлет удаляет правило виртуальной сети PostgreSql Server по имени.</span><span class="sxs-lookup"><span data-stu-id="49e3a-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="49e3a-112">Пример 2: Удаление правила виртуальной сети PostgreSql Server по удостоверению</span><span class="sxs-lookup"><span data-stu-id="49e3a-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="49e3a-113">Эти командлеты удаляют правило виртуальной сети PostgreSql Server по идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="49e3a-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="49e3a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49e3a-114">PARAMETERS</span></span>

### <span data-ttu-id="49e3a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49e3a-115">-AsJob</span></span>
<span data-ttu-id="49e3a-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="49e3a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="49e3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e3a-117">-DefaultProfile</span></span>
<span data-ttu-id="49e3a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49e3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49e3a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49e3a-119">-InputObject</span></span>
<span data-ttu-id="49e3a-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="49e3a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49e3a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49e3a-121">-Name</span></span>
<span data-ttu-id="49e3a-122">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="49e3a-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e3a-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="49e3a-123">-NoWait</span></span>
<span data-ttu-id="49e3a-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="49e3a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="49e3a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49e3a-125">-PassThru</span></span>
<span data-ttu-id="49e3a-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="49e3a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="49e3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="49e3a-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49e3a-128">The name of the resource group.</span></span>
<span data-ttu-id="49e3a-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="49e3a-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e3a-130">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="49e3a-130">-ServerName</span></span>
<span data-ttu-id="49e3a-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="49e3a-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e3a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49e3a-132">-SubscriptionId</span></span>
<span data-ttu-id="49e3a-133">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="49e3a-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e3a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49e3a-134">-Confirm</span></span>
<span data-ttu-id="49e3a-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49e3a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49e3a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49e3a-136">-WhatIf</span></span>
<span data-ttu-id="49e3a-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49e3a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49e3a-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49e3a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49e3a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e3a-139">CommonParameters</span></span>
<span data-ttu-id="49e3a-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49e3a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e3a-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49e3a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e3a-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49e3a-142">INPUTS</span></span>

### <span data-ttu-id="49e3a-143">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="49e3a-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="49e3a-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49e3a-144">OUTPUTS</span></span>

### <span data-ttu-id="49e3a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49e3a-145">System.Boolean</span></span>

## <span data-ttu-id="49e3a-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="49e3a-146">NOTES</span></span>

<span data-ttu-id="49e3a-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="49e3a-147">ALIASES</span></span>

<span data-ttu-id="49e3a-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="49e3a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49e3a-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="49e3a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49e3a-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49e3a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49e3a-151">INPUTOBJECT <IPostgreSqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="49e3a-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49e3a-152">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="49e3a-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="49e3a-153">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="49e3a-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="49e3a-154">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="49e3a-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="49e3a-155">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="49e3a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49e3a-156">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="49e3a-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="49e3a-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49e3a-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="49e3a-158">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="49e3a-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="49e3a-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="49e3a-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="49e3a-160">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="49e3a-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="49e3a-161">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="49e3a-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="49e3a-162">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="49e3a-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="49e3a-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49e3a-163">RELATED LINKS</span></span>

