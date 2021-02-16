---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212017"
---
# <span data-ttu-id="fe9f6-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="fe9f6-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="fe9f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe9f6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9f6-103">Создание или обновление узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="fe9f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe9f6-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe9f6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe9f6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9f6-106">Создание или обновление узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="fe9f6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe9f6-107">EXAMPLES</span></span>

### <span data-ttu-id="fe9f6-108">Пример 1. Создание узла транзакции</span><span class="sxs-lookup"><span data-stu-id="fe9f6-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="fe9f6-109">Эта команда создает узел транзакций.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="fe9f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe9f6-110">PARAMETERS</span></span>

### <span data-ttu-id="fe9f6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe9f6-111">-AsJob</span></span>
<span data-ttu-id="fe9f6-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="fe9f6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fe9f6-113">-ЛесОИмяноИмя</span><span class="sxs-lookup"><span data-stu-id="fe9f6-113">-BlockchainMemberName</span></span>
<span data-ttu-id="fe9f6-114">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="fe9f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9f6-115">-DefaultProfile</span></span>
<span data-ttu-id="fe9f6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe9f6-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="fe9f6-117">-FirewallRule</span></span>
<span data-ttu-id="fe9f6-118">Получает или настраивает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="fe9f6-119">Чтобы построить, см. раздел "ЗАМЕТКИ" для свойств FIREWALLRULE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f6-120">-Location</span><span class="sxs-lookup"><span data-stu-id="fe9f6-120">-Location</span></span>
<span data-ttu-id="fe9f6-121">Возвращает или задает расположение узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="fe9f6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fe9f6-122">-Name</span></span>
<span data-ttu-id="fe9f6-123">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f6-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fe9f6-124">-NoWait</span></span>
<span data-ttu-id="fe9f6-125">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="fe9f6-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fe9f6-126">-Password</span><span class="sxs-lookup"><span data-stu-id="fe9f6-126">-Password</span></span>
<span data-ttu-id="fe9f6-127">Задает пароль основной пароля для узла транзакции dns basic для конечных точек.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-127">Sets the transaction node dns endpoint basic auth password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="fe9f6-129">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fe9f6-130">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fe9f6-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe9f6-131">-SubscriptionId</span></span>
<span data-ttu-id="fe9f6-132">Возвращает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fe9f6-133">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fe9f6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe9f6-134">-Confirm</span></span>
<span data-ttu-id="fe9f6-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe9f6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe9f6-136">-WhatIf</span></span>
<span data-ttu-id="fe9f6-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe9f6-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe9f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9f6-139">CommonParameters</span></span>
<span data-ttu-id="fe9f6-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9f6-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe9f6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9f6-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe9f6-142">INPUTS</span></span>

## <span data-ttu-id="fe9f6-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe9f6-143">OUTPUTS</span></span>

### <span data-ttu-id="fe9f6-144">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="fe9f6-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="fe9f6-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe9f6-145">NOTES</span></span>

<span data-ttu-id="fe9f6-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fe9f6-146">ALIASES</span></span>

<span data-ttu-id="fe9f6-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fe9f6-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fe9f6-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe9f6-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fe9f6-150">FIREWALLRULE <IFirewallRule[]>: получает или настраивает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="fe9f6-151">`[EndIPAddress <String>]`. Возвращает или устанавливает конечный IP-адрес диапазона правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="fe9f6-152">`[RuleName <String>]`: получает или задает имя правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="fe9f6-153">`[StartIPAddress <String>]`: получает или устанавливает IP-адрес запуска в диапазоне правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="fe9f6-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="fe9f6-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe9f6-154">RELATED LINKS</span></span>

