---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219193"
---
# <span data-ttu-id="d193f-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d193f-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="d193f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d193f-102">SYNOPSIS</span></span>
<span data-ttu-id="d193f-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d193f-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="d193f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d193f-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d193f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d193f-105">DESCRIPTION</span></span>
<span data-ttu-id="d193f-106">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d193f-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="d193f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d193f-107">EXAMPLES</span></span>

### <span data-ttu-id="d193f-108">Пример 1. Создание виртуального правила сети для MariaDB</span><span class="sxs-lookup"><span data-stu-id="d193f-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="d193f-109">Эта команда создает виртуальное правило сети для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d193f-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="d193f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d193f-110">PARAMETERS</span></span>

### <span data-ttu-id="d193f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d193f-111">-AsJob</span></span>
<span data-ttu-id="d193f-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d193f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d193f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d193f-113">-DefaultProfile</span></span>
<span data-ttu-id="d193f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d193f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d193f-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d193f-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="d193f-116">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="d193f-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="d193f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d193f-117">-Name</span></span>
<span data-ttu-id="d193f-118">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="d193f-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="d193f-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d193f-119">-NoWait</span></span>
<span data-ttu-id="d193f-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="d193f-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d193f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d193f-121">-PassThru</span></span>
<span data-ttu-id="d193f-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="d193f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d193f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d193f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d193f-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="d193f-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d193f-125">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d193f-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d193f-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d193f-126">-ServerName</span></span>
<span data-ttu-id="d193f-127">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d193f-127">The name of the server.</span></span>

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

### <span data-ttu-id="d193f-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d193f-128">-SubnetId</span></span>
<span data-ttu-id="d193f-129">Подсети ARM ресурсов виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d193f-129">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d193f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d193f-130">-SubscriptionId</span></span>
<span data-ttu-id="d193f-131">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="d193f-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d193f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d193f-132">-Confirm</span></span>
<span data-ttu-id="d193f-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d193f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d193f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d193f-134">-WhatIf</span></span>
<span data-ttu-id="d193f-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d193f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d193f-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d193f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d193f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d193f-137">CommonParameters</span></span>
<span data-ttu-id="d193f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d193f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d193f-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d193f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d193f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d193f-140">INPUTS</span></span>

## <span data-ttu-id="d193f-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d193f-141">OUTPUTS</span></span>

### <span data-ttu-id="d193f-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d193f-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="d193f-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d193f-143">NOTES</span></span>

<span data-ttu-id="d193f-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d193f-144">ALIASES</span></span>

## <span data-ttu-id="d193f-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d193f-145">RELATED LINKS</span></span>

