---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078172"
---
# <span data-ttu-id="62e2d-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="62e2d-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="62e2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="62e2d-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="62e2d-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="62e2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62e2d-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62e2d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62e2d-105">DESCRIPTION</span></span>
<span data-ttu-id="62e2d-106">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="62e2d-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="62e2d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62e2d-107">EXAMPLES</span></span>

### <span data-ttu-id="62e2d-108">Пример 1: Создание правила виртуальной сети сервера MySql</span><span class="sxs-lookup"><span data-stu-id="62e2d-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="62e2d-109">Эти командлеты создают правило виртуальной сети сервера MySql.</span><span class="sxs-lookup"><span data-stu-id="62e2d-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="62e2d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62e2d-110">PARAMETERS</span></span>

### <span data-ttu-id="62e2d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62e2d-111">-AsJob</span></span>
<span data-ttu-id="62e2d-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="62e2d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="62e2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e2d-113">-DefaultProfile</span></span>
<span data-ttu-id="62e2d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62e2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e2d-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="62e2d-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="62e2d-116">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="62e2d-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="62e2d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62e2d-117">-Name</span></span>
<span data-ttu-id="62e2d-118">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="62e2d-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e2d-119">-Wait</span><span class="sxs-lookup"><span data-stu-id="62e2d-119">-NoWait</span></span>
<span data-ttu-id="62e2d-120">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="62e2d-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="62e2d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62e2d-121">-PassThru</span></span>
<span data-ttu-id="62e2d-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="62e2d-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="62e2d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e2d-123">-ResourceGroupName</span></span>
<span data-ttu-id="62e2d-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62e2d-124">The name of the resource group.</span></span>
<span data-ttu-id="62e2d-125">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="62e2d-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="62e2d-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="62e2d-126">-ServerName</span></span>
<span data-ttu-id="62e2d-127">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="62e2d-127">The name of the server.</span></span>

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

### <span data-ttu-id="62e2d-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="62e2d-128">-SubnetId</span></span>
<span data-ttu-id="62e2d-129">Идентификатор ресурса ARM для подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="62e2d-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="62e2d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62e2d-130">-SubscriptionId</span></span>
<span data-ttu-id="62e2d-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="62e2d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="62e2d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62e2d-132">-Confirm</span></span>
<span data-ttu-id="62e2d-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62e2d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e2d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e2d-134">-WhatIf</span></span>
<span data-ttu-id="62e2d-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62e2d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e2d-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62e2d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e2d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e2d-137">CommonParameters</span></span>
<span data-ttu-id="62e2d-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62e2d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e2d-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62e2d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e2d-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62e2d-140">INPUTS</span></span>

## <span data-ttu-id="62e2d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62e2d-141">OUTPUTS</span></span>

### <span data-ttu-id="62e2d-142">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="62e2d-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="62e2d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="62e2d-143">NOTES</span></span>

<span data-ttu-id="62e2d-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="62e2d-144">ALIASES</span></span>

## <span data-ttu-id="62e2d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62e2d-145">RELATED LINKS</span></span>

