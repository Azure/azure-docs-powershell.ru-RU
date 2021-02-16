---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212025"
---
# <span data-ttu-id="24da4-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="24da4-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="24da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24da4-102">SYNOPSIS</span></span>
<span data-ttu-id="24da4-103">Создайте участника-участника.</span><span class="sxs-lookup"><span data-stu-id="24da4-103">Create a blockchain member.</span></span>

## <span data-ttu-id="24da4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24da4-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24da4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24da4-105">DESCRIPTION</span></span>
<span data-ttu-id="24da4-106">Создайте участника-участника.</span><span class="sxs-lookup"><span data-stu-id="24da4-106">Create a blockchain member.</span></span>

## <span data-ttu-id="24da4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24da4-107">EXAMPLES</span></span>

### <span data-ttu-id="24da4-108">Пример 1. Создание нового участника</span><span class="sxs-lookup"><span data-stu-id="24da4-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="24da4-109">Эта команда создает нового участника группы.</span><span class="sxs-lookup"><span data-stu-id="24da4-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="24da4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24da4-110">PARAMETERS</span></span>

### <span data-ttu-id="24da4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24da4-111">-AsJob</span></span>
<span data-ttu-id="24da4-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="24da4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="24da4-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="24da4-113">-Consortium</span></span>
<span data-ttu-id="24da4-114">Получает или задает в качестве участника-участника от компании-участника или задает его для него.</span><span class="sxs-lookup"><span data-stu-id="24da4-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="24da4-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="24da4-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="24da4-116">Задает пароль учетной записи для управления управляемым консорциумом.</span><span class="sxs-lookup"><span data-stu-id="24da4-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="24da4-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="24da4-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="24da4-118">Возвращает отображаемую имя участника в составе отл.</span><span class="sxs-lookup"><span data-stu-id="24da4-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="24da4-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="24da4-119">-ConsortiumRole</span></span>
<span data-ttu-id="24da4-120">Получает роль участника в консорциуме.</span><span class="sxs-lookup"><span data-stu-id="24da4-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="24da4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24da4-121">-DefaultProfile</span></span>
<span data-ttu-id="24da4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24da4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24da4-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="24da4-123">-FirewallRule</span></span>
<span data-ttu-id="24da4-124">Получает или устанавливает правила брандмауэра Для создания, см. раздел "ЗАМЕТКИ" для свойств FIREWALLRULE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="24da4-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="24da4-125">-Location</span><span class="sxs-lookup"><span data-stu-id="24da4-125">-Location</span></span>
<span data-ttu-id="24da4-126">Расположение службы GEO службы-службы.</span><span class="sxs-lookup"><span data-stu-id="24da4-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="24da4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="24da4-127">-Name</span></span>
<span data-ttu-id="24da4-128">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="24da4-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="24da4-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="24da4-129">-NoWait</span></span>
<span data-ttu-id="24da4-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="24da4-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="24da4-131">-Password</span><span class="sxs-lookup"><span data-stu-id="24da4-131">-Password</span></span>
<span data-ttu-id="24da4-132">Задает базовый пароль для пароля участника группы.</span><span class="sxs-lookup"><span data-stu-id="24da4-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="24da4-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="24da4-133">-Protocol</span></span>
<span data-ttu-id="24da4-134">Возвращает или устанавливает протокол протокола-протокола.</span><span class="sxs-lookup"><span data-stu-id="24da4-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="24da4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24da4-135">-ResourceGroupName</span></span>
<span data-ttu-id="24da4-136">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="24da4-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="24da4-137">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="24da4-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="24da4-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="24da4-138">-Sku</span></span>
<span data-ttu-id="24da4-139">Получает или задает имя SKU</span><span class="sxs-lookup"><span data-stu-id="24da4-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="24da4-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="24da4-140">-SkuTier</span></span>
<span data-ttu-id="24da4-141">Получает или задает уровень SKU</span><span class="sxs-lookup"><span data-stu-id="24da4-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="24da4-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24da4-142">-SubscriptionId</span></span>
<span data-ttu-id="24da4-143">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24da4-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="24da4-144">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="24da4-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="24da4-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="24da4-145">-Tag</span></span>
<span data-ttu-id="24da4-146">Теги службы, которые являются списком пар ключевых значений, описывают ресурс.</span><span class="sxs-lookup"><span data-stu-id="24da4-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="24da4-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="24da4-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="24da4-148">Получает или задает емкость узлов.</span><span class="sxs-lookup"><span data-stu-id="24da4-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="24da4-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24da4-149">-Confirm</span></span>
<span data-ttu-id="24da4-150">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="24da4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24da4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24da4-151">-WhatIf</span></span>
<span data-ttu-id="24da4-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24da4-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24da4-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="24da4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24da4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24da4-154">CommonParameters</span></span>
<span data-ttu-id="24da4-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24da4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24da4-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24da4-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24da4-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24da4-157">INPUTS</span></span>

## <span data-ttu-id="24da4-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24da4-158">OUTPUTS</span></span>

### <span data-ttu-id="24da4-159">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="24da4-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="24da4-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24da4-160">NOTES</span></span>

<span data-ttu-id="24da4-161">ALIASES</span><span class="sxs-lookup"><span data-stu-id="24da4-161">ALIASES</span></span>

<span data-ttu-id="24da4-162">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="24da4-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24da4-163">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="24da4-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24da4-164">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24da4-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24da4-165">FIREWALLRULE <IFirewallRule[]>: получает или устанавливает правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="24da4-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="24da4-166">`[EndIPAddress <String>]`. Возвращает или устанавливает конечный IP-адрес диапазона правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="24da4-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="24da4-167">`[RuleName <String>]`: получает или задает имя правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="24da4-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="24da4-168">`[StartIPAddress <String>]`: получает или устанавливает IP-адрес запуска в диапазоне правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="24da4-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="24da4-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24da4-169">RELATED LINKS</span></span>

