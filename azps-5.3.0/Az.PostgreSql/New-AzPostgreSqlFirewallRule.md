---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421308"
---
# <span data-ttu-id="6f098-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6f098-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="6f098-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f098-102">SYNOPSIS</span></span>
<span data-ttu-id="6f098-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="6f098-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6f098-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f098-104">SYNTAX</span></span>

### <span data-ttu-id="6f098-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f098-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6f098-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="6f098-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6f098-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6f098-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6f098-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f098-108">DESCRIPTION</span></span>
<span data-ttu-id="6f098-109">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="6f098-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6f098-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f098-110">EXAMPLES</span></span>

### <span data-ttu-id="6f098-111">Пример 1. Создание правила брандмауэра PostgreSql server</span><span class="sxs-lookup"><span data-stu-id="6f098-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="6f098-112">Эти cmdlets создают правило брандмауэра PostgreSql server.</span><span class="sxs-lookup"><span data-stu-id="6f098-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="6f098-113">Пример 2. Создание правила брандмауэра PostgreSql с помощью -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6f098-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="6f098-114">Эти cmdlets создают правило брандмауэра PostgreSql с помощью -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6f098-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="6f098-115">Пример 3. Создание правила брандмауэра PostgreSql для разрешение всех IPS</span><span class="sxs-lookup"><span data-stu-id="6f098-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="6f098-116">С помощью этих cmdlets можно создать новое правило брандмауэра PostgreSql, разрешив все IP-сообщения.</span><span class="sxs-lookup"><span data-stu-id="6f098-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="6f098-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f098-117">PARAMETERS</span></span>

### <span data-ttu-id="6f098-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="6f098-118">-AllowAll</span></span>
<span data-ttu-id="6f098-119">Позволяет использовать все IPS диапазона от 0.0.0.0 до 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="6f098-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="6f098-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f098-120">-AsJob</span></span>
<span data-ttu-id="6f098-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="6f098-121">Run the command as a job</span></span>

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

### <span data-ttu-id="6f098-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6f098-122">-ClientIPAddress</span></span>
<span data-ttu-id="6f098-123">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="6f098-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="6f098-124">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="6f098-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6f098-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f098-125">-DefaultProfile</span></span>
<span data-ttu-id="6f098-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f098-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f098-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="6f098-127">-EndIPAddress</span></span>
<span data-ttu-id="6f098-128">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="6f098-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="6f098-129">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="6f098-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6f098-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6f098-130">-Name</span></span>
<span data-ttu-id="6f098-131">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="6f098-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="6f098-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6f098-132">-NoWait</span></span>
<span data-ttu-id="6f098-133">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="6f098-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6f098-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f098-134">-ResourceGroupName</span></span>
<span data-ttu-id="6f098-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f098-135">The name of the resource group.</span></span>
<span data-ttu-id="6f098-136">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="6f098-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6f098-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f098-137">-ServerName</span></span>
<span data-ttu-id="6f098-138">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6f098-138">The name of the server.</span></span>

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

### <span data-ttu-id="6f098-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="6f098-139">-StartIPAddress</span></span>
<span data-ttu-id="6f098-140">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="6f098-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="6f098-141">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="6f098-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6f098-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f098-142">-SubscriptionId</span></span>
<span data-ttu-id="6f098-143">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6f098-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6f098-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f098-144">-Confirm</span></span>
<span data-ttu-id="6f098-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6f098-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f098-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f098-146">-WhatIf</span></span>
<span data-ttu-id="6f098-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f098-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f098-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6f098-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f098-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f098-149">CommonParameters</span></span>
<span data-ttu-id="6f098-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f098-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f098-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f098-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f098-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f098-152">INPUTS</span></span>

## <span data-ttu-id="6f098-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f098-153">OUTPUTS</span></span>

### <span data-ttu-id="6f098-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6f098-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="6f098-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f098-155">NOTES</span></span>

<span data-ttu-id="6f098-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6f098-156">ALIASES</span></span>

## <span data-ttu-id="6f098-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f098-157">RELATED LINKS</span></span>

