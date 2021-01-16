---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServer.md
ms.openlocfilehash: 8e16ee1ad3a8d8b695a433af8c9194ad460c3138
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397404"
---
# <span data-ttu-id="875f5-101">Remove-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="875f5-101">Remove-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="875f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="875f5-102">SYNOPSIS</span></span>
<span data-ttu-id="875f5-103">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="875f5-103">Deletes a server.</span></span>

## <span data-ttu-id="875f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="875f5-104">SYNTAX</span></span>

### <span data-ttu-id="875f5-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="875f5-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="875f5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="875f5-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="875f5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="875f5-107">DESCRIPTION</span></span>
<span data-ttu-id="875f5-108">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="875f5-108">Deletes a server.</span></span>

## <span data-ttu-id="875f5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="875f5-109">EXAMPLES</span></span>

### <span data-ttu-id="875f5-110">Пример 1. Удаление сервера MySql по resourceGroup и имени сервера</span><span class="sxs-lookup"><span data-stu-id="875f5-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="875f5-111">Этот cmdlet removes MySql server by resourceGroup and server name.</span><span class="sxs-lookup"><span data-stu-id="875f5-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="875f5-112">Пример 2. Удаление сервера MySql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="875f5-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Remove-AzMySqlFlexibleServer -InputObject $ID
 
```

<span data-ttu-id="875f5-113">Эти cmdlets remove MySql Server by identity.</span><span class="sxs-lookup"><span data-stu-id="875f5-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="875f5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="875f5-114">PARAMETERS</span></span>

### <span data-ttu-id="875f5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="875f5-115">-AsJob</span></span>
<span data-ttu-id="875f5-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="875f5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="875f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="875f5-117">-DefaultProfile</span></span>
<span data-ttu-id="875f5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="875f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="875f5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="875f5-119">-InputObject</span></span>
<span data-ttu-id="875f5-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="875f5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="875f5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="875f5-121">-Name</span></span>
<span data-ttu-id="875f5-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="875f5-122">The name of the server.</span></span>

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

### <span data-ttu-id="875f5-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="875f5-123">-NoWait</span></span>
<span data-ttu-id="875f5-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="875f5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="875f5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="875f5-125">-PassThru</span></span>
<span data-ttu-id="875f5-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="875f5-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="875f5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="875f5-127">-ResourceGroupName</span></span>
<span data-ttu-id="875f5-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="875f5-128">The name of the resource group.</span></span>
<span data-ttu-id="875f5-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="875f5-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="875f5-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="875f5-130">-SubscriptionId</span></span>
<span data-ttu-id="875f5-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="875f5-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="875f5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="875f5-132">-Confirm</span></span>
<span data-ttu-id="875f5-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="875f5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="875f5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="875f5-134">-WhatIf</span></span>
<span data-ttu-id="875f5-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="875f5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="875f5-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="875f5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="875f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875f5-137">CommonParameters</span></span>
<span data-ttu-id="875f5-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="875f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875f5-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="875f5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875f5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="875f5-140">INPUTS</span></span>

### <span data-ttu-id="875f5-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="875f5-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="875f5-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="875f5-142">OUTPUTS</span></span>

### <span data-ttu-id="875f5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="875f5-143">System.Boolean</span></span>

## <span data-ttu-id="875f5-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="875f5-144">NOTES</span></span>

<span data-ttu-id="875f5-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="875f5-145">ALIASES</span></span>

<span data-ttu-id="875f5-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="875f5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="875f5-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="875f5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="875f5-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="875f5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="875f5-149">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="875f5-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="875f5-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="875f5-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="875f5-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="875f5-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="875f5-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="875f5-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="875f5-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="875f5-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="875f5-154">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="875f5-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="875f5-155">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="875f5-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="875f5-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="875f5-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="875f5-157">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="875f5-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="875f5-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="875f5-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="875f5-159">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="875f5-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="875f5-160">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="875f5-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="875f5-161">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="875f5-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="875f5-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="875f5-162">RELATED LINKS</span></span>

