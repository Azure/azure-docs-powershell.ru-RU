---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412599"
---
# <span data-ttu-id="ad64d-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="ad64d-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="ad64d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad64d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad64d-103">Обновив узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="ad64d-103">Update the transaction node.</span></span>

## <span data-ttu-id="ad64d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad64d-104">SYNTAX</span></span>

### <span data-ttu-id="ad64d-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad64d-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ad64d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ad64d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad64d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad64d-107">DESCRIPTION</span></span>
<span data-ttu-id="ad64d-108">Обновив узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="ad64d-108">Update the transaction node.</span></span>

## <span data-ttu-id="ad64d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad64d-109">EXAMPLES</span></span>

### <span data-ttu-id="ad64d-110">Пример 1. Обновление узла транспонации</span><span class="sxs-lookup"><span data-stu-id="ad64d-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="ad64d-111">Эта команда обновляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="ad64d-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="ad64d-112">Пример 2. Обновление узла транспонации</span><span class="sxs-lookup"><span data-stu-id="ad64d-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="ad64d-113">Эта команда обновляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="ad64d-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="ad64d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad64d-114">PARAMETERS</span></span>

### <span data-ttu-id="ad64d-115">-ЛесОИмяноИмя</span><span class="sxs-lookup"><span data-stu-id="ad64d-115">-BlockchainMemberName</span></span>
<span data-ttu-id="ad64d-116">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="ad64d-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="ad64d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad64d-117">-DefaultProfile</span></span>
<span data-ttu-id="ad64d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad64d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad64d-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad64d-119">-FirewallRule</span></span>
<span data-ttu-id="ad64d-120">Получает или настраивает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ad64d-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="ad64d-121">Чтобы построить, см. раздел "ЗАМЕТКИ" для свойств FIREWALLRULE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ad64d-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad64d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad64d-122">-InputObject</span></span>
<span data-ttu-id="ad64d-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ad64d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad64d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ad64d-124">-Name</span></span>
<span data-ttu-id="ad64d-125">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ad64d-125">Transaction node name.</span></span>

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

### <span data-ttu-id="ad64d-126">-Password</span><span class="sxs-lookup"><span data-stu-id="ad64d-126">-Password</span></span>
<span data-ttu-id="ad64d-127">Задает пароль основной auth узла транзакции dns для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ad64d-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="ad64d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad64d-128">-ResourceGroupName</span></span>
<span data-ttu-id="ad64d-129">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="ad64d-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ad64d-130">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ad64d-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ad64d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad64d-131">-SubscriptionId</span></span>
<span data-ttu-id="ad64d-132">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad64d-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ad64d-133">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ad64d-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ad64d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad64d-134">-Confirm</span></span>
<span data-ttu-id="ad64d-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad64d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad64d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad64d-136">-WhatIf</span></span>
<span data-ttu-id="ad64d-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad64d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad64d-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad64d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad64d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad64d-139">CommonParameters</span></span>
<span data-ttu-id="ad64d-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad64d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad64d-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad64d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad64d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad64d-142">INPUTS</span></span>

### <span data-ttu-id="ad64d-143">Microsoft.Azure.PowerShell.Cmdlets.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="ad64d-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="ad64d-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad64d-144">OUTPUTS</span></span>

### <span data-ttu-id="ad64d-145">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="ad64d-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="ad64d-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad64d-146">NOTES</span></span>

<span data-ttu-id="ad64d-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ad64d-147">ALIASES</span></span>

<span data-ttu-id="ad64d-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ad64d-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad64d-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ad64d-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad64d-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad64d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad64d-151">FIREWALLRULE <IFirewallRule[]>: получает или устанавливает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ad64d-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="ad64d-152">`[EndIPAddress <String>]`. Возвращает или устанавливает конечный IP-адрес диапазона правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ad64d-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="ad64d-153">`[RuleName <String>]`: получает или задает имя правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ad64d-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="ad64d-154">`[StartIPAddress <String>]`: получает или устанавливает IP-адрес запуска в диапазоне правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ad64d-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="ad64d-155">INPUTOBJECT <IBlockchainIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ad64d-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad64d-156">`[BlockchainMemberName <String>]`: Имя участника.</span><span class="sxs-lookup"><span data-stu-id="ad64d-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="ad64d-157">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ad64d-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad64d-158">`[Location <String>]`: имя расположения.</span><span class="sxs-lookup"><span data-stu-id="ad64d-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="ad64d-159">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="ad64d-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="ad64d-160">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="ad64d-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ad64d-161">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ad64d-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ad64d-162">`[SubscriptionId <String>]`: получает идентификатор подписки, однозначно определяя подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad64d-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="ad64d-163">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ad64d-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="ad64d-164">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ad64d-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="ad64d-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad64d-165">RELATED LINKS</span></span>

