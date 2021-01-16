---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509481"
---
# <span data-ttu-id="ae019-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="ae019-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="ae019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae019-102">SYNOPSIS</span></span>
<span data-ttu-id="ae019-103">Перечислите ключи API для узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae019-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="ae019-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae019-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ae019-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae019-105">DESCRIPTION</span></span>
<span data-ttu-id="ae019-106">Перечислите ключи API для узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae019-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="ae019-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae019-107">EXAMPLES</span></span>

### <span data-ttu-id="ae019-108">Пример 1. Клавиши API списка для узла транзакции</span><span class="sxs-lookup"><span data-stu-id="ae019-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="ae019-109">Эта команда содержит клавиши API для узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae019-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="ae019-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae019-110">PARAMETERS</span></span>

### <span data-ttu-id="ae019-111">-ДолжныеИмяЯ</span><span class="sxs-lookup"><span data-stu-id="ae019-111">-BlockchainMemberName</span></span>
<span data-ttu-id="ae019-112">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="ae019-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="ae019-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae019-113">-DefaultProfile</span></span>
<span data-ttu-id="ae019-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae019-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae019-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae019-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae019-116">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="ae019-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ae019-117">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ae019-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ae019-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae019-118">-SubscriptionId</span></span>
<span data-ttu-id="ae019-119">Возвращает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae019-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ae019-120">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ae019-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae019-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="ae019-121">-TransactionNodeName</span></span>
<span data-ttu-id="ae019-122">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae019-122">Transaction node name.</span></span>

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

### <span data-ttu-id="ae019-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae019-123">-Confirm</span></span>
<span data-ttu-id="ae019-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae019-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae019-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae019-125">-WhatIf</span></span>
<span data-ttu-id="ae019-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae019-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae019-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ae019-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae019-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae019-128">CommonParameters</span></span>
<span data-ttu-id="ae019-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae019-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae019-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae019-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae019-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae019-131">INPUTS</span></span>

## <span data-ttu-id="ae019-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae019-132">OUTPUTS</span></span>

### <span data-ttu-id="ae019-133">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="ae019-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="ae019-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae019-134">NOTES</span></span>

<span data-ttu-id="ae019-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ae019-135">ALIASES</span></span>

## <span data-ttu-id="ae019-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae019-136">RELATED LINKS</span></span>

