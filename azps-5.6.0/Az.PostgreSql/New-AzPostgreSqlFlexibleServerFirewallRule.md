---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 682e0fb901e1ba40043d7251d15795247592cc3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953720"
---
# <span data-ttu-id="5da30-101">New-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5da30-101">New-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="5da30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5da30-102">SYNOPSIS</span></span>
<span data-ttu-id="5da30-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5da30-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5da30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5da30-104">SYNTAX</span></span>

### <span data-ttu-id="5da30-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5da30-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5da30-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="5da30-106">AllowAll</span></span>
```
New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5da30-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5da30-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5da30-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5da30-108">DESCRIPTION</span></span>
<span data-ttu-id="5da30-109">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5da30-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5da30-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5da30-110">EXAMPLES</span></span>

### <span data-ttu-id="5da30-111">Пример 1. Создание правила брандмауэра PostgreSql server</span><span class="sxs-lookup"><span data-stu-id="5da30-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name              StartIPAddress EndIPAddress
----------------- -------------- ------------
firewallrule-test 0.0.0.0        0.0.0.1
```

<span data-ttu-id="5da30-112">Эти cmdlets создают правило брандмауэра PostgreSql server.</span><span class="sxs-lookup"><span data-stu-id="5da30-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="5da30-113">Пример 2. Создание правила брандмауэра PostgreSql с помощью -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="5da30-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="5da30-114">Эти cmdlets создают правило брандмауэра PostgreSql с помощью -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="5da30-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="5da30-115">Пример 3. Создание правила брандмауэра PostgreSql для разрешение всех IPS</span><span class="sxs-lookup"><span data-stu-id="5da30-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="5da30-116">С помощью этих cmdlets можно создать новое правило брандмауэра PostgreSql, разрешив все IP-сообщения.</span><span class="sxs-lookup"><span data-stu-id="5da30-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="5da30-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5da30-117">PARAMETERS</span></span>

### <span data-ttu-id="5da30-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="5da30-118">-AllowAll</span></span>
<span data-ttu-id="5da30-119">Позволяет использовать все IPS диапазона от 0.0.0.0 до 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="5da30-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="5da30-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5da30-120">-AsJob</span></span>
<span data-ttu-id="5da30-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="5da30-121">Run the command as a job</span></span>

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

### <span data-ttu-id="5da30-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5da30-122">-ClientIPAddress</span></span>
<span data-ttu-id="5da30-123">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="5da30-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="5da30-124">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="5da30-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5da30-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da30-125">-DefaultProfile</span></span>
<span data-ttu-id="5da30-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5da30-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5da30-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="5da30-127">-EndIPAddress</span></span>
<span data-ttu-id="5da30-128">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="5da30-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="5da30-129">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="5da30-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5da30-130">-Name</span><span class="sxs-lookup"><span data-stu-id="5da30-130">-Name</span></span>
<span data-ttu-id="5da30-131">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="5da30-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="5da30-132">Если он не указан, значение по умолчанию не определено.</span><span class="sxs-lookup"><span data-stu-id="5da30-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="5da30-133">Если в этом случае значение AllowAll имеет значение AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="5da30-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="5da30-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5da30-134">-NoWait</span></span>
<span data-ttu-id="5da30-135">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="5da30-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5da30-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da30-136">-ResourceGroupName</span></span>
<span data-ttu-id="5da30-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5da30-137">The name of the resource group.</span></span>
<span data-ttu-id="5da30-138">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5da30-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5da30-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5da30-139">-ServerName</span></span>
<span data-ttu-id="5da30-140">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5da30-140">The name of the server.</span></span>

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

### <span data-ttu-id="5da30-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="5da30-141">-StartIPAddress</span></span>
<span data-ttu-id="5da30-142">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="5da30-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="5da30-143">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="5da30-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5da30-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5da30-144">-SubscriptionId</span></span>
<span data-ttu-id="5da30-145">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5da30-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5da30-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5da30-146">-Confirm</span></span>
<span data-ttu-id="5da30-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5da30-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5da30-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5da30-148">-WhatIf</span></span>
<span data-ttu-id="5da30-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da30-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5da30-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5da30-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5da30-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da30-151">CommonParameters</span></span>
<span data-ttu-id="5da30-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da30-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da30-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5da30-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da30-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5da30-154">INPUTS</span></span>

## <span data-ttu-id="5da30-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5da30-155">OUTPUTS</span></span>

### <span data-ttu-id="5da30-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5da30-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="5da30-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5da30-157">NOTES</span></span>

<span data-ttu-id="5da30-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5da30-158">ALIASES</span></span>

## <span data-ttu-id="5da30-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5da30-159">RELATED LINKS</span></span>

