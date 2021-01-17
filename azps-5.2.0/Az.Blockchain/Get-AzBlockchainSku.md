---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399055"
---
# <span data-ttu-id="47839-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="47839-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="47839-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47839-102">SYNOPSIS</span></span>
<span data-ttu-id="47839-103">В этой области перечислены skus этого типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47839-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="47839-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47839-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="47839-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47839-105">DESCRIPTION</span></span>
<span data-ttu-id="47839-106">В этой области перечислены skus этого типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47839-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="47839-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47839-107">EXAMPLES</span></span>

### <span data-ttu-id="47839-108">Пример 1. SKU списка для подписки</span><span class="sxs-lookup"><span data-stu-id="47839-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="47839-109">Эта команда содержит SKU подписки.</span><span class="sxs-lookup"><span data-stu-id="47839-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="47839-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47839-110">PARAMETERS</span></span>

### <span data-ttu-id="47839-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47839-111">-DefaultProfile</span></span>
<span data-ttu-id="47839-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47839-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47839-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47839-113">-SubscriptionId</span></span>
<span data-ttu-id="47839-114">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47839-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="47839-115">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="47839-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47839-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47839-116">CommonParameters</span></span>
<span data-ttu-id="47839-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47839-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47839-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47839-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47839-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47839-119">INPUTS</span></span>

## <span data-ttu-id="47839-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47839-120">OUTPUTS</span></span>

### <span data-ttu-id="47839-121">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="47839-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="47839-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47839-122">NOTES</span></span>

<span data-ttu-id="47839-123">ALIASES</span><span class="sxs-lookup"><span data-stu-id="47839-123">ALIASES</span></span>

## <span data-ttu-id="47839-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47839-124">RELATED LINKS</span></span>

