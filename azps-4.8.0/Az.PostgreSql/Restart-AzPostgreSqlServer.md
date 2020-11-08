---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234815"
---
# <span data-ttu-id="12f17-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="12f17-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="12f17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12f17-102">SYNOPSIS</span></span>
<span data-ttu-id="12f17-103">Перезапускает сервер.</span><span class="sxs-lookup"><span data-stu-id="12f17-103">Restarts a server.</span></span>

## <span data-ttu-id="12f17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12f17-104">SYNTAX</span></span>

### <span data-ttu-id="12f17-105">Перезагрузка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="12f17-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12f17-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12f17-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12f17-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12f17-107">DESCRIPTION</span></span>
<span data-ttu-id="12f17-108">Перезапускает сервер.</span><span class="sxs-lookup"><span data-stu-id="12f17-108">Restarts a server.</span></span>

## <span data-ttu-id="12f17-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12f17-109">EXAMPLES</span></span>

### <span data-ttu-id="12f17-110">Пример 1: перезапуск сервера PostgreSql с помощью группы ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="12f17-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="12f17-111">Этот командлет перезапускает сервер PostgreSql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="12f17-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="12f17-112">Пример 2: перезапуск сервера PostgreSql по удостоверению</span><span class="sxs-lookup"><span data-stu-id="12f17-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="12f17-113">Эти командлеты перезапускают сервер PostgreSql по идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="12f17-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="12f17-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12f17-114">PARAMETERS</span></span>

### <span data-ttu-id="12f17-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12f17-115">-AsJob</span></span>
<span data-ttu-id="12f17-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="12f17-116">Run the command as a job</span></span>

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

### <span data-ttu-id="12f17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f17-117">-DefaultProfile</span></span>
<span data-ttu-id="12f17-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12f17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f17-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12f17-119">-InputObject</span></span>
<span data-ttu-id="12f17-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="12f17-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12f17-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12f17-121">-Name</span></span>
<span data-ttu-id="12f17-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="12f17-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f17-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="12f17-123">-NoWait</span></span>
<span data-ttu-id="12f17-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="12f17-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12f17-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12f17-125">-PassThru</span></span>
<span data-ttu-id="12f17-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="12f17-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="12f17-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12f17-127">-ResourceGroupName</span></span>
<span data-ttu-id="12f17-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12f17-128">The name of the resource group.</span></span>
<span data-ttu-id="12f17-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="12f17-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f17-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12f17-130">-SubscriptionId</span></span>
<span data-ttu-id="12f17-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="12f17-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f17-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12f17-132">-Confirm</span></span>
<span data-ttu-id="12f17-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12f17-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12f17-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12f17-134">-WhatIf</span></span>
<span data-ttu-id="12f17-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12f17-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12f17-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12f17-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12f17-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f17-137">CommonParameters</span></span>
<span data-ttu-id="12f17-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12f17-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f17-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12f17-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f17-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12f17-140">INPUTS</span></span>

### <span data-ttu-id="12f17-141">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="12f17-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="12f17-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12f17-142">OUTPUTS</span></span>

### <span data-ttu-id="12f17-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12f17-143">System.Boolean</span></span>

## <span data-ttu-id="12f17-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="12f17-144">NOTES</span></span>

<span data-ttu-id="12f17-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="12f17-145">ALIASES</span></span>

<span data-ttu-id="12f17-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="12f17-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12f17-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="12f17-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12f17-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12f17-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12f17-149">INPUTOBJECT <IPostgreSqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="12f17-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12f17-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="12f17-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="12f17-151">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="12f17-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="12f17-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="12f17-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="12f17-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="12f17-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12f17-154">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="12f17-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="12f17-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12f17-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="12f17-156">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="12f17-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="12f17-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="12f17-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="12f17-158">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="12f17-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="12f17-159">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="12f17-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="12f17-160">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="12f17-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="12f17-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12f17-161">RELATED LINKS</span></span>

