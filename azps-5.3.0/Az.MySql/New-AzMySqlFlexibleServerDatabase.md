---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422564"
---
# <span data-ttu-id="dd329-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="dd329-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="dd329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd329-102">SYNOPSIS</span></span>
<span data-ttu-id="dd329-103">Создает новую базу данных или обновляет существующую.</span><span class="sxs-lookup"><span data-stu-id="dd329-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="dd329-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd329-104">SYNTAX</span></span>

### <span data-ttu-id="dd329-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd329-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd329-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dd329-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd329-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd329-107">DESCRIPTION</span></span>
<span data-ttu-id="dd329-108">Создает новую базу данных или обновляет существующую.</span><span class="sxs-lookup"><span data-stu-id="dd329-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="dd329-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd329-109">EXAMPLES</span></span>

### <span data-ttu-id="dd329-110">Пример 1. Создание базы данных сервера MySql</span><span class="sxs-lookup"><span data-stu-id="dd329-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="dd329-111">Создание базы данных с настройками по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dd329-111">Create a database with default settings.</span></span>

## <span data-ttu-id="dd329-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd329-112">PARAMETERS</span></span>

### <span data-ttu-id="dd329-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd329-113">-AsJob</span></span>
<span data-ttu-id="dd329-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="dd329-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dd329-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="dd329-115">-Charset</span></span>
<span data-ttu-id="dd329-116">Набор данных.</span><span class="sxs-lookup"><span data-stu-id="dd329-116">The charset of the database.</span></span>

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

### <span data-ttu-id="dd329-117">-Collation</span><span class="sxs-lookup"><span data-stu-id="dd329-117">-Collation</span></span>
<span data-ttu-id="dd329-118">Разлиновка базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd329-118">The collation of the database.</span></span>

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

### <span data-ttu-id="dd329-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd329-119">-DefaultProfile</span></span>
<span data-ttu-id="dd329-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd329-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd329-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd329-121">-InputObject</span></span>
<span data-ttu-id="dd329-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="dd329-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd329-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dd329-123">-Name</span></span>
<span data-ttu-id="dd329-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd329-124">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd329-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dd329-125">-NoWait</span></span>
<span data-ttu-id="dd329-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="dd329-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dd329-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd329-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd329-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd329-128">The name of the resource group.</span></span>
<span data-ttu-id="dd329-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="dd329-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd329-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dd329-130">-ServerName</span></span>
<span data-ttu-id="dd329-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="dd329-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd329-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd329-132">-SubscriptionId</span></span>
<span data-ttu-id="dd329-133">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="dd329-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd329-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd329-134">-Confirm</span></span>
<span data-ttu-id="dd329-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd329-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd329-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd329-136">-WhatIf</span></span>
<span data-ttu-id="dd329-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd329-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd329-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dd329-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd329-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd329-139">CommonParameters</span></span>
<span data-ttu-id="dd329-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd329-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd329-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd329-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd329-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd329-142">INPUTS</span></span>

### <span data-ttu-id="dd329-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="dd329-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="dd329-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd329-144">OUTPUTS</span></span>

### <span data-ttu-id="dd329-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="dd329-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="dd329-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd329-146">NOTES</span></span>

<span data-ttu-id="dd329-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dd329-147">ALIASES</span></span>

<span data-ttu-id="dd329-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dd329-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd329-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="dd329-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd329-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd329-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd329-151">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="dd329-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd329-152">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="dd329-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dd329-153">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd329-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dd329-154">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="dd329-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dd329-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="dd329-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd329-156">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="dd329-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="dd329-157">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="dd329-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dd329-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd329-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dd329-159">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="dd329-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="dd329-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="dd329-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dd329-161">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="dd329-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dd329-162">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="dd329-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dd329-163">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="dd329-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dd329-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd329-164">RELATED LINKS</span></span>

