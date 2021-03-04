---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 418786855833164c3f9c15dcd2716ad00c8c6d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954872"
---
# <span data-ttu-id="476c6-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="476c6-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="476c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="476c6-102">SYNOPSIS</span></span>
<span data-ttu-id="476c6-103">Повторно сгенерировать ключи API для участника.</span><span class="sxs-lookup"><span data-stu-id="476c6-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="476c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="476c6-104">SYNTAX</span></span>

### <span data-ttu-id="476c6-105">RegenerateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="476c6-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="476c6-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="476c6-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="476c6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="476c6-107">DESCRIPTION</span></span>
<span data-ttu-id="476c6-108">Повторно сгенерировать ключи API для участника.</span><span class="sxs-lookup"><span data-stu-id="476c6-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="476c6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="476c6-109">EXAMPLES</span></span>

### <span data-ttu-id="476c6-110">Пример 1. Повторное сгенерировать ключи API для узла транзакции с использованием имени.</span><span class="sxs-lookup"><span data-stu-id="476c6-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="476c6-111">Эта команда создает ключи API для узла транзакции с использованием имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="476c6-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="476c6-112">Пример 2. Повторное сгенерировать ключи API для узла транзакции</span><span class="sxs-lookup"><span data-stu-id="476c6-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="476c6-113">Эта команда создает ключи API для узла транзакции с использованием idenity.</span><span class="sxs-lookup"><span data-stu-id="476c6-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="476c6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="476c6-114">PARAMETERS</span></span>

### <span data-ttu-id="476c6-115">-ДолжныеИмяЯ</span><span class="sxs-lookup"><span data-stu-id="476c6-115">-BlockchainMemberName</span></span>
<span data-ttu-id="476c6-116">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="476c6-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476c6-117">-DefaultProfile</span></span>
<span data-ttu-id="476c6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="476c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="476c6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="476c6-119">-InputObject</span></span>
<span data-ttu-id="476c6-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="476c6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="476c6-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="476c6-121">-KeyName</span></span>
<span data-ttu-id="476c6-122">Возвращает или задает имя ключа API.</span><span class="sxs-lookup"><span data-stu-id="476c6-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="476c6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="476c6-123">-ResourceGroupName</span></span>
<span data-ttu-id="476c6-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="476c6-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="476c6-125">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="476c6-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476c6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="476c6-126">-SubscriptionId</span></span>
<span data-ttu-id="476c6-127">Возвращает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="476c6-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="476c6-128">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="476c6-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476c6-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="476c6-129">-TransactionNodeName</span></span>
<span data-ttu-id="476c6-130">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="476c6-130">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476c6-131">-Value</span><span class="sxs-lookup"><span data-stu-id="476c6-131">-Value</span></span>
<span data-ttu-id="476c6-132">Возвращает или задает значение ключа API.</span><span class="sxs-lookup"><span data-stu-id="476c6-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="476c6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="476c6-133">-Confirm</span></span>
<span data-ttu-id="476c6-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="476c6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="476c6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="476c6-135">-WhatIf</span></span>
<span data-ttu-id="476c6-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="476c6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="476c6-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="476c6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="476c6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476c6-138">CommonParameters</span></span>
<span data-ttu-id="476c6-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476c6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476c6-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="476c6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476c6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="476c6-141">INPUTS</span></span>

### <span data-ttu-id="476c6-142">Microsoft.Azure.PowerShell.Cmdlets.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="476c6-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="476c6-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="476c6-143">OUTPUTS</span></span>

### <span data-ttu-id="476c6-144">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="476c6-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="476c6-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="476c6-145">NOTES</span></span>

<span data-ttu-id="476c6-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="476c6-146">ALIASES</span></span>

<span data-ttu-id="476c6-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="476c6-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="476c6-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="476c6-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="476c6-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="476c6-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="476c6-150">INPUTOBJECT <IBlockchainIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="476c6-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="476c6-151">`[BlockchainMemberName <String>]`: Имя участника.</span><span class="sxs-lookup"><span data-stu-id="476c6-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="476c6-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="476c6-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="476c6-153">`[Location <String>]`: имя расположения.</span><span class="sxs-lookup"><span data-stu-id="476c6-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="476c6-154">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="476c6-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="476c6-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="476c6-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="476c6-156">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="476c6-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="476c6-157">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="476c6-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="476c6-158">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="476c6-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="476c6-159">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="476c6-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="476c6-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="476c6-160">RELATED LINKS</span></span>

