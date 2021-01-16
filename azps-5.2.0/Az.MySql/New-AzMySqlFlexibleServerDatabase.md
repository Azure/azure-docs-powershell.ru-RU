---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394876"
---
# <span data-ttu-id="2bbf9-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="2bbf9-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="2bbf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bbf9-102">SYNOPSIS</span></span>
<span data-ttu-id="2bbf9-103">Создает новую базу данных или обновляет существующую.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2bbf9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2bbf9-104">SYNTAX</span></span>

### <span data-ttu-id="2bbf9-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2bbf9-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2bbf9-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2bbf9-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2bbf9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bbf9-107">DESCRIPTION</span></span>
<span data-ttu-id="2bbf9-108">Создает новую базу данных или обновляет существующую.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2bbf9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2bbf9-109">EXAMPLES</span></span>

### <span data-ttu-id="2bbf9-110">Пример 1. Создание базы данных Сервера MySql</span><span class="sxs-lookup"><span data-stu-id="2bbf9-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="2bbf9-111">Создание базы данных с настройками по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-111">Create a database with default settings.</span></span>

## <span data-ttu-id="2bbf9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bbf9-112">PARAMETERS</span></span>

### <span data-ttu-id="2bbf9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bbf9-113">-AsJob</span></span>
<span data-ttu-id="2bbf9-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="2bbf9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2bbf9-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="2bbf9-115">-Charset</span></span>
<span data-ttu-id="2bbf9-116">Набор данных.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-116">The charset of the database.</span></span>

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

### <span data-ttu-id="2bbf9-117">-Collation</span><span class="sxs-lookup"><span data-stu-id="2bbf9-117">-Collation</span></span>
<span data-ttu-id="2bbf9-118">Разлиновка базы данных.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-118">The collation of the database.</span></span>

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

### <span data-ttu-id="2bbf9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bbf9-119">-DefaultProfile</span></span>
<span data-ttu-id="2bbf9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bbf9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bbf9-121">-InputObject</span></span>
<span data-ttu-id="2bbf9-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2bbf9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2bbf9-123">-Name</span></span>
<span data-ttu-id="2bbf9-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-124">The name of the database.</span></span>

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

### <span data-ttu-id="2bbf9-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2bbf9-125">-NoWait</span></span>
<span data-ttu-id="2bbf9-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="2bbf9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2bbf9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bbf9-127">-ResourceGroupName</span></span>
<span data-ttu-id="2bbf9-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-128">The name of the resource group.</span></span>
<span data-ttu-id="2bbf9-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2bbf9-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2bbf9-130">-ServerName</span></span>
<span data-ttu-id="2bbf9-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-131">The name of the server.</span></span>

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

### <span data-ttu-id="2bbf9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2bbf9-132">-SubscriptionId</span></span>
<span data-ttu-id="2bbf9-133">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2bbf9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2bbf9-134">-Confirm</span></span>
<span data-ttu-id="2bbf9-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bbf9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bbf9-136">-WhatIf</span></span>
<span data-ttu-id="2bbf9-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bbf9-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bbf9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbf9-139">CommonParameters</span></span>
<span data-ttu-id="2bbf9-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbf9-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bbf9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbf9-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bbf9-142">INPUTS</span></span>

### <span data-ttu-id="2bbf9-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2bbf9-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2bbf9-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2bbf9-144">OUTPUTS</span></span>

### <span data-ttu-id="2bbf9-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="2bbf9-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="2bbf9-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2bbf9-146">NOTES</span></span>

<span data-ttu-id="2bbf9-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2bbf9-147">ALIASES</span></span>

<span data-ttu-id="2bbf9-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="2bbf9-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2bbf9-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2bbf9-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2bbf9-151">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="2bbf9-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2bbf9-152">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2bbf9-153">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2bbf9-154">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2bbf9-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="2bbf9-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2bbf9-156">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2bbf9-157">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2bbf9-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2bbf9-159">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="2bbf9-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2bbf9-161">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2bbf9-162">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2bbf9-163">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="2bbf9-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2bbf9-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bbf9-164">RELATED LINKS</span></span>

