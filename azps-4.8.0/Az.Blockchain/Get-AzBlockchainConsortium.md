---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078486"
---
# <span data-ttu-id="cf448-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="cf448-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="cf448-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf448-102">SYNOPSIS</span></span>
<span data-ttu-id="cf448-103">Список доступных для подписки консорциумов.</span><span class="sxs-lookup"><span data-stu-id="cf448-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="cf448-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf448-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf448-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf448-105">DESCRIPTION</span></span>
<span data-ttu-id="cf448-106">Список доступных для подписки консорциумов.</span><span class="sxs-lookup"><span data-stu-id="cf448-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="cf448-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf448-107">EXAMPLES</span></span>

### <span data-ttu-id="cf448-108">Пример 1: получение Blockchainных консорциумов.</span><span class="sxs-lookup"><span data-stu-id="cf448-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="cf448-109">Эта команда перечисляет консорциумы по подписке для определенного местоположения.</span><span class="sxs-lookup"><span data-stu-id="cf448-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="cf448-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf448-110">PARAMETERS</span></span>

### <span data-ttu-id="cf448-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf448-111">-DefaultProfile</span></span>
<span data-ttu-id="cf448-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf448-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf448-113">-Location</span><span class="sxs-lookup"><span data-stu-id="cf448-113">-Location</span></span>
<span data-ttu-id="cf448-114">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="cf448-114">Location Name.</span></span>

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

### <span data-ttu-id="cf448-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf448-115">-SubscriptionId</span></span>
<span data-ttu-id="cf448-116">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf448-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf448-117">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="cf448-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cf448-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf448-118">-Confirm</span></span>
<span data-ttu-id="cf448-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf448-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf448-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf448-120">-WhatIf</span></span>
<span data-ttu-id="cf448-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf448-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf448-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf448-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf448-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf448-123">CommonParameters</span></span>
<span data-ttu-id="cf448-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf448-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf448-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf448-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf448-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf448-126">INPUTS</span></span>

## <span data-ttu-id="cf448-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf448-127">OUTPUTS</span></span>

### <span data-ttu-id="cf448-128">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="cf448-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="cf448-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf448-129">NOTES</span></span>

<span data-ttu-id="cf448-130">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="cf448-130">ALIASES</span></span>

## <span data-ttu-id="cf448-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf448-131">RELATED LINKS</span></span>

