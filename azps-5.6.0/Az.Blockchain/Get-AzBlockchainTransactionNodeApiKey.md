---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: dbde273c1694f4622904ac00b261e902036c6e03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971459"
---
# <span data-ttu-id="56e38-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="56e38-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="56e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e38-102">SYNOPSIS</span></span>
<span data-ttu-id="56e38-103">Перечислите ключи API для узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="56e38-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="56e38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56e38-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="56e38-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56e38-105">DESCRIPTION</span></span>
<span data-ttu-id="56e38-106">Перечислите ключи API для узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="56e38-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="56e38-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56e38-107">EXAMPLES</span></span>

### <span data-ttu-id="56e38-108">Пример 1. Клавиши API списка для узла транзакции</span><span class="sxs-lookup"><span data-stu-id="56e38-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="56e38-109">Эта команда содержит перечень ключей API для узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="56e38-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="56e38-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56e38-110">PARAMETERS</span></span>

### <span data-ttu-id="56e38-111">-ЛесОИмяноИмя</span><span class="sxs-lookup"><span data-stu-id="56e38-111">-BlockchainMemberName</span></span>
<span data-ttu-id="56e38-112">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="56e38-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="56e38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e38-113">-DefaultProfile</span></span>
<span data-ttu-id="56e38-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56e38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56e38-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e38-115">-ResourceGroupName</span></span>
<span data-ttu-id="56e38-116">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="56e38-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="56e38-117">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="56e38-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="56e38-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56e38-118">-SubscriptionId</span></span>
<span data-ttu-id="56e38-119">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="56e38-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="56e38-120">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="56e38-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="56e38-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="56e38-121">-TransactionNodeName</span></span>
<span data-ttu-id="56e38-122">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="56e38-122">Transaction node name.</span></span>

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

### <span data-ttu-id="56e38-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56e38-123">-Confirm</span></span>
<span data-ttu-id="56e38-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e38-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e38-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e38-125">-WhatIf</span></span>
<span data-ttu-id="56e38-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e38-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e38-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56e38-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e38-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e38-128">CommonParameters</span></span>
<span data-ttu-id="56e38-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e38-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e38-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56e38-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e38-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56e38-131">INPUTS</span></span>

## <span data-ttu-id="56e38-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56e38-132">OUTPUTS</span></span>

### <span data-ttu-id="56e38-133">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="56e38-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="56e38-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56e38-134">NOTES</span></span>

<span data-ttu-id="56e38-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="56e38-135">ALIASES</span></span>

## <span data-ttu-id="56e38-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56e38-136">RELATED LINKS</span></span>

