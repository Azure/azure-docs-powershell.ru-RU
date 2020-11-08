---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247570"
---
# <span data-ttu-id="95499-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="95499-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="95499-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95499-102">SYNOPSIS</span></span>
<span data-ttu-id="95499-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="95499-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="95499-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95499-104">SYNTAX</span></span>

### <span data-ttu-id="95499-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95499-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="95499-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="95499-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="95499-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="95499-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="95499-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95499-108">DESCRIPTION</span></span>
<span data-ttu-id="95499-109">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="95499-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="95499-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95499-110">EXAMPLES</span></span>

### <span data-ttu-id="95499-111">Пример 1: Создание правила межсетевого экрана сервера PostgreSql</span><span class="sxs-lookup"><span data-stu-id="95499-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="95499-112">Эти командлеты создают правило брандмауэра сервера PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="95499-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="95499-113">Пример 2: создание нового правила брандмауэра PostgreSql с помощью ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="95499-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="95499-114">Эти командлеты создают правило брандмауэра PostgreSql с помощью ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="95499-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="95499-115">Пример 3: Создание правила брандмауэра PostgreSql, разрешающего все IP-адреса</span><span class="sxs-lookup"><span data-stu-id="95499-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="95499-116">Эти командлеты создают новое правило брандмауэра PostgreSql, разрешающее все IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="95499-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="95499-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95499-117">PARAMETERS</span></span>

### <span data-ttu-id="95499-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="95499-118">-AllowAll</span></span>
<span data-ttu-id="95499-119">Выступающий для всех диапазонов IP от 0.0.0.0 до 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="95499-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="95499-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95499-120">-AsJob</span></span>
<span data-ttu-id="95499-121">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="95499-121">Run the command as a job</span></span>

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

### <span data-ttu-id="95499-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="95499-122">-ClientIPAddress</span></span>
<span data-ttu-id="95499-123">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="95499-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="95499-124">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="95499-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="95499-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95499-125">-DefaultProfile</span></span>
<span data-ttu-id="95499-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95499-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95499-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="95499-127">-EndIPAddress</span></span>
<span data-ttu-id="95499-128">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="95499-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="95499-129">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="95499-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="95499-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95499-130">-Name</span></span>
<span data-ttu-id="95499-131">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="95499-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="95499-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="95499-132">-NoWait</span></span>
<span data-ttu-id="95499-133">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="95499-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="95499-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95499-134">-ResourceGroupName</span></span>
<span data-ttu-id="95499-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95499-135">The name of the resource group.</span></span>
<span data-ttu-id="95499-136">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="95499-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="95499-137">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="95499-137">-ServerName</span></span>
<span data-ttu-id="95499-138">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="95499-138">The name of the server.</span></span>

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

### <span data-ttu-id="95499-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="95499-139">-StartIPAddress</span></span>
<span data-ttu-id="95499-140">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="95499-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="95499-141">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="95499-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="95499-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95499-142">-SubscriptionId</span></span>
<span data-ttu-id="95499-143">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="95499-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="95499-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95499-144">-Confirm</span></span>
<span data-ttu-id="95499-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95499-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95499-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95499-146">-WhatIf</span></span>
<span data-ttu-id="95499-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95499-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95499-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95499-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95499-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95499-149">CommonParameters</span></span>
<span data-ttu-id="95499-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95499-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95499-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95499-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95499-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95499-152">INPUTS</span></span>

## <span data-ttu-id="95499-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95499-153">OUTPUTS</span></span>

### <span data-ttu-id="95499-154">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="95499-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="95499-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="95499-155">NOTES</span></span>

<span data-ttu-id="95499-156">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="95499-156">ALIASES</span></span>

## <span data-ttu-id="95499-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95499-157">RELATED LINKS</span></span>

