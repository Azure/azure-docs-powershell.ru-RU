---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216028"
---
# <span data-ttu-id="bc953-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="bc953-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="bc953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc953-102">SYNOPSIS</span></span>
<span data-ttu-id="bc953-103">Получите сведения о участниках группы.</span><span class="sxs-lookup"><span data-stu-id="bc953-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="bc953-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc953-104">SYNTAX</span></span>

### <span data-ttu-id="bc953-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc953-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc953-106">Получить</span><span class="sxs-lookup"><span data-stu-id="bc953-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc953-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc953-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc953-108">Список</span><span class="sxs-lookup"><span data-stu-id="bc953-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc953-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc953-109">DESCRIPTION</span></span>
<span data-ttu-id="bc953-110">Получите сведения о участниках группы.</span><span class="sxs-lookup"><span data-stu-id="bc953-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="bc953-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc953-111">EXAMPLES</span></span>

### <span data-ttu-id="bc953-112">Пример 1. Участники списка</span><span class="sxs-lookup"><span data-stu-id="bc953-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="bc953-113">Эта команда содержит список участников, которые находятся в подписке.</span><span class="sxs-lookup"><span data-stu-id="bc953-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="bc953-114">Пример 2. Список участников</span><span class="sxs-lookup"><span data-stu-id="bc953-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="bc953-115">Эта команда содержит список участников группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc953-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="bc953-116">Пример 3. Получить участника группы</span><span class="sxs-lookup"><span data-stu-id="bc953-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="bc953-117">Эта команда возвращает участника в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc953-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="bc953-118">Пример 4. Получить участника группы</span><span class="sxs-lookup"><span data-stu-id="bc953-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="bc953-119">Эта команда возвращает участника в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc953-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="bc953-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc953-120">PARAMETERS</span></span>

### <span data-ttu-id="bc953-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc953-121">-DefaultProfile</span></span>
<span data-ttu-id="bc953-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc953-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc953-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc953-123">-InputObject</span></span>
<span data-ttu-id="bc953-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="bc953-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc953-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bc953-125">-Name</span></span>
<span data-ttu-id="bc953-126">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="bc953-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc953-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc953-127">-ResourceGroupName</span></span>
<span data-ttu-id="bc953-128">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="bc953-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bc953-129">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="bc953-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bc953-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc953-130">-SubscriptionId</span></span>
<span data-ttu-id="bc953-131">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc953-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="bc953-132">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="bc953-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc953-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc953-133">CommonParameters</span></span>
<span data-ttu-id="bc953-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc953-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc953-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc953-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc953-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc953-136">INPUTS</span></span>

### <span data-ttu-id="bc953-137">Microsoft.Azure.PowerShell.Cmdlets.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="bc953-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="bc953-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc953-138">OUTPUTS</span></span>

### <span data-ttu-id="bc953-139">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="bc953-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="bc953-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc953-140">NOTES</span></span>

<span data-ttu-id="bc953-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bc953-141">ALIASES</span></span>

<span data-ttu-id="bc953-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="bc953-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc953-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="bc953-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc953-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc953-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc953-145">INPUTOBJECT <IBlockchainIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="bc953-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc953-146">`[BlockchainMemberName <String>]`: Имя участника.</span><span class="sxs-lookup"><span data-stu-id="bc953-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="bc953-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="bc953-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc953-148">`[Location <String>]`: имя расположения.</span><span class="sxs-lookup"><span data-stu-id="bc953-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="bc953-149">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="bc953-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="bc953-150">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="bc953-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="bc953-151">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="bc953-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="bc953-152">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc953-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="bc953-153">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="bc953-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="bc953-154">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="bc953-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="bc953-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc953-155">RELATED LINKS</span></span>

