---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227185"
---
# <span data-ttu-id="172a6-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="172a6-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="172a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="172a6-102">SYNOPSIS</span></span>
<span data-ttu-id="172a6-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="172a6-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="172a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="172a6-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="172a6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="172a6-105">DESCRIPTION</span></span>
<span data-ttu-id="172a6-106">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="172a6-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="172a6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="172a6-107">EXAMPLES</span></span>

### <span data-ttu-id="172a6-108">Пример 1. Создание нового правила виртуальной сети PostgreSql server</span><span class="sxs-lookup"><span data-stu-id="172a6-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="172a6-109">Эти cmdlets create a PostgreSql server Virtual Network Rule.</span><span class="sxs-lookup"><span data-stu-id="172a6-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="172a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="172a6-110">PARAMETERS</span></span>

### <span data-ttu-id="172a6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="172a6-111">-AsJob</span></span>
<span data-ttu-id="172a6-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="172a6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="172a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172a6-113">-DefaultProfile</span></span>
<span data-ttu-id="172a6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="172a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="172a6-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="172a6-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="172a6-116">Создайте правило брандмауэра до того, как в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="172a6-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="172a6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="172a6-117">-Name</span></span>
<span data-ttu-id="172a6-118">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="172a6-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="172a6-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="172a6-119">-NoWait</span></span>
<span data-ttu-id="172a6-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="172a6-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="172a6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="172a6-121">-PassThru</span></span>
<span data-ttu-id="172a6-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="172a6-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="172a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="172a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="172a6-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="172a6-124">The name of the resource group.</span></span>
<span data-ttu-id="172a6-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="172a6-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="172a6-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="172a6-126">-ServerName</span></span>
<span data-ttu-id="172a6-127">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="172a6-127">The name of the server.</span></span>

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

### <span data-ttu-id="172a6-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="172a6-128">-SubnetId</span></span>
<span data-ttu-id="172a6-129">Это ARM ресурса виртуальной подсети сети.</span><span class="sxs-lookup"><span data-stu-id="172a6-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="172a6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="172a6-130">-SubscriptionId</span></span>
<span data-ttu-id="172a6-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="172a6-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="172a6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="172a6-132">-Confirm</span></span>
<span data-ttu-id="172a6-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="172a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="172a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="172a6-134">-WhatIf</span></span>
<span data-ttu-id="172a6-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="172a6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="172a6-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="172a6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="172a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172a6-137">CommonParameters</span></span>
<span data-ttu-id="172a6-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172a6-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="172a6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172a6-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="172a6-140">INPUTS</span></span>

## <span data-ttu-id="172a6-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="172a6-141">OUTPUTS</span></span>

### <span data-ttu-id="172a6-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="172a6-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="172a6-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="172a6-143">NOTES</span></span>

<span data-ttu-id="172a6-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="172a6-144">ALIASES</span></span>

## <span data-ttu-id="172a6-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="172a6-145">RELATED LINKS</span></span>

