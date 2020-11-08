---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248639"
---
# <span data-ttu-id="8700f-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="8700f-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="8700f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8700f-102">SYNOPSIS</span></span>
<span data-ttu-id="8700f-103">Получение списка частных хранилищ</span><span class="sxs-lookup"><span data-stu-id="8700f-103">Get private store list</span></span>

## <span data-ttu-id="8700f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8700f-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8700f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8700f-105">DESCRIPTION</span></span>
<span data-ttu-id="8700f-106">Получение списка закрытого хранилища, созданного в рамках области клиента</span><span class="sxs-lookup"><span data-stu-id="8700f-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="8700f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8700f-107">EXAMPLES</span></span>

### <span data-ttu-id="8700f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8700f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="8700f-109">частный список хранилищ, созданный в области клиента</span><span class="sxs-lookup"><span data-stu-id="8700f-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="8700f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8700f-110">PARAMETERS</span></span>

### <span data-ttu-id="8700f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8700f-111">-DefaultProfile</span></span>
<span data-ttu-id="8700f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8700f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8700f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8700f-113">CommonParameters</span></span>
<span data-ttu-id="8700f-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8700f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8700f-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8700f-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8700f-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8700f-116">INPUTS</span></span>

### <span data-ttu-id="8700f-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="8700f-117">None</span></span>

## <span data-ttu-id="8700f-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8700f-118">OUTPUTS</span></span>

### <span data-ttu-id="8700f-119">Microsoft. Azure. Commands. Marketplace. Models. PrivateStore. PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="8700f-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="8700f-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="8700f-120">NOTES</span></span>

## <span data-ttu-id="8700f-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8700f-121">RELATED LINKS</span></span>
