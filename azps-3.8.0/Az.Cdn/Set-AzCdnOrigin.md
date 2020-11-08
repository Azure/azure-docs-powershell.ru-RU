---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 9635031d6eaea5a7920a6862fb8cf20ce536c1db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072832"
---
# <span data-ttu-id="9614f-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9614f-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="9614f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9614f-102">SYNOPSIS</span></span>
<span data-ttu-id="9614f-103">Обновляет сервер источника CDN.</span><span class="sxs-lookup"><span data-stu-id="9614f-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="9614f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9614f-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9614f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9614f-105">DESCRIPTION</span></span>
<span data-ttu-id="9614f-106">Командлет **Set-AzCdnOrigin** обновляет сервер происхождения сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="9614f-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="9614f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9614f-107">EXAMPLES</span></span>

## <span data-ttu-id="9614f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9614f-108">PARAMETERS</span></span>

### <span data-ttu-id="9614f-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9614f-109">-CdnOrigin</span></span>
<span data-ttu-id="9614f-110">Указывает исходный сервер, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9614f-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9614f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9614f-111">-DefaultProfile</span></span>
<span data-ttu-id="9614f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9614f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9614f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9614f-113">CommonParameters</span></span>
<span data-ttu-id="9614f-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9614f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9614f-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9614f-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9614f-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9614f-116">INPUTS</span></span>

### <span data-ttu-id="9614f-117">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="9614f-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="9614f-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9614f-118">OUTPUTS</span></span>

### <span data-ttu-id="9614f-119">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="9614f-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="9614f-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="9614f-120">NOTES</span></span>

## <span data-ttu-id="9614f-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9614f-121">RELATED LINKS</span></span>

[<span data-ttu-id="9614f-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9614f-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


