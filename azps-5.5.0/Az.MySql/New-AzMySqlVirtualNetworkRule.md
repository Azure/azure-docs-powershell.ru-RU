---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214121"
---
# <span data-ttu-id="93056-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="93056-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="93056-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93056-102">SYNOPSIS</span></span>
<span data-ttu-id="93056-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="93056-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="93056-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93056-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93056-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93056-105">DESCRIPTION</span></span>
<span data-ttu-id="93056-106">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="93056-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="93056-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93056-107">EXAMPLES</span></span>

### <span data-ttu-id="93056-108">Пример 1. Создание нового правила виртуальной сети MySql Server</span><span class="sxs-lookup"><span data-stu-id="93056-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="93056-109">Эти cmdlets создают правило виртуальной сети MySql Server.</span><span class="sxs-lookup"><span data-stu-id="93056-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="93056-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93056-110">PARAMETERS</span></span>

### <span data-ttu-id="93056-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93056-111">-AsJob</span></span>
<span data-ttu-id="93056-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="93056-112">Run the command as a job</span></span>

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

### <span data-ttu-id="93056-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93056-113">-DefaultProfile</span></span>
<span data-ttu-id="93056-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93056-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93056-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="93056-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="93056-116">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="93056-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="93056-117">-Name</span><span class="sxs-lookup"><span data-stu-id="93056-117">-Name</span></span>
<span data-ttu-id="93056-118">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="93056-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="93056-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="93056-119">-NoWait</span></span>
<span data-ttu-id="93056-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="93056-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="93056-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93056-121">-PassThru</span></span>
<span data-ttu-id="93056-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="93056-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="93056-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93056-123">-ResourceGroupName</span></span>
<span data-ttu-id="93056-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93056-124">The name of the resource group.</span></span>
<span data-ttu-id="93056-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="93056-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="93056-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93056-126">-ServerName</span></span>
<span data-ttu-id="93056-127">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="93056-127">The name of the server.</span></span>

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

### <span data-ttu-id="93056-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="93056-128">-SubnetId</span></span>
<span data-ttu-id="93056-129">Это ARM ресурса виртуальной подсети сети.</span><span class="sxs-lookup"><span data-stu-id="93056-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="93056-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93056-130">-SubscriptionId</span></span>
<span data-ttu-id="93056-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="93056-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="93056-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93056-132">-Confirm</span></span>
<span data-ttu-id="93056-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93056-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93056-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93056-134">-WhatIf</span></span>
<span data-ttu-id="93056-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93056-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93056-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="93056-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93056-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93056-137">CommonParameters</span></span>
<span data-ttu-id="93056-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93056-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93056-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93056-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93056-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93056-140">INPUTS</span></span>

## <span data-ttu-id="93056-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93056-141">OUTPUTS</span></span>

### <span data-ttu-id="93056-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="93056-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="93056-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93056-143">NOTES</span></span>

<span data-ttu-id="93056-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="93056-144">ALIASES</span></span>

## <span data-ttu-id="93056-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93056-145">RELATED LINKS</span></span>

