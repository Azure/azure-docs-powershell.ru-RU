---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249542"
---
# <span data-ttu-id="b08aa-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="b08aa-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="b08aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b08aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b08aa-103">Создание или обновление узла "транзакция".</span><span class="sxs-lookup"><span data-stu-id="b08aa-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="b08aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b08aa-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b08aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b08aa-105">DESCRIPTION</span></span>
<span data-ttu-id="b08aa-106">Создание или обновление узла "транзакция".</span><span class="sxs-lookup"><span data-stu-id="b08aa-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="b08aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b08aa-107">EXAMPLES</span></span>

### <span data-ttu-id="b08aa-108">Пример 1: создание узла транзакции blockchain</span><span class="sxs-lookup"><span data-stu-id="b08aa-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="b08aa-109">Эта команда создает узел транзакции blockchain.</span><span class="sxs-lookup"><span data-stu-id="b08aa-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="b08aa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b08aa-110">PARAMETERS</span></span>

### <span data-ttu-id="b08aa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b08aa-111">-AsJob</span></span>
<span data-ttu-id="b08aa-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b08aa-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b08aa-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="b08aa-113">-BlockchainMemberName</span></span>
<span data-ttu-id="b08aa-114">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="b08aa-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="b08aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08aa-115">-DefaultProfile</span></span>
<span data-ttu-id="b08aa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b08aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b08aa-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="b08aa-117">-FirewallRule</span></span>
<span data-ttu-id="b08aa-118">Возвращает или задает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b08aa-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="b08aa-119">Для конструирования ознакомьтесь с разделом "Заметки" для свойств FIREWALLRULE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="b08aa-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="b08aa-120">-Location</span><span class="sxs-lookup"><span data-stu-id="b08aa-120">-Location</span></span>
<span data-ttu-id="b08aa-121">Возвращает или задает расположение узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="b08aa-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="b08aa-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b08aa-122">-Name</span></span>
<span data-ttu-id="b08aa-123">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="b08aa-123">Transaction node name.</span></span>

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

### <span data-ttu-id="b08aa-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="b08aa-124">-NoWait</span></span>
<span data-ttu-id="b08aa-125">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="b08aa-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b08aa-126">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="b08aa-126">-Password</span></span>
<span data-ttu-id="b08aa-127">Задает пароль базовой проверки подлинности конечной точки DNS узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="b08aa-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="b08aa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b08aa-128">-ResourceGroupName</span></span>
<span data-ttu-id="b08aa-129">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="b08aa-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b08aa-130">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="b08aa-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b08aa-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b08aa-131">-SubscriptionId</span></span>
<span data-ttu-id="b08aa-132">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b08aa-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b08aa-133">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b08aa-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b08aa-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b08aa-134">-Confirm</span></span>
<span data-ttu-id="b08aa-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b08aa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b08aa-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b08aa-136">-WhatIf</span></span>
<span data-ttu-id="b08aa-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b08aa-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b08aa-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b08aa-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b08aa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08aa-139">CommonParameters</span></span>
<span data-ttu-id="b08aa-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b08aa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08aa-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b08aa-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08aa-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b08aa-142">INPUTS</span></span>

## <span data-ttu-id="b08aa-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b08aa-143">OUTPUTS</span></span>

### <span data-ttu-id="b08aa-144">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="b08aa-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="b08aa-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="b08aa-145">NOTES</span></span>

<span data-ttu-id="b08aa-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="b08aa-146">ALIASES</span></span>

<span data-ttu-id="b08aa-147">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b08aa-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b08aa-148">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b08aa-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b08aa-149">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b08aa-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b08aa-150">FIREWALLRULE <IFirewallRule [] >: Получает или задает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b08aa-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="b08aa-151">`[EndIPAddress <String>]`: Возвращает или задает конечный IP-адрес диапазона правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b08aa-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="b08aa-152">`[RuleName <String>]`: Получает или задает имя правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b08aa-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="b08aa-153">`[StartIPAddress <String>]`: Возвращает или задает начальный IP-адрес диапазона правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b08aa-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="b08aa-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b08aa-154">RELATED LINKS</span></span>

