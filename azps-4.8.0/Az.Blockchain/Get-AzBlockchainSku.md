---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080051"
---
# <span data-ttu-id="b4ffd-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="b4ffd-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="b4ffd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ffd-103">Список конфигураций типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4ffd-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="b4ffd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4ffd-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b4ffd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ffd-106">Список конфигураций типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4ffd-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="b4ffd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4ffd-107">EXAMPLES</span></span>

### <span data-ttu-id="b4ffd-108">Пример 1: список SKU для подписки</span><span class="sxs-lookup"><span data-stu-id="b4ffd-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="b4ffd-109">Эта команда перечисляет SKU для подписки.</span><span class="sxs-lookup"><span data-stu-id="b4ffd-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="b4ffd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4ffd-110">PARAMETERS</span></span>

### <span data-ttu-id="b4ffd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ffd-111">-DefaultProfile</span></span>
<span data-ttu-id="b4ffd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ffd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ffd-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4ffd-113">-SubscriptionId</span></span>
<span data-ttu-id="b4ffd-114">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ffd-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b4ffd-115">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b4ffd-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b4ffd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ffd-116">CommonParameters</span></span>
<span data-ttu-id="b4ffd-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4ffd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ffd-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4ffd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ffd-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4ffd-119">INPUTS</span></span>

## <span data-ttu-id="b4ffd-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4ffd-120">OUTPUTS</span></span>

### <span data-ttu-id="b4ffd-121">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="b4ffd-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="b4ffd-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4ffd-122">NOTES</span></span>

<span data-ttu-id="b4ffd-123">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="b4ffd-123">ALIASES</span></span>

## <span data-ttu-id="b4ffd-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4ffd-124">RELATED LINKS</span></span>

