---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249550"
---
# <span data-ttu-id="08696-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="08696-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="08696-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08696-102">SYNOPSIS</span></span>
<span data-ttu-id="08696-103">Получение сведений об узле "транзакция".</span><span class="sxs-lookup"><span data-stu-id="08696-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="08696-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08696-104">SYNTAX</span></span>

### <span data-ttu-id="08696-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08696-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="08696-106">Получить</span><span class="sxs-lookup"><span data-stu-id="08696-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="08696-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="08696-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="08696-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08696-108">DESCRIPTION</span></span>
<span data-ttu-id="08696-109">Получение сведений об узле "транзакция".</span><span class="sxs-lookup"><span data-stu-id="08696-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="08696-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08696-110">EXAMPLES</span></span>

### <span data-ttu-id="08696-111">Пример 1: список узлов транзакций для элемента blockchain</span><span class="sxs-lookup"><span data-stu-id="08696-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="08696-112">Эта команда перечисляет узлы транзакций для элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="08696-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="08696-113">Пример 2: получение узла транзакции</span><span class="sxs-lookup"><span data-stu-id="08696-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="08696-114">Эта команда получает узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="08696-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="08696-115">Пример 3: получение узла транзакции</span><span class="sxs-lookup"><span data-stu-id="08696-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="08696-116">Эта команда получает узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="08696-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="08696-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08696-117">PARAMETERS</span></span>

### <span data-ttu-id="08696-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="08696-118">-BlockchainMemberName</span></span>
<span data-ttu-id="08696-119">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="08696-119">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08696-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08696-120">-DefaultProfile</span></span>
<span data-ttu-id="08696-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08696-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08696-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08696-122">-InputObject</span></span>
<span data-ttu-id="08696-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="08696-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08696-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="08696-124">-Name</span></span>
<span data-ttu-id="08696-125">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="08696-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08696-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08696-126">-ResourceGroupName</span></span>
<span data-ttu-id="08696-127">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="08696-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="08696-128">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="08696-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08696-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08696-129">-SubscriptionId</span></span>
<span data-ttu-id="08696-130">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08696-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="08696-131">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="08696-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08696-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08696-132">CommonParameters</span></span>
<span data-ttu-id="08696-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08696-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08696-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08696-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08696-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08696-135">INPUTS</span></span>

### <span data-ttu-id="08696-136">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="08696-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="08696-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08696-137">OUTPUTS</span></span>

### <span data-ttu-id="08696-138">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="08696-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="08696-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="08696-139">NOTES</span></span>

<span data-ttu-id="08696-140">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="08696-140">ALIASES</span></span>

<span data-ttu-id="08696-141">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="08696-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="08696-142">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="08696-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08696-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="08696-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="08696-144">INPUTOBJECT <IBlockchainIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="08696-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="08696-145">`[BlockchainMemberName <String>]`: Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="08696-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="08696-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="08696-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="08696-147">`[Location <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="08696-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="08696-148">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="08696-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="08696-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="08696-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="08696-150">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="08696-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="08696-151">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08696-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="08696-152">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="08696-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="08696-153">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="08696-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="08696-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08696-154">RELATED LINKS</span></span>

