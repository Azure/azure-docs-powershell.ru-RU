---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391052"
---
# <span data-ttu-id="ec652-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="ec652-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="ec652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec652-102">SYNOPSIS</span></span>
<span data-ttu-id="ec652-103">Получить список частного магазина</span><span class="sxs-lookup"><span data-stu-id="ec652-103">Get private store list</span></span>

## <span data-ttu-id="ec652-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec652-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec652-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec652-105">DESCRIPTION</span></span>
<span data-ttu-id="ec652-106">Получить список частного магазина, созданный в области клиента</span><span class="sxs-lookup"><span data-stu-id="ec652-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="ec652-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec652-107">EXAMPLES</span></span>

### <span data-ttu-id="ec652-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec652-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="ec652-109">Список частного магазина, созданный в области клиента</span><span class="sxs-lookup"><span data-stu-id="ec652-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="ec652-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec652-110">PARAMETERS</span></span>

### <span data-ttu-id="ec652-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec652-111">-DefaultProfile</span></span>
<span data-ttu-id="ec652-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec652-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec652-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec652-113">CommonParameters</span></span>
<span data-ttu-id="ec652-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec652-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec652-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec652-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec652-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec652-116">INPUTS</span></span>

### <span data-ttu-id="ec652-117">Нет</span><span class="sxs-lookup"><span data-stu-id="ec652-117">None</span></span>

## <span data-ttu-id="ec652-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec652-118">OUTPUTS</span></span>

### <span data-ttu-id="ec652-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="ec652-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="ec652-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec652-120">NOTES</span></span>

## <span data-ttu-id="ec652-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec652-121">RELATED LINKS</span></span>
