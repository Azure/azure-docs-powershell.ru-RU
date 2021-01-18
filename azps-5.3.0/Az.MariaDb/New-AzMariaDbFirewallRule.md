---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507139"
---
# <span data-ttu-id="f7b26-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f7b26-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="f7b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7b26-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b26-103">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f7b26-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f7b26-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7b26-104">SYNTAX</span></span>

### <span data-ttu-id="f7b26-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7b26-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f7b26-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="f7b26-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f7b26-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f7b26-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7b26-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7b26-108">DESCRIPTION</span></span>
<span data-ttu-id="f7b26-109">Создает новое правило брандмауэра или обновляет существующее правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f7b26-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f7b26-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7b26-110">EXAMPLES</span></span>

### <span data-ttu-id="f7b26-111">Пример 1. Создание правила брандмауэра для MariaDB</span><span class="sxs-lookup"><span data-stu-id="f7b26-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="f7b26-112">Эта команда создает правило брандмауэра для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f7b26-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="f7b26-113">Пример 2. Создание правила брандмауэра MariaDB с помощью -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="f7b26-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="f7b26-114">Эти cmdlets создают правило брандмауэра MariaDB с помощью -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="f7b26-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="f7b26-115">Пример 3. Создание нового правила брандмауэра MariaDB для разрешение всех IPS</span><span class="sxs-lookup"><span data-stu-id="f7b26-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="f7b26-116">С помощью этих рабочих буклетов можно создать новое правило брандмауэра MariaDB, разрешив все IPs.</span><span class="sxs-lookup"><span data-stu-id="f7b26-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="f7b26-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7b26-117">PARAMETERS</span></span>

### <span data-ttu-id="f7b26-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="f7b26-118">-AllowAll</span></span>
<span data-ttu-id="f7b26-119">Позволяет использовать все IPS диапазона от 0.0.0.0 до 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="f7b26-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="f7b26-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7b26-120">-AsJob</span></span>
<span data-ttu-id="f7b26-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f7b26-121">Run the command as a job</span></span>

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

### <span data-ttu-id="f7b26-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f7b26-122">-ClientIPAddress</span></span>
<span data-ttu-id="f7b26-123">Клиент указал один IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f7b26-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="f7b26-124">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="f7b26-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f7b26-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b26-125">-DefaultProfile</span></span>
<span data-ttu-id="f7b26-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b26-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7b26-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="f7b26-127">-EndIPAddress</span></span>
<span data-ttu-id="f7b26-128">Конечный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f7b26-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="f7b26-129">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="f7b26-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f7b26-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f7b26-130">-Name</span></span>
<span data-ttu-id="f7b26-131">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f7b26-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="f7b26-132">Если он не указан, значение по умолчанию не определено.</span><span class="sxs-lookup"><span data-stu-id="f7b26-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="f7b26-133">Если в этом случае значение AllowAll имеет значение AllowAll_yyyy-DD_HH-мм-сс.</span><span class="sxs-lookup"><span data-stu-id="f7b26-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="f7b26-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f7b26-134">-NoWait</span></span>
<span data-ttu-id="f7b26-135">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="f7b26-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f7b26-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b26-136">-ResourceGroupName</span></span>
<span data-ttu-id="f7b26-137">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="f7b26-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f7b26-138">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="f7b26-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f7b26-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f7b26-139">-ServerName</span></span>
<span data-ttu-id="f7b26-140">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f7b26-140">The name of the server.</span></span>

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

### <span data-ttu-id="f7b26-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="f7b26-141">-StartIPAddress</span></span>
<span data-ttu-id="f7b26-142">Начальный IP-адрес правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="f7b26-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="f7b26-143">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="f7b26-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f7b26-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7b26-144">-SubscriptionId</span></span>
<span data-ttu-id="f7b26-145">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b26-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f7b26-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7b26-146">-Confirm</span></span>
<span data-ttu-id="f7b26-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f7b26-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b26-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b26-148">-WhatIf</span></span>
<span data-ttu-id="f7b26-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b26-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b26-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f7b26-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b26-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b26-151">CommonParameters</span></span>
<span data-ttu-id="f7b26-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b26-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b26-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7b26-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b26-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7b26-154">INPUTS</span></span>

## <span data-ttu-id="f7b26-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7b26-155">OUTPUTS</span></span>

### <span data-ttu-id="f7b26-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f7b26-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="f7b26-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7b26-157">NOTES</span></span>

<span data-ttu-id="f7b26-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f7b26-158">ALIASES</span></span>

## <span data-ttu-id="f7b26-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7b26-159">RELATED LINKS</span></span>

