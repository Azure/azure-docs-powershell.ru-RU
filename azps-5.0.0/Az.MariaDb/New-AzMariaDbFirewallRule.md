---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250098"
---
# <span data-ttu-id="a6ff9-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a6ff9-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="a6ff9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ff9-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="a6ff9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6ff9-104">SYNTAX</span></span>

### <span data-ttu-id="a6ff9-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6ff9-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6ff9-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="a6ff9-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a6ff9-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="a6ff9-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6ff9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6ff9-108">DESCRIPTION</span></span>
<span data-ttu-id="a6ff9-109">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="a6ff9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6ff9-110">EXAMPLES</span></span>

### <span data-ttu-id="a6ff9-111">Пример 1: Создание правила брандмауэра для MariaDB</span><span class="sxs-lookup"><span data-stu-id="a6ff9-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="a6ff9-112">Эта команда создает правило брандмауэра в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="a6ff9-113">Пример 2: создание нового правила брандмауэра MariaDB с помощью ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="a6ff9-114">Эти командлеты создают правило брандмауэра MariaDB с помощью ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="a6ff9-115">Пример 3: Создание правила брандмауэра MariaDB, разрешающего все IP-адреса</span><span class="sxs-lookup"><span data-stu-id="a6ff9-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="a6ff9-116">Эти командлеты создают новое правило брандмауэра MariaDB, разрешающее все IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="a6ff9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6ff9-117">PARAMETERS</span></span>

### <span data-ttu-id="a6ff9-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="a6ff9-118">-AllowAll</span></span>
<span data-ttu-id="a6ff9-119">Выступающий для всех диапазонов IP от 0.0.0.0 до 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="a6ff9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6ff9-120">-AsJob</span></span>
<span data-ttu-id="a6ff9-121">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="a6ff9-121">Run the command as a job</span></span>

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

### <span data-ttu-id="a6ff9-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="a6ff9-122">-ClientIPAddress</span></span>
<span data-ttu-id="a6ff9-123">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="a6ff9-124">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="a6ff9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ff9-125">-DefaultProfile</span></span>
<span data-ttu-id="a6ff9-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6ff9-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="a6ff9-127">-EndIPAddress</span></span>
<span data-ttu-id="a6ff9-128">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="a6ff9-129">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="a6ff9-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6ff9-130">-Name</span></span>
<span data-ttu-id="a6ff9-131">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="a6ff9-132">Если этот элемент не указан, значение по умолчанию — undefine.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="a6ff9-133">Если присутствует AllowAll, то по умолчанию используется имя AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="a6ff9-134">-Wait</span><span class="sxs-lookup"><span data-stu-id="a6ff9-134">-NoWait</span></span>
<span data-ttu-id="a6ff9-135">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="a6ff9-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6ff9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ff9-136">-ResourceGroupName</span></span>
<span data-ttu-id="a6ff9-137">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a6ff9-138">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a6ff9-139">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a6ff9-139">-ServerName</span></span>
<span data-ttu-id="a6ff9-140">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-140">The name of the server.</span></span>

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

### <span data-ttu-id="a6ff9-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="a6ff9-141">-StartIPAddress</span></span>
<span data-ttu-id="a6ff9-142">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="a6ff9-143">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="a6ff9-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6ff9-144">-SubscriptionId</span></span>
<span data-ttu-id="a6ff9-145">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a6ff9-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6ff9-146">-Confirm</span></span>
<span data-ttu-id="a6ff9-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ff9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ff9-148">-WhatIf</span></span>
<span data-ttu-id="a6ff9-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6ff9-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ff9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ff9-151">CommonParameters</span></span>
<span data-ttu-id="a6ff9-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ff9-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6ff9-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ff9-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6ff9-154">INPUTS</span></span>

## <span data-ttu-id="a6ff9-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6ff9-155">OUTPUTS</span></span>

### <span data-ttu-id="a6ff9-156">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a6ff9-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="a6ff9-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6ff9-157">NOTES</span></span>

<span data-ttu-id="a6ff9-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a6ff9-158">ALIASES</span></span>

## <span data-ttu-id="a6ff9-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6ff9-159">RELATED LINKS</span></span>
