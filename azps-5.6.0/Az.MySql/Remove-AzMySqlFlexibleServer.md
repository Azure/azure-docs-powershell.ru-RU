---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/remove-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServer.md
ms.openlocfilehash: 963303b921e29d117dba27077e561d4bb4413fda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962808"
---
# <span data-ttu-id="b5ecc-101">Remove-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="b5ecc-101">Remove-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="b5ecc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ecc-103">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-103">Deletes a server.</span></span>

## <span data-ttu-id="b5ecc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b5ecc-104">SYNTAX</span></span>

### <span data-ttu-id="b5ecc-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5ecc-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b5ecc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b5ecc-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5ecc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5ecc-107">DESCRIPTION</span></span>
<span data-ttu-id="b5ecc-108">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-108">Deletes a server.</span></span>

## <span data-ttu-id="b5ecc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b5ecc-109">EXAMPLES</span></span>

### <span data-ttu-id="b5ecc-110">Пример 1. Удаление сервера MySql по resourceGroup и имени сервера</span><span class="sxs-lookup"><span data-stu-id="b5ecc-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="b5ecc-111">Этот cmdlet removes MySql server by resourceGroup and server name.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="b5ecc-112">Пример 2. Удаление сервера MySql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="b5ecc-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Remove-AzMySqlFlexibleServer -InputObject $ID
 
```

<span data-ttu-id="b5ecc-113">Эти cmdlets remove MySql Server by identity.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="b5ecc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5ecc-114">PARAMETERS</span></span>

### <span data-ttu-id="b5ecc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5ecc-115">-AsJob</span></span>
<span data-ttu-id="b5ecc-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b5ecc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b5ecc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ecc-117">-DefaultProfile</span></span>
<span data-ttu-id="b5ecc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ecc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5ecc-119">-InputObject</span></span>
<span data-ttu-id="b5ecc-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b5ecc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b5ecc-121">-Name</span></span>
<span data-ttu-id="b5ecc-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-122">The name of the server.</span></span>

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

### <span data-ttu-id="b5ecc-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b5ecc-123">-NoWait</span></span>
<span data-ttu-id="b5ecc-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="b5ecc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b5ecc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5ecc-125">-PassThru</span></span>
<span data-ttu-id="b5ecc-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b5ecc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ecc-127">-ResourceGroupName</span></span>
<span data-ttu-id="b5ecc-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-128">The name of the resource group.</span></span>
<span data-ttu-id="b5ecc-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b5ecc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5ecc-130">-SubscriptionId</span></span>
<span data-ttu-id="b5ecc-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b5ecc-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5ecc-132">-Confirm</span></span>
<span data-ttu-id="b5ecc-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ecc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ecc-134">-WhatIf</span></span>
<span data-ttu-id="b5ecc-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ecc-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ecc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ecc-137">CommonParameters</span></span>
<span data-ttu-id="b5ecc-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ecc-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5ecc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ecc-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5ecc-140">INPUTS</span></span>

### <span data-ttu-id="b5ecc-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b5ecc-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b5ecc-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5ecc-142">OUTPUTS</span></span>

### <span data-ttu-id="b5ecc-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5ecc-143">System.Boolean</span></span>

## <span data-ttu-id="b5ecc-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b5ecc-144">NOTES</span></span>

<span data-ttu-id="b5ecc-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b5ecc-145">ALIASES</span></span>

<span data-ttu-id="b5ecc-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b5ecc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5ecc-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5ecc-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5ecc-149">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b5ecc-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5ecc-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b5ecc-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b5ecc-152">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b5ecc-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b5ecc-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5ecc-154">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b5ecc-155">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b5ecc-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b5ecc-157">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="b5ecc-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b5ecc-159">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b5ecc-160">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b5ecc-161">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="b5ecc-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b5ecc-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5ecc-162">RELATED LINKS</span></span>

