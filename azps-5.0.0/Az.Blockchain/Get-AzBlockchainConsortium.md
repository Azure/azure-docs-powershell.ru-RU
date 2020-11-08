---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249561"
---
# <span data-ttu-id="116cc-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="116cc-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="116cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="116cc-102">SYNOPSIS</span></span>
<span data-ttu-id="116cc-103">Список доступных для подписки консорциумов.</span><span class="sxs-lookup"><span data-stu-id="116cc-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="116cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="116cc-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="116cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="116cc-105">DESCRIPTION</span></span>
<span data-ttu-id="116cc-106">Список доступных для подписки консорциумов.</span><span class="sxs-lookup"><span data-stu-id="116cc-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="116cc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="116cc-107">EXAMPLES</span></span>

### <span data-ttu-id="116cc-108">Пример 1: получение Blockchainных консорциумов.</span><span class="sxs-lookup"><span data-stu-id="116cc-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="116cc-109">Эта команда перечисляет консорциумы по подписке для определенного местоположения.</span><span class="sxs-lookup"><span data-stu-id="116cc-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="116cc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="116cc-110">PARAMETERS</span></span>

### <span data-ttu-id="116cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116cc-111">-DefaultProfile</span></span>
<span data-ttu-id="116cc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="116cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116cc-113">-Location</span><span class="sxs-lookup"><span data-stu-id="116cc-113">-Location</span></span>
<span data-ttu-id="116cc-114">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="116cc-114">Location Name.</span></span>

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

### <span data-ttu-id="116cc-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="116cc-115">-SubscriptionId</span></span>
<span data-ttu-id="116cc-116">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="116cc-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="116cc-117">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="116cc-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="116cc-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="116cc-118">-Confirm</span></span>
<span data-ttu-id="116cc-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="116cc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="116cc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116cc-120">-WhatIf</span></span>
<span data-ttu-id="116cc-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="116cc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="116cc-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="116cc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="116cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116cc-123">CommonParameters</span></span>
<span data-ttu-id="116cc-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="116cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116cc-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="116cc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116cc-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="116cc-126">INPUTS</span></span>

## <span data-ttu-id="116cc-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="116cc-127">OUTPUTS</span></span>

### <span data-ttu-id="116cc-128">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="116cc-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="116cc-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="116cc-129">NOTES</span></span>

<span data-ttu-id="116cc-130">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="116cc-130">ALIASES</span></span>

## <span data-ttu-id="116cc-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="116cc-131">RELATED LINKS</span></span>

