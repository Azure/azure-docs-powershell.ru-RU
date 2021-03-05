---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: e06447fc72dc8dc3bc09768360039a561b1b862a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995445"
---
# <span data-ttu-id="d78c9-101">New-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d78c9-101">New-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="d78c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d78c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d78c9-103">Создание правила брандмауэра для гибкого сервера MySQL</span><span class="sxs-lookup"><span data-stu-id="d78c9-103">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="d78c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d78c9-104">SYNTAX</span></span>

### <span data-ttu-id="d78c9-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d78c9-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d78c9-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="d78c9-106">AllowAll</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d78c9-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d78c9-107">ClientIPAddress</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d78c9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d78c9-108">DESCRIPTION</span></span>
<span data-ttu-id="d78c9-109">Создание правила брандмауэра для гибкого сервера MySQL</span><span class="sxs-lookup"><span data-stu-id="d78c9-109">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="d78c9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d78c9-110">EXAMPLES</span></span>

### <span data-ttu-id="d78c9-111">Пример 1. Создание нового правила брандмауэра MySql Server</span><span class="sxs-lookup"><span data-stu-id="d78c9-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name              StartIPAddress EndIPAddress
----------------- -------------- ------------
firewallrule-test 0.0.0.0        0.0.0.1
```

<span data-ttu-id="d78c9-112">Эти cmdlets создают правило брандмауэра MySql Server.</span><span class="sxs-lookup"><span data-stu-id="d78c9-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="d78c9-113">Пример 2. Создание правила брандмауэра MySql с помощью -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d78c9-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="d78c9-114">Эти cmdlets создают правило брандмауэра MySql с помощью -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="d78c9-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="d78c9-115">Пример 3. Создание правила брандмауэра MySql для разрешение всех IPS</span><span class="sxs-lookup"><span data-stu-id="d78c9-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="d78c9-116">Эти cmdlets создают новое правило брандмауэра MySql, разрешая все IPs.</span><span class="sxs-lookup"><span data-stu-id="d78c9-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="d78c9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d78c9-117">PARAMETERS</span></span>

### <span data-ttu-id="d78c9-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="d78c9-118">-AllowAll</span></span>
<span data-ttu-id="d78c9-119">Позволяет использовать все IPS диапазона от 0.0.0.0 до 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="d78c9-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d78c9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d78c9-120">-AsJob</span></span>
<span data-ttu-id="d78c9-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d78c9-121">Run the command as a job</span></span>

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

### <span data-ttu-id="d78c9-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d78c9-122">-ClientIPAddress</span></span>
<span data-ttu-id="d78c9-123">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d78c9-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="d78c9-124">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="d78c9-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d78c9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78c9-125">-DefaultProfile</span></span>
<span data-ttu-id="d78c9-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d78c9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d78c9-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="d78c9-127">-EndIPAddress</span></span>
<span data-ttu-id="d78c9-128">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d78c9-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="d78c9-129">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="d78c9-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d78c9-130">-Name</span><span class="sxs-lookup"><span data-stu-id="d78c9-130">-Name</span></span>
<span data-ttu-id="d78c9-131">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d78c9-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="d78c9-132">Если он не указан, значение по умолчанию не определено.</span><span class="sxs-lookup"><span data-stu-id="d78c9-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="d78c9-133">Если в этом случае значение AllowAll имеет значение AllowAll_yyyy-DD_HH-мм-сс.</span><span class="sxs-lookup"><span data-stu-id="d78c9-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d78c9-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d78c9-134">-NoWait</span></span>
<span data-ttu-id="d78c9-135">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="d78c9-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d78c9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d78c9-136">-ResourceGroupName</span></span>
<span data-ttu-id="d78c9-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d78c9-137">The name of the resource group.</span></span>
<span data-ttu-id="d78c9-138">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d78c9-138">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d78c9-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d78c9-139">-ServerName</span></span>
<span data-ttu-id="d78c9-140">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d78c9-140">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d78c9-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d78c9-141">-StartIPAddress</span></span>
<span data-ttu-id="d78c9-142">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d78c9-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="d78c9-143">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="d78c9-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d78c9-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d78c9-144">-SubscriptionId</span></span>
<span data-ttu-id="d78c9-145">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d78c9-145">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d78c9-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d78c9-146">-Confirm</span></span>
<span data-ttu-id="d78c9-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d78c9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d78c9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d78c9-148">-WhatIf</span></span>
<span data-ttu-id="d78c9-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d78c9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d78c9-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d78c9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d78c9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78c9-151">CommonParameters</span></span>
<span data-ttu-id="d78c9-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d78c9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78c9-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d78c9-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78c9-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d78c9-154">INPUTS</span></span>

## <span data-ttu-id="d78c9-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d78c9-155">OUTPUTS</span></span>

### <span data-ttu-id="d78c9-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d78c9-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="d78c9-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d78c9-157">NOTES</span></span>

<span data-ttu-id="d78c9-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d78c9-158">ALIASES</span></span>

## <span data-ttu-id="d78c9-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d78c9-159">RELATED LINKS</span></span>

