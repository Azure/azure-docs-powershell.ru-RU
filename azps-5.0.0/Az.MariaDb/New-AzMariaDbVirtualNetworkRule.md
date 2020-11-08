---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248644"
---
# <span data-ttu-id="302ee-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="302ee-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="302ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="302ee-102">SYNOPSIS</span></span>
<span data-ttu-id="302ee-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="302ee-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="302ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="302ee-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="302ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="302ee-105">DESCRIPTION</span></span>
<span data-ttu-id="302ee-106">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="302ee-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="302ee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="302ee-107">EXAMPLES</span></span>

### <span data-ttu-id="302ee-108">Пример 1: Создание правила для виртуальной сети для MariaDB</span><span class="sxs-lookup"><span data-stu-id="302ee-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="302ee-109">Эта команда создает правило виртуальной сети для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="302ee-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="302ee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="302ee-110">PARAMETERS</span></span>

### <span data-ttu-id="302ee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="302ee-111">-AsJob</span></span>
<span data-ttu-id="302ee-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="302ee-112">Run the command as a job</span></span>

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

### <span data-ttu-id="302ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302ee-113">-DefaultProfile</span></span>
<span data-ttu-id="302ee-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="302ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="302ee-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="302ee-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="302ee-116">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="302ee-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="302ee-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="302ee-117">-Name</span></span>
<span data-ttu-id="302ee-118">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="302ee-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="302ee-119">-Wait</span><span class="sxs-lookup"><span data-stu-id="302ee-119">-NoWait</span></span>
<span data-ttu-id="302ee-120">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="302ee-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="302ee-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="302ee-121">-PassThru</span></span>
<span data-ttu-id="302ee-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="302ee-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="302ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="302ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="302ee-124">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="302ee-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="302ee-125">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="302ee-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="302ee-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="302ee-126">-ServerName</span></span>
<span data-ttu-id="302ee-127">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="302ee-127">The name of the server.</span></span>

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

### <span data-ttu-id="302ee-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="302ee-128">-SubnetId</span></span>
<span data-ttu-id="302ee-129">Идентификатор ресурса ARM для подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="302ee-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="302ee-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="302ee-130">-SubscriptionId</span></span>
<span data-ttu-id="302ee-131">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="302ee-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="302ee-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="302ee-132">-Confirm</span></span>
<span data-ttu-id="302ee-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="302ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="302ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="302ee-134">-WhatIf</span></span>
<span data-ttu-id="302ee-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="302ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="302ee-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="302ee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="302ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302ee-137">CommonParameters</span></span>
<span data-ttu-id="302ee-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="302ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302ee-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="302ee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302ee-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="302ee-140">INPUTS</span></span>

## <span data-ttu-id="302ee-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="302ee-141">OUTPUTS</span></span>

### <span data-ttu-id="302ee-142">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="302ee-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="302ee-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="302ee-143">NOTES</span></span>

<span data-ttu-id="302ee-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="302ee-144">ALIASES</span></span>

## <span data-ttu-id="302ee-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="302ee-145">RELATED LINKS</span></span>

