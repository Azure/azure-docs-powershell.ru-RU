---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246918"
---
# <span data-ttu-id="a924b-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="a924b-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="a924b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a924b-102">SYNOPSIS</span></span>
<span data-ttu-id="a924b-103">Обновите узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="a924b-103">Update the transaction node.</span></span>

## <span data-ttu-id="a924b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a924b-104">SYNTAX</span></span>

### <span data-ttu-id="a924b-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a924b-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a924b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a924b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a924b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a924b-107">DESCRIPTION</span></span>
<span data-ttu-id="a924b-108">Обновите узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="a924b-108">Update the transaction node.</span></span>

## <span data-ttu-id="a924b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a924b-109">EXAMPLES</span></span>

### <span data-ttu-id="a924b-110">Пример 1: обновление узла transcation</span><span class="sxs-lookup"><span data-stu-id="a924b-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="a924b-111">Эта команда обновляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="a924b-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="a924b-112">Пример 2: обновление узла transcation</span><span class="sxs-lookup"><span data-stu-id="a924b-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="a924b-113">Эта команда обновляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="a924b-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="a924b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a924b-114">PARAMETERS</span></span>

### <span data-ttu-id="a924b-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="a924b-115">-BlockchainMemberName</span></span>
<span data-ttu-id="a924b-116">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="a924b-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a924b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a924b-117">-DefaultProfile</span></span>
<span data-ttu-id="a924b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a924b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a924b-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="a924b-119">-FirewallRule</span></span>
<span data-ttu-id="a924b-120">Возвращает или задает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a924b-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="a924b-121">Для конструирования ознакомьтесь с разделом "Заметки" для свойств FIREWALLRULE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a924b-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a924b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a924b-122">-InputObject</span></span>
<span data-ttu-id="a924b-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a924b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a924b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a924b-124">-Name</span></span>
<span data-ttu-id="a924b-125">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="a924b-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a924b-126">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="a924b-126">-Password</span></span>
<span data-ttu-id="a924b-127">Задает пароль базовой проверки подлинности конечной точки DNS узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="a924b-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="a924b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a924b-128">-ResourceGroupName</span></span>
<span data-ttu-id="a924b-129">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="a924b-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a924b-130">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="a924b-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a924b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a924b-131">-SubscriptionId</span></span>
<span data-ttu-id="a924b-132">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a924b-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a924b-133">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a924b-133">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a924b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a924b-134">-Confirm</span></span>
<span data-ttu-id="a924b-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a924b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a924b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a924b-136">-WhatIf</span></span>
<span data-ttu-id="a924b-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a924b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a924b-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a924b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a924b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a924b-139">CommonParameters</span></span>
<span data-ttu-id="a924b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a924b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a924b-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a924b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a924b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a924b-142">INPUTS</span></span>

### <span data-ttu-id="a924b-143">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="a924b-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="a924b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a924b-144">OUTPUTS</span></span>

### <span data-ttu-id="a924b-145">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="a924b-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="a924b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="a924b-146">NOTES</span></span>

<span data-ttu-id="a924b-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a924b-147">ALIASES</span></span>

<span data-ttu-id="a924b-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a924b-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a924b-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a924b-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a924b-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a924b-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a924b-151">FIREWALLRULE <IFirewallRule [] >: Получает или задает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a924b-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="a924b-152">`[EndIPAddress <String>]`: Возвращает или задает конечный IP-адрес диапазона правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a924b-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="a924b-153">`[RuleName <String>]`: Получает или задает имя правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a924b-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="a924b-154">`[StartIPAddress <String>]`: Возвращает или задает начальный IP-адрес диапазона правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a924b-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="a924b-155">INPUTOBJECT <IBlockchainIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a924b-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a924b-156">`[BlockchainMemberName <String>]`: Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="a924b-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="a924b-157">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a924b-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a924b-158">`[Location <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="a924b-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="a924b-159">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="a924b-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="a924b-160">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="a924b-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a924b-161">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="a924b-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a924b-162">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a924b-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="a924b-163">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a924b-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="a924b-164">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="a924b-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="a924b-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a924b-165">RELATED LINKS</span></span>
