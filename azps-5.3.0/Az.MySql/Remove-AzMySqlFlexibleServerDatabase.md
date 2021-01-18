---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 656fbdc012f4e6de5f80c88a20cde42a49244618
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505043"
---
# <span data-ttu-id="13547-101">Remove-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="13547-101">Remove-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="13547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13547-102">SYNOPSIS</span></span>
<span data-ttu-id="13547-103">Удаляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="13547-103">Deletes a database.</span></span>

## <span data-ttu-id="13547-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="13547-104">SYNTAX</span></span>

### <span data-ttu-id="13547-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13547-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="13547-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="13547-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13547-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13547-107">DESCRIPTION</span></span>
<span data-ttu-id="13547-108">Удаляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="13547-108">Deletes a database.</span></span>

## <span data-ttu-id="13547-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="13547-109">EXAMPLES</span></span>

### <span data-ttu-id="13547-110">Пример 1. Удаление базы данных MySql по имени</span><span class="sxs-lookup"><span data-stu-id="13547-110">Example 1: Remove MySql database by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
```

<span data-ttu-id="13547-111">Этот cmdlet удаляет базу данных MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="13547-111">This cmdlet removes MySql database by name.</span></span>

### <span data-ttu-id="13547-112">Пример 2. Удаление базы данных MySql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="13547-112">Example 2: Remove MySql database by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/databases/databasetest"
PS C:\> Remove-AzMySqlFlexibleServerDatabase -InputObject $ID
 
```

<span data-ttu-id="13547-113">Эти cmdlets remove MySql database by identity.</span><span class="sxs-lookup"><span data-stu-id="13547-113">These cmdlets remove MySql database by identity.</span></span>

## <span data-ttu-id="13547-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13547-114">PARAMETERS</span></span>

### <span data-ttu-id="13547-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13547-115">-AsJob</span></span>
<span data-ttu-id="13547-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="13547-116">Run the command as a job</span></span>

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

### <span data-ttu-id="13547-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13547-117">-DefaultProfile</span></span>
<span data-ttu-id="13547-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13547-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13547-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13547-119">-InputObject</span></span>
<span data-ttu-id="13547-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="13547-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="13547-121">-Name</span><span class="sxs-lookup"><span data-stu-id="13547-121">-Name</span></span>
<span data-ttu-id="13547-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="13547-122">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13547-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="13547-123">-NoWait</span></span>
<span data-ttu-id="13547-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="13547-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13547-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13547-125">-PassThru</span></span>
<span data-ttu-id="13547-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="13547-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="13547-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13547-127">-ResourceGroupName</span></span>
<span data-ttu-id="13547-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13547-128">The name of the resource group.</span></span>
<span data-ttu-id="13547-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="13547-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="13547-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="13547-130">-ServerName</span></span>
<span data-ttu-id="13547-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="13547-131">The name of the server.</span></span>

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

### <span data-ttu-id="13547-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13547-132">-SubscriptionId</span></span>
<span data-ttu-id="13547-133">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="13547-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="13547-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13547-134">-Confirm</span></span>
<span data-ttu-id="13547-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="13547-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13547-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13547-136">-WhatIf</span></span>
<span data-ttu-id="13547-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13547-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13547-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="13547-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13547-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13547-139">CommonParameters</span></span>
<span data-ttu-id="13547-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13547-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13547-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13547-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13547-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13547-142">INPUTS</span></span>

### <span data-ttu-id="13547-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="13547-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="13547-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="13547-144">OUTPUTS</span></span>

### <span data-ttu-id="13547-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="13547-145">System.Boolean</span></span>

## <span data-ttu-id="13547-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="13547-146">NOTES</span></span>

<span data-ttu-id="13547-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="13547-147">ALIASES</span></span>

<span data-ttu-id="13547-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="13547-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13547-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="13547-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13547-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13547-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13547-151">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="13547-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13547-152">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="13547-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="13547-153">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="13547-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="13547-154">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="13547-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="13547-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="13547-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13547-156">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="13547-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="13547-157">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="13547-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="13547-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13547-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="13547-159">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="13547-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="13547-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="13547-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="13547-161">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="13547-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="13547-162">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="13547-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="13547-163">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="13547-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="13547-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13547-164">RELATED LINKS</span></span>

