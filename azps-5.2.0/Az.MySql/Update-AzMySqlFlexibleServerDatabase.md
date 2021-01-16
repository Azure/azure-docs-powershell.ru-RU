---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410895"
---
# <span data-ttu-id="62507-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="62507-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="62507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62507-102">SYNOPSIS</span></span>
<span data-ttu-id="62507-103">Создает новую базу данных или обновляет существующую.</span><span class="sxs-lookup"><span data-stu-id="62507-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="62507-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62507-104">SYNTAX</span></span>

### <span data-ttu-id="62507-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62507-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62507-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="62507-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62507-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62507-107">DESCRIPTION</span></span>
<span data-ttu-id="62507-108">Создает новую базу данных или обновляет существующую.</span><span class="sxs-lookup"><span data-stu-id="62507-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="62507-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62507-109">EXAMPLES</span></span>

### <span data-ttu-id="62507-110">Пример 1. Обновление базы данных Сервера MySql по имени</span><span class="sxs-lookup"><span data-stu-id="62507-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="62507-111">Обновление базы данных по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="62507-111">Update a database by resource name.</span></span>

### <span data-ttu-id="62507-112">Пример 2. Обновление базы данных MySql с помощью параметра.</span><span class="sxs-lookup"><span data-stu-id="62507-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="62507-113">Обновление базы данных по параметрам</span><span class="sxs-lookup"><span data-stu-id="62507-113">Update a database by parameter</span></span>

## <span data-ttu-id="62507-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62507-114">PARAMETERS</span></span>

### <span data-ttu-id="62507-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62507-115">-AsJob</span></span>
<span data-ttu-id="62507-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="62507-116">Run the command as a job</span></span>

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

### <span data-ttu-id="62507-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="62507-117">-Charset</span></span>
<span data-ttu-id="62507-118">Набор данных.</span><span class="sxs-lookup"><span data-stu-id="62507-118">The charset of the database.</span></span>

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

### <span data-ttu-id="62507-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="62507-119">-Collation</span></span>
<span data-ttu-id="62507-120">Разлиновка базы данных.</span><span class="sxs-lookup"><span data-stu-id="62507-120">The collation of the database.</span></span>

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

### <span data-ttu-id="62507-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62507-121">-DefaultProfile</span></span>
<span data-ttu-id="62507-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62507-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62507-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62507-123">-InputObject</span></span>
<span data-ttu-id="62507-124">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="62507-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="62507-125">-Name</span><span class="sxs-lookup"><span data-stu-id="62507-125">-Name</span></span>
<span data-ttu-id="62507-126">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="62507-126">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62507-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="62507-127">-NoWait</span></span>
<span data-ttu-id="62507-128">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="62507-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="62507-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62507-129">-ResourceGroupName</span></span>
<span data-ttu-id="62507-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62507-130">The name of the resource group.</span></span>
<span data-ttu-id="62507-131">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="62507-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="62507-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62507-132">-ServerName</span></span>
<span data-ttu-id="62507-133">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="62507-133">The name of the server.</span></span>

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

### <span data-ttu-id="62507-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62507-134">-SubscriptionId</span></span>
<span data-ttu-id="62507-135">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="62507-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="62507-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62507-136">-Confirm</span></span>
<span data-ttu-id="62507-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="62507-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62507-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62507-138">-WhatIf</span></span>
<span data-ttu-id="62507-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62507-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62507-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62507-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62507-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62507-141">CommonParameters</span></span>
<span data-ttu-id="62507-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62507-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62507-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62507-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62507-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62507-144">INPUTS</span></span>

### <span data-ttu-id="62507-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="62507-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="62507-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62507-146">OUTPUTS</span></span>

### <span data-ttu-id="62507-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="62507-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="62507-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62507-148">NOTES</span></span>

<span data-ttu-id="62507-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="62507-149">ALIASES</span></span>

<span data-ttu-id="62507-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="62507-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62507-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="62507-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62507-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62507-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62507-153">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="62507-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="62507-154">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="62507-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="62507-155">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="62507-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="62507-156">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="62507-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="62507-157">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="62507-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="62507-158">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="62507-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="62507-159">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="62507-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="62507-160">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62507-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="62507-161">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="62507-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="62507-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="62507-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="62507-163">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="62507-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="62507-164">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="62507-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="62507-165">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="62507-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="62507-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62507-166">RELATED LINKS</span></span>

