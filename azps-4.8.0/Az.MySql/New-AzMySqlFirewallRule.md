---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 036628943afc8b2c5f07b30f2db14f27229364c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236253"
---
# <span data-ttu-id="3f10c-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3f10c-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="3f10c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f10c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f10c-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3f10c-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3f10c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f10c-104">SYNTAX</span></span>

### <span data-ttu-id="3f10c-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f10c-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f10c-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="3f10c-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3f10c-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3f10c-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f10c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f10c-108">DESCRIPTION</span></span>
<span data-ttu-id="3f10c-109">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3f10c-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3f10c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f10c-110">EXAMPLES</span></span>

### <span data-ttu-id="3f10c-111">Пример 1: Создание правила межсетевого экрана сервера MySql</span><span class="sxs-lookup"><span data-stu-id="3f10c-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="3f10c-112">Эти командлеты создают правило брандмауэра сервера MySql.</span><span class="sxs-lookup"><span data-stu-id="3f10c-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="3f10c-113">Пример 2. Создайте новое правило брандмауэра MySql с помощью функции-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="3f10c-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="3f10c-114">Эти командлеты создают правило брандмауэра MySql с помощью функции-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="3f10c-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="3f10c-115">Пример 3: создание нового правила брандмауэра MySql для разрешения всех IP-адресов</span><span class="sxs-lookup"><span data-stu-id="3f10c-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="3f10c-116">Эти командлеты создают новое правило брандмауэра MySql для разрешения всех IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3f10c-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="3f10c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f10c-117">PARAMETERS</span></span>

### <span data-ttu-id="3f10c-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="3f10c-118">-AllowAll</span></span>
<span data-ttu-id="3f10c-119">Выступающий для всех диапазонов IP от 0.0.0.0 до 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="3f10c-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="3f10c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f10c-120">-AsJob</span></span>
<span data-ttu-id="3f10c-121">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3f10c-121">Run the command as a job</span></span>

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

### <span data-ttu-id="3f10c-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3f10c-122">-ClientIPAddress</span></span>
<span data-ttu-id="3f10c-123">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3f10c-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="3f10c-124">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="3f10c-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3f10c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f10c-125">-DefaultProfile</span></span>
<span data-ttu-id="3f10c-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f10c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f10c-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="3f10c-127">-EndIPAddress</span></span>
<span data-ttu-id="3f10c-128">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3f10c-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="3f10c-129">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="3f10c-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3f10c-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f10c-130">-Name</span></span>
<span data-ttu-id="3f10c-131">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3f10c-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="3f10c-132">Если этот элемент не указан, значение по умолчанию — undefine.</span><span class="sxs-lookup"><span data-stu-id="3f10c-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="3f10c-133">Если присутствует AllowAll, то по умолчанию используется имя AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="3f10c-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="3f10c-134">-Wait</span><span class="sxs-lookup"><span data-stu-id="3f10c-134">-NoWait</span></span>
<span data-ttu-id="3f10c-135">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="3f10c-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f10c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f10c-136">-ResourceGroupName</span></span>
<span data-ttu-id="3f10c-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f10c-137">The name of the resource group.</span></span>
<span data-ttu-id="3f10c-138">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="3f10c-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3f10c-139">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3f10c-139">-ServerName</span></span>
<span data-ttu-id="3f10c-140">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3f10c-140">The name of the server.</span></span>

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

### <span data-ttu-id="3f10c-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="3f10c-141">-StartIPAddress</span></span>
<span data-ttu-id="3f10c-142">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3f10c-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="3f10c-143">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="3f10c-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3f10c-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f10c-144">-SubscriptionId</span></span>
<span data-ttu-id="3f10c-145">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="3f10c-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3f10c-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f10c-146">-Confirm</span></span>
<span data-ttu-id="3f10c-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f10c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f10c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f10c-148">-WhatIf</span></span>
<span data-ttu-id="3f10c-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f10c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f10c-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f10c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f10c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f10c-151">CommonParameters</span></span>
<span data-ttu-id="3f10c-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f10c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f10c-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f10c-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f10c-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f10c-154">INPUTS</span></span>

## <span data-ttu-id="3f10c-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f10c-155">OUTPUTS</span></span>

### <span data-ttu-id="3f10c-156">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3f10c-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="3f10c-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f10c-157">NOTES</span></span>

<span data-ttu-id="3f10c-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3f10c-158">ALIASES</span></span>

## <span data-ttu-id="3f10c-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f10c-159">RELATED LINKS</span></span>

