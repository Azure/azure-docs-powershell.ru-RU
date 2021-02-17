---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216025"
---
# <span data-ttu-id="c2f0a-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c2f0a-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="c2f0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f0a-103">Обновим участника- участника.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-103">Update a blockchain member.</span></span>

## <span data-ttu-id="c2f0a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2f0a-104">SYNTAX</span></span>

### <span data-ttu-id="c2f0a-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2f0a-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c2f0a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c2f0a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c2f0a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2f0a-107">DESCRIPTION</span></span>
<span data-ttu-id="c2f0a-108">Обновим участника- участника.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-108">Update a blockchain member.</span></span>

## <span data-ttu-id="c2f0a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2f0a-109">EXAMPLES</span></span>

### <span data-ttu-id="c2f0a-110">Пример 1. Обновление участника-участника</span><span class="sxs-lookup"><span data-stu-id="c2f0a-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c2f0a-111">Эта команда обновляет участника-участника.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="c2f0a-112">Пример 2. Обновление участника-участника</span><span class="sxs-lookup"><span data-stu-id="c2f0a-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c2f0a-113">Эта команда обновляет участника-участника.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="c2f0a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2f0a-114">PARAMETERS</span></span>

### <span data-ttu-id="c2f0a-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="c2f0a-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="c2f0a-116">Задает пароль учетной записи для управления управляемым консорциумом.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="c2f0a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f0a-117">-DefaultProfile</span></span>
<span data-ttu-id="c2f0a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f0a-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="c2f0a-119">-FirewallRule</span></span>
<span data-ttu-id="c2f0a-120">Получает или настраивает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="c2f0a-121">Чтобы построить, см. раздел "ЗАМЕТКИ" для свойств FIREWALLRULE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2f0a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2f0a-122">-InputObject</span></span>
<span data-ttu-id="c2f0a-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2f0a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c2f0a-124">-Name</span></span>
<span data-ttu-id="c2f0a-125">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-125">Blockchain member name.</span></span>

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

### <span data-ttu-id="c2f0a-126">-Password</span><span class="sxs-lookup"><span data-stu-id="c2f0a-126">-Password</span></span>
<span data-ttu-id="c2f0a-127">Задает пароль основной пароля для узла транзакции dns basic для конечных точек.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="c2f0a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2f0a-128">-ResourceGroupName</span></span>
<span data-ttu-id="c2f0a-129">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c2f0a-130">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c2f0a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2f0a-131">-SubscriptionId</span></span>
<span data-ttu-id="c2f0a-132">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c2f0a-133">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c2f0a-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2f0a-134">-Tag</span></span>
<span data-ttu-id="c2f0a-135">Теги службы— список ключевых пар значений, описываний ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="c2f0a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2f0a-136">-Confirm</span></span>
<span data-ttu-id="c2f0a-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f0a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f0a-138">-WhatIf</span></span>
<span data-ttu-id="c2f0a-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f0a-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f0a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f0a-141">CommonParameters</span></span>
<span data-ttu-id="c2f0a-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f0a-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2f0a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f0a-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2f0a-144">INPUTS</span></span>

### <span data-ttu-id="c2f0a-145">Microsoft.Azure.PowerShell.Cmdlets.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="c2f0a-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="c2f0a-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2f0a-146">OUTPUTS</span></span>

### <span data-ttu-id="c2f0a-147">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c2f0a-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="c2f0a-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2f0a-148">NOTES</span></span>

<span data-ttu-id="c2f0a-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c2f0a-149">ALIASES</span></span>

<span data-ttu-id="c2f0a-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c2f0a-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c2f0a-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2f0a-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c2f0a-153">FIREWALLRULE <IFirewallRule[]>: получает или настраивает правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="c2f0a-154">`[EndIPAddress <String>]`. Возвращает или устанавливает конечный IP-адрес диапазона правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="c2f0a-155">`[RuleName <String>]`: получает или задает имя правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="c2f0a-156">`[StartIPAddress <String>]`: получает или устанавливает IP-адрес запуска в диапазоне правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="c2f0a-157">INPUTOBJECT <IBlockchainIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="c2f0a-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c2f0a-158">`[BlockchainMemberName <String>]`: Имя участника.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="c2f0a-159">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="c2f0a-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2f0a-160">`[Location <String>]`: имя расположения.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="c2f0a-161">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="c2f0a-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c2f0a-163">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c2f0a-164">`[SubscriptionId <String>]`: получает идентификатор подписки, однозначно определяя подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c2f0a-165">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="c2f0a-166">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="c2f0a-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="c2f0a-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2f0a-167">RELATED LINKS</span></span>

