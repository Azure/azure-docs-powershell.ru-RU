---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079155"
---
# <span data-ttu-id="81b3a-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="81b3a-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="81b3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="81b3a-103">Обновление элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="81b3a-103">Update a blockchain member.</span></span>

## <span data-ttu-id="81b3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81b3a-104">SYNTAX</span></span>

### <span data-ttu-id="81b3a-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81b3a-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="81b3a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="81b3a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="81b3a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81b3a-107">DESCRIPTION</span></span>
<span data-ttu-id="81b3a-108">Обновление элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="81b3a-108">Update a blockchain member.</span></span>

## <span data-ttu-id="81b3a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81b3a-109">EXAMPLES</span></span>

### <span data-ttu-id="81b3a-110">Пример 1: обновление элемента blockchain</span><span class="sxs-lookup"><span data-stu-id="81b3a-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="81b3a-111">Эта команда обновляет элемент blockchain.</span><span class="sxs-lookup"><span data-stu-id="81b3a-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="81b3a-112">Пример 2: обновление элемента blockchain</span><span class="sxs-lookup"><span data-stu-id="81b3a-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="81b3a-113">Эта команда обновляет элемент blockchain.</span><span class="sxs-lookup"><span data-stu-id="81b3a-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="81b3a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81b3a-114">PARAMETERS</span></span>

### <span data-ttu-id="81b3a-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="81b3a-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="81b3a-116">Задает пароль учетной записи управляемого консорциума для управления.</span><span class="sxs-lookup"><span data-stu-id="81b3a-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="81b3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b3a-117">-DefaultProfile</span></span>
<span data-ttu-id="81b3a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81b3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81b3a-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="81b3a-119">-FirewallRule</span></span>
<span data-ttu-id="81b3a-120">Возвращает или задает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="81b3a-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="81b3a-121">Для конструирования ознакомьтесь с разделом "Заметки" для свойств FIREWALLRULE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="81b3a-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="81b3a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81b3a-122">-InputObject</span></span>
<span data-ttu-id="81b3a-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="81b3a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="81b3a-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81b3a-124">-Name</span></span>
<span data-ttu-id="81b3a-125">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="81b3a-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b3a-126">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="81b3a-126">-Password</span></span>
<span data-ttu-id="81b3a-127">Задает пароль базовой проверки подлинности конечной точки DNS узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="81b3a-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="81b3a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b3a-128">-ResourceGroupName</span></span>
<span data-ttu-id="81b3a-129">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="81b3a-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="81b3a-130">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="81b3a-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="81b3a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81b3a-131">-SubscriptionId</span></span>
<span data-ttu-id="81b3a-132">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="81b3a-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="81b3a-133">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="81b3a-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="81b3a-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="81b3a-134">-Tag</span></span>
<span data-ttu-id="81b3a-135">Теги службы, представляющие собой список пар "ключ-значение", описывающих ресурс.</span><span class="sxs-lookup"><span data-stu-id="81b3a-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="81b3a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81b3a-136">-Confirm</span></span>
<span data-ttu-id="81b3a-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81b3a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b3a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b3a-138">-WhatIf</span></span>
<span data-ttu-id="81b3a-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81b3a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b3a-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81b3a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b3a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b3a-141">CommonParameters</span></span>
<span data-ttu-id="81b3a-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81b3a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b3a-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81b3a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b3a-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81b3a-144">INPUTS</span></span>

### <span data-ttu-id="81b3a-145">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="81b3a-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="81b3a-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81b3a-146">OUTPUTS</span></span>

### <span data-ttu-id="81b3a-147">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="81b3a-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="81b3a-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="81b3a-148">NOTES</span></span>

<span data-ttu-id="81b3a-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="81b3a-149">ALIASES</span></span>

<span data-ttu-id="81b3a-150">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="81b3a-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81b3a-151">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="81b3a-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81b3a-152">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81b3a-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81b3a-153">FIREWALLRULE <IFirewallRule [] >: Получает или задает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="81b3a-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="81b3a-154">`[EndIPAddress <String>]`: Возвращает или задает конечный IP-адрес диапазона правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="81b3a-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="81b3a-155">`[RuleName <String>]`: Получает или задает имя правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="81b3a-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="81b3a-156">`[StartIPAddress <String>]`: Возвращает или задает начальный IP-адрес диапазона правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="81b3a-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="81b3a-157">INPUTOBJECT <IBlockchainIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="81b3a-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81b3a-158">`[BlockchainMemberName <String>]`: Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="81b3a-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="81b3a-159">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="81b3a-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81b3a-160">`[Location <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="81b3a-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="81b3a-161">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="81b3a-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="81b3a-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="81b3a-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="81b3a-163">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="81b3a-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="81b3a-164">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="81b3a-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="81b3a-165">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="81b3a-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="81b3a-166">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="81b3a-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="81b3a-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81b3a-167">RELATED LINKS</span></span>

