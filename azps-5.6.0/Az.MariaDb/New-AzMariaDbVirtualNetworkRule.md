---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cfbbfd9472d18d75dea3da68cb4d2e06cf54c9a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970568"
---
# <span data-ttu-id="e0109-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e0109-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="e0109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0109-102">SYNOPSIS</span></span>
<span data-ttu-id="e0109-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e0109-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e0109-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0109-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0109-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0109-105">DESCRIPTION</span></span>
<span data-ttu-id="e0109-106">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e0109-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e0109-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0109-107">EXAMPLES</span></span>

### <span data-ttu-id="e0109-108">Пример 1. Создание виртуального правила сети для MariaDB</span><span class="sxs-lookup"><span data-stu-id="e0109-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="e0109-109">Эта команда создает виртуальное правило сети для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="e0109-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="e0109-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0109-110">PARAMETERS</span></span>

### <span data-ttu-id="e0109-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0109-111">-AsJob</span></span>
<span data-ttu-id="e0109-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e0109-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e0109-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0109-113">-DefaultProfile</span></span>
<span data-ttu-id="e0109-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0109-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0109-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e0109-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e0109-116">Создайте правило брандмауэра до того, как в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="e0109-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="e0109-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e0109-117">-Name</span></span>
<span data-ttu-id="e0109-118">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="e0109-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e0109-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e0109-119">-NoWait</span></span>
<span data-ttu-id="e0109-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="e0109-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e0109-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0109-121">-PassThru</span></span>
<span data-ttu-id="e0109-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="e0109-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e0109-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0109-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0109-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="e0109-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e0109-125">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="e0109-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e0109-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0109-126">-ServerName</span></span>
<span data-ttu-id="e0109-127">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e0109-127">The name of the server.</span></span>

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

### <span data-ttu-id="e0109-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e0109-128">-SubnetId</span></span>
<span data-ttu-id="e0109-129">Это ARM ресурса виртуальной подсети сети.</span><span class="sxs-lookup"><span data-stu-id="e0109-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="e0109-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0109-130">-SubscriptionId</span></span>
<span data-ttu-id="e0109-131">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="e0109-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e0109-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0109-132">-Confirm</span></span>
<span data-ttu-id="e0109-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e0109-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0109-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0109-134">-WhatIf</span></span>
<span data-ttu-id="e0109-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0109-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0109-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e0109-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0109-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0109-137">CommonParameters</span></span>
<span data-ttu-id="e0109-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0109-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0109-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0109-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0109-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0109-140">INPUTS</span></span>

## <span data-ttu-id="e0109-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0109-141">OUTPUTS</span></span>

### <span data-ttu-id="e0109-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e0109-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="e0109-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0109-143">NOTES</span></span>

<span data-ttu-id="e0109-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e0109-144">ALIASES</span></span>

## <span data-ttu-id="e0109-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0109-145">RELATED LINKS</span></span>

