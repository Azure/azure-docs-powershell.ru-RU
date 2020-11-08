---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079161"
---
# <span data-ttu-id="70d9a-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="70d9a-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="70d9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="70d9a-103">Создание blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="70d9a-103">Create a blockchain member.</span></span>

## <span data-ttu-id="70d9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70d9a-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70d9a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="70d9a-106">Создание blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="70d9a-106">Create a blockchain member.</span></span>

## <span data-ttu-id="70d9a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="70d9a-108">Пример 1: создание нового участника blockchain</span><span class="sxs-lookup"><span data-stu-id="70d9a-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="70d9a-109">Эта команда создает новый элемент blockchain.</span><span class="sxs-lookup"><span data-stu-id="70d9a-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="70d9a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70d9a-110">PARAMETERS</span></span>

### <span data-ttu-id="70d9a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70d9a-111">-AsJob</span></span>
<span data-ttu-id="70d9a-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="70d9a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="70d9a-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="70d9a-113">-Consortium</span></span>
<span data-ttu-id="70d9a-114">Возвращает или задает консорциума для элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="70d9a-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="70d9a-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="70d9a-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="70d9a-116">Задает пароль учетной записи управляемого консорциума для управления.</span><span class="sxs-lookup"><span data-stu-id="70d9a-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="70d9a-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="70d9a-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="70d9a-118">Возвращает отображаемое имя элемента в консорциуме.</span><span class="sxs-lookup"><span data-stu-id="70d9a-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="70d9a-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="70d9a-119">-ConsortiumRole</span></span>
<span data-ttu-id="70d9a-120">Получает роль элемента в консорциуме.</span><span class="sxs-lookup"><span data-stu-id="70d9a-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="70d9a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d9a-121">-DefaultProfile</span></span>
<span data-ttu-id="70d9a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70d9a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70d9a-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="70d9a-123">-FirewallRule</span></span>
<span data-ttu-id="70d9a-124">Возвращает или задает правила брандмауэра для создания свойств FIREWALLRULE и создания хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="70d9a-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="70d9a-125">-Location</span><span class="sxs-lookup"><span data-stu-id="70d9a-125">-Location</span></span>
<span data-ttu-id="70d9a-126">Географическое расположение службы blockchain.</span><span class="sxs-lookup"><span data-stu-id="70d9a-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="70d9a-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="70d9a-127">-Name</span></span>
<span data-ttu-id="70d9a-128">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="70d9a-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d9a-129">-Wait</span><span class="sxs-lookup"><span data-stu-id="70d9a-129">-NoWait</span></span>
<span data-ttu-id="70d9a-130">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="70d9a-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="70d9a-131">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="70d9a-131">-Password</span></span>
<span data-ttu-id="70d9a-132">Задает основной пароль для проверки подлинности участника blockchain.</span><span class="sxs-lookup"><span data-stu-id="70d9a-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="70d9a-133">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="70d9a-133">-Protocol</span></span>
<span data-ttu-id="70d9a-134">Возвращает или задает протокол blockchain.</span><span class="sxs-lookup"><span data-stu-id="70d9a-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d9a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d9a-135">-ResourceGroupName</span></span>
<span data-ttu-id="70d9a-136">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="70d9a-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="70d9a-137">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="70d9a-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="70d9a-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="70d9a-138">-Sku</span></span>
<span data-ttu-id="70d9a-139">Возвращает или задает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="70d9a-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="70d9a-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="70d9a-140">-SkuTier</span></span>
<span data-ttu-id="70d9a-141">Возвращает или задает уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="70d9a-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="70d9a-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70d9a-142">-SubscriptionId</span></span>
<span data-ttu-id="70d9a-143">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="70d9a-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="70d9a-144">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="70d9a-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="70d9a-145">-Тег</span><span class="sxs-lookup"><span data-stu-id="70d9a-145">-Tag</span></span>
<span data-ttu-id="70d9a-146">Теги службы, представляющие собой список пар "ключ-значение", описывающих ресурс.</span><span class="sxs-lookup"><span data-stu-id="70d9a-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d9a-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="70d9a-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="70d9a-148">Возвращает или задает емкость узлов.</span><span class="sxs-lookup"><span data-stu-id="70d9a-148">Gets or sets the nodes capacity.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d9a-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70d9a-149">-Confirm</span></span>
<span data-ttu-id="70d9a-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70d9a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d9a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d9a-151">-WhatIf</span></span>
<span data-ttu-id="70d9a-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70d9a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70d9a-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70d9a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d9a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d9a-154">CommonParameters</span></span>
<span data-ttu-id="70d9a-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70d9a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d9a-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70d9a-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d9a-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70d9a-157">INPUTS</span></span>

## <span data-ttu-id="70d9a-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70d9a-158">OUTPUTS</span></span>

### <span data-ttu-id="70d9a-159">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="70d9a-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="70d9a-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="70d9a-160">NOTES</span></span>

<span data-ttu-id="70d9a-161">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="70d9a-161">ALIASES</span></span>

<span data-ttu-id="70d9a-162">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="70d9a-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70d9a-163">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70d9a-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70d9a-164">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="70d9a-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70d9a-165">FIREWALLRULE <IFirewallRule [] >: Получает или задает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="70d9a-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="70d9a-166">`[EndIPAddress <String>]`: Возвращает или задает конечный IP-адрес диапазона правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="70d9a-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="70d9a-167">`[RuleName <String>]`: Получает или задает имя правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="70d9a-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="70d9a-168">`[StartIPAddress <String>]`: Возвращает или задает начальный IP-адрес диапазона правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="70d9a-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="70d9a-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70d9a-169">RELATED LINKS</span></span>

