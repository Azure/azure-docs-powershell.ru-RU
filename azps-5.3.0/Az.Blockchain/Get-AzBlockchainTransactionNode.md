---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519757"
---
# <span data-ttu-id="784e1-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="784e1-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="784e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="784e1-102">SYNOPSIS</span></span>
<span data-ttu-id="784e1-103">Получите сведения о узле транзакции.</span><span class="sxs-lookup"><span data-stu-id="784e1-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="784e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="784e1-104">SYNTAX</span></span>

### <span data-ttu-id="784e1-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="784e1-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="784e1-106">Получить</span><span class="sxs-lookup"><span data-stu-id="784e1-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="784e1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="784e1-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="784e1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="784e1-108">DESCRIPTION</span></span>
<span data-ttu-id="784e1-109">Получите сведения о узле транзакции.</span><span class="sxs-lookup"><span data-stu-id="784e1-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="784e1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="784e1-110">EXAMPLES</span></span>

### <span data-ttu-id="784e1-111">Пример 1. Узлы транзакций списка для участника-участника</span><span class="sxs-lookup"><span data-stu-id="784e1-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="784e1-112">Эта команда содержит узлы транзакций для участника- группы.</span><span class="sxs-lookup"><span data-stu-id="784e1-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="784e1-113">Пример 2. Получить узел транзакции</span><span class="sxs-lookup"><span data-stu-id="784e1-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="784e1-114">Эта команда получает узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="784e1-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="784e1-115">Пример 3. Получить узел транзакции</span><span class="sxs-lookup"><span data-stu-id="784e1-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="784e1-116">Эта команда получает узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="784e1-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="784e1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="784e1-117">PARAMETERS</span></span>

### <span data-ttu-id="784e1-118">-ЛесОИмяноИмя</span><span class="sxs-lookup"><span data-stu-id="784e1-118">-BlockchainMemberName</span></span>
<span data-ttu-id="784e1-119">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="784e1-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="784e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784e1-120">-DefaultProfile</span></span>
<span data-ttu-id="784e1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="784e1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="784e1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="784e1-122">-InputObject</span></span>
<span data-ttu-id="784e1-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="784e1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="784e1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="784e1-124">-Name</span></span>
<span data-ttu-id="784e1-125">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="784e1-125">Transaction node name.</span></span>

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

### <span data-ttu-id="784e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="784e1-127">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="784e1-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="784e1-128">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="784e1-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="784e1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="784e1-129">-SubscriptionId</span></span>
<span data-ttu-id="784e1-130">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="784e1-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="784e1-131">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="784e1-131">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="784e1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784e1-132">CommonParameters</span></span>
<span data-ttu-id="784e1-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="784e1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784e1-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="784e1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784e1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="784e1-135">INPUTS</span></span>

### <span data-ttu-id="784e1-136">Microsoft.Azure.PowerShell.Cmdlets.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="784e1-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="784e1-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="784e1-137">OUTPUTS</span></span>

### <span data-ttu-id="784e1-138">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="784e1-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="784e1-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="784e1-139">NOTES</span></span>

<span data-ttu-id="784e1-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="784e1-140">ALIASES</span></span>

<span data-ttu-id="784e1-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="784e1-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="784e1-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="784e1-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="784e1-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="784e1-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="784e1-144">INPUTOBJECT <IBlockchainIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="784e1-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="784e1-145">`[BlockchainMemberName <String>]`: Имя участника.</span><span class="sxs-lookup"><span data-stu-id="784e1-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="784e1-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="784e1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="784e1-147">`[Location <String>]`: имя расположения.</span><span class="sxs-lookup"><span data-stu-id="784e1-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="784e1-148">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="784e1-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="784e1-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="784e1-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="784e1-150">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="784e1-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="784e1-151">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="784e1-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="784e1-152">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="784e1-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="784e1-153">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="784e1-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="784e1-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="784e1-154">RELATED LINKS</span></span>

