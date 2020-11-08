---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: 86cc2a249479807adc14ad0faa4c682d1fef4725
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248397"
---
# <span data-ttu-id="9486c-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="9486c-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="9486c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9486c-102">SYNOPSIS</span></span>
<span data-ttu-id="9486c-103">Удаление сервера.</span><span class="sxs-lookup"><span data-stu-id="9486c-103">Deletes a server.</span></span>

## <span data-ttu-id="9486c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9486c-104">SYNTAX</span></span>

### <span data-ttu-id="9486c-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9486c-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9486c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9486c-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9486c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9486c-107">DESCRIPTION</span></span>
<span data-ttu-id="9486c-108">Удаление сервера.</span><span class="sxs-lookup"><span data-stu-id="9486c-108">Deletes a server.</span></span>

## <span data-ttu-id="9486c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9486c-109">EXAMPLES</span></span>

### <span data-ttu-id="9486c-110">Пример 1: Удаление сервера MySql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="9486c-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="9486c-111">Этот командлет удаляет сервер MySql по группе resourceGroup и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="9486c-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="9486c-112">Пример 2: Удаление сервера MySql по удостоверению</span><span class="sxs-lookup"><span data-stu-id="9486c-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="9486c-113">Эти командлеты удаляют сервер MySql по идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="9486c-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="9486c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9486c-114">PARAMETERS</span></span>

### <span data-ttu-id="9486c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9486c-115">-AsJob</span></span>
<span data-ttu-id="9486c-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9486c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9486c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9486c-117">-DefaultProfile</span></span>
<span data-ttu-id="9486c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9486c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9486c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9486c-119">-InputObject</span></span>
<span data-ttu-id="9486c-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9486c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9486c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9486c-121">-Name</span></span>
<span data-ttu-id="9486c-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9486c-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9486c-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="9486c-123">-NoWait</span></span>
<span data-ttu-id="9486c-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="9486c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9486c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9486c-125">-PassThru</span></span>
<span data-ttu-id="9486c-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9486c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9486c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9486c-127">-ResourceGroupName</span></span>
<span data-ttu-id="9486c-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9486c-128">The name of the resource group.</span></span>
<span data-ttu-id="9486c-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9486c-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9486c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9486c-130">-SubscriptionId</span></span>
<span data-ttu-id="9486c-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9486c-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9486c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9486c-132">-Confirm</span></span>
<span data-ttu-id="9486c-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9486c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9486c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9486c-134">-WhatIf</span></span>
<span data-ttu-id="9486c-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9486c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9486c-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9486c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9486c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9486c-137">CommonParameters</span></span>
<span data-ttu-id="9486c-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9486c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9486c-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9486c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9486c-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9486c-140">INPUTS</span></span>

### <span data-ttu-id="9486c-141">Microsoft. Azure. PowerShell. командлеты. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9486c-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9486c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9486c-142">OUTPUTS</span></span>

### <span data-ttu-id="9486c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9486c-143">System.Boolean</span></span>

## <span data-ttu-id="9486c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9486c-144">NOTES</span></span>

<span data-ttu-id="9486c-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9486c-145">ALIASES</span></span>

<span data-ttu-id="9486c-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9486c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9486c-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9486c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9486c-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9486c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9486c-149">INPUTOBJECT <IMySqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="9486c-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9486c-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="9486c-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9486c-151">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9486c-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9486c-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="9486c-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9486c-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="9486c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9486c-154">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="9486c-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9486c-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9486c-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9486c-156">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9486c-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="9486c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="9486c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9486c-158">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9486c-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9486c-159">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9486c-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9486c-160">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9486c-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9486c-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9486c-161">RELATED LINKS</span></span>

