---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079158"
---
# <span data-ttu-id="be4cf-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="be4cf-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="be4cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="be4cf-103">Повторно создайте ключи API для элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="be4cf-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="be4cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be4cf-104">SYNTAX</span></span>

### <span data-ttu-id="be4cf-105">RegenerateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be4cf-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="be4cf-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="be4cf-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be4cf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be4cf-107">DESCRIPTION</span></span>
<span data-ttu-id="be4cf-108">Повторно создайте ключи API для элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="be4cf-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="be4cf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be4cf-109">EXAMPLES</span></span>

### <span data-ttu-id="be4cf-110">Пример 1: повторное создание ключей API для узла транзакции с помощью имени.</span><span class="sxs-lookup"><span data-stu-id="be4cf-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="be4cf-111">Эта команда создает ключи API для узла транзакции, используя имя, группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be4cf-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="be4cf-112">Пример 2: повторное создание ключей API для узла транзакции</span><span class="sxs-lookup"><span data-stu-id="be4cf-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="be4cf-113">Эта команда создает ключи API для узла транзакции с помощью idenity.</span><span class="sxs-lookup"><span data-stu-id="be4cf-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="be4cf-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be4cf-114">PARAMETERS</span></span>

### <span data-ttu-id="be4cf-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="be4cf-115">-BlockchainMemberName</span></span>
<span data-ttu-id="be4cf-116">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="be4cf-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="be4cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be4cf-117">-DefaultProfile</span></span>
<span data-ttu-id="be4cf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be4cf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be4cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be4cf-119">-InputObject</span></span>
<span data-ttu-id="be4cf-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="be4cf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="be4cf-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="be4cf-121">-KeyName</span></span>
<span data-ttu-id="be4cf-122">Возвращает или задает имя ключа API.</span><span class="sxs-lookup"><span data-stu-id="be4cf-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="be4cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be4cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="be4cf-124">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="be4cf-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="be4cf-125">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="be4cf-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="be4cf-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be4cf-126">-SubscriptionId</span></span>
<span data-ttu-id="be4cf-127">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be4cf-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="be4cf-128">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="be4cf-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="be4cf-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="be4cf-129">-TransactionNodeName</span></span>
<span data-ttu-id="be4cf-130">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="be4cf-130">Transaction node name.</span></span>

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

### <span data-ttu-id="be4cf-131">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="be4cf-131">-Value</span></span>
<span data-ttu-id="be4cf-132">Возвращает или задает значение ключа API.</span><span class="sxs-lookup"><span data-stu-id="be4cf-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="be4cf-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be4cf-133">-Confirm</span></span>
<span data-ttu-id="be4cf-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be4cf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be4cf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be4cf-135">-WhatIf</span></span>
<span data-ttu-id="be4cf-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be4cf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be4cf-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be4cf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be4cf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be4cf-138">CommonParameters</span></span>
<span data-ttu-id="be4cf-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be4cf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be4cf-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be4cf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be4cf-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be4cf-141">INPUTS</span></span>

### <span data-ttu-id="be4cf-142">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="be4cf-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="be4cf-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be4cf-143">OUTPUTS</span></span>

### <span data-ttu-id="be4cf-144">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="be4cf-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="be4cf-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="be4cf-145">NOTES</span></span>

<span data-ttu-id="be4cf-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="be4cf-146">ALIASES</span></span>

<span data-ttu-id="be4cf-147">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="be4cf-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be4cf-148">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be4cf-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be4cf-149">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be4cf-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be4cf-150">INPUTOBJECT <IBlockchainIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="be4cf-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be4cf-151">`[BlockchainMemberName <String>]`: Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="be4cf-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="be4cf-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="be4cf-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be4cf-153">`[Location <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="be4cf-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="be4cf-154">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="be4cf-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="be4cf-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="be4cf-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="be4cf-156">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="be4cf-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="be4cf-157">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be4cf-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="be4cf-158">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="be4cf-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="be4cf-159">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="be4cf-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="be4cf-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be4cf-160">RELATED LINKS</span></span>

