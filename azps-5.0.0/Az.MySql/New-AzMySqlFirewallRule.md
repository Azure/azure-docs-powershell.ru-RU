---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 036628943afc8b2c5f07b30f2db14f27229364c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250019"
---
# <span data-ttu-id="c7c90-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c7c90-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="c7c90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7c90-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c90-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c7c90-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c7c90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7c90-104">SYNTAX</span></span>

### <span data-ttu-id="c7c90-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7c90-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7c90-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="c7c90-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c7c90-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7c90-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7c90-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7c90-108">DESCRIPTION</span></span>
<span data-ttu-id="c7c90-109">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c7c90-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c7c90-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7c90-110">EXAMPLES</span></span>

### <span data-ttu-id="c7c90-111">Пример 1: Создание правила межсетевого экрана сервера MySql</span><span class="sxs-lookup"><span data-stu-id="c7c90-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="c7c90-112">Эти командлеты создают правило брандмауэра сервера MySql.</span><span class="sxs-lookup"><span data-stu-id="c7c90-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="c7c90-113">Пример 2. Создайте новое правило брандмауэра MySql с помощью функции-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="c7c90-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="c7c90-114">Эти командлеты создают правило брандмауэра MySql с помощью функции-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="c7c90-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="c7c90-115">Пример 3: создание нового правила брандмауэра MySql для разрешения всех IP-адресов</span><span class="sxs-lookup"><span data-stu-id="c7c90-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="c7c90-116">Эти командлеты создают новое правило брандмауэра MySql для разрешения всех IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c7c90-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="c7c90-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7c90-117">PARAMETERS</span></span>

### <span data-ttu-id="c7c90-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="c7c90-118">-AllowAll</span></span>
<span data-ttu-id="c7c90-119">Выступающий для всех диапазонов IP от 0.0.0.0 до 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="c7c90-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="c7c90-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7c90-120">-AsJob</span></span>
<span data-ttu-id="c7c90-121">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c7c90-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c7c90-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7c90-122">-ClientIPAddress</span></span>
<span data-ttu-id="c7c90-123">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="c7c90-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="c7c90-124">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="c7c90-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c7c90-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c90-125">-DefaultProfile</span></span>
<span data-ttu-id="c7c90-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c90-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c90-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7c90-127">-EndIPAddress</span></span>
<span data-ttu-id="c7c90-128">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="c7c90-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="c7c90-129">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="c7c90-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c7c90-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7c90-130">-Name</span></span>
<span data-ttu-id="c7c90-131">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="c7c90-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="c7c90-132">Если этот элемент не указан, значение по умолчанию — undefine.</span><span class="sxs-lookup"><span data-stu-id="c7c90-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="c7c90-133">Если присутствует AllowAll, то по умолчанию используется имя AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="c7c90-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="c7c90-134">-Wait</span><span class="sxs-lookup"><span data-stu-id="c7c90-134">-NoWait</span></span>
<span data-ttu-id="c7c90-135">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="c7c90-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c7c90-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7c90-136">-ResourceGroupName</span></span>
<span data-ttu-id="c7c90-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7c90-137">The name of the resource group.</span></span>
<span data-ttu-id="c7c90-138">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c7c90-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c7c90-139">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c7c90-139">-ServerName</span></span>
<span data-ttu-id="c7c90-140">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="c7c90-140">The name of the server.</span></span>

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

### <span data-ttu-id="c7c90-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7c90-141">-StartIPAddress</span></span>
<span data-ttu-id="c7c90-142">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="c7c90-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="c7c90-143">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="c7c90-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c7c90-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7c90-144">-SubscriptionId</span></span>
<span data-ttu-id="c7c90-145">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c7c90-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c7c90-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7c90-146">-Confirm</span></span>
<span data-ttu-id="c7c90-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7c90-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7c90-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7c90-148">-WhatIf</span></span>
<span data-ttu-id="c7c90-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7c90-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7c90-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7c90-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7c90-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c90-151">CommonParameters</span></span>
<span data-ttu-id="c7c90-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7c90-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c90-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7c90-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c90-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7c90-154">INPUTS</span></span>

## <span data-ttu-id="c7c90-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7c90-155">OUTPUTS</span></span>

### <span data-ttu-id="c7c90-156">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c7c90-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="c7c90-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7c90-157">NOTES</span></span>

<span data-ttu-id="c7c90-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c7c90-158">ALIASES</span></span>

## <span data-ttu-id="c7c90-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7c90-159">RELATED LINKS</span></span>

