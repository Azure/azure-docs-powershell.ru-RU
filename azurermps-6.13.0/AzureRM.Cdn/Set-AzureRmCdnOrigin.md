---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 395ee4b20ae2c26d05ad66489b3c643d0f4245a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565884"
---
# <span data-ttu-id="35f87-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="35f87-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="35f87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35f87-102">SYNOPSIS</span></span>
<span data-ttu-id="35f87-103">Обновляет сервер источника CDN.</span><span class="sxs-lookup"><span data-stu-id="35f87-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35f87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35f87-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35f87-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35f87-105">DESCRIPTION</span></span>
<span data-ttu-id="35f87-106">Командлет **Set-AzureRmCdnOrigin** обновляет сервер происхождения сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="35f87-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="35f87-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35f87-107">EXAMPLES</span></span>

## <span data-ttu-id="35f87-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35f87-108">PARAMETERS</span></span>

### <span data-ttu-id="35f87-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="35f87-109">-CdnOrigin</span></span>
<span data-ttu-id="35f87-110">Указывает исходный сервер, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="35f87-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="35f87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f87-111">-DefaultProfile</span></span>
<span data-ttu-id="35f87-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="35f87-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f87-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f87-113">CommonParameters</span></span>
<span data-ttu-id="35f87-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35f87-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f87-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35f87-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f87-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35f87-116">INPUTS</span></span>

### <span data-ttu-id="35f87-117">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="35f87-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>
<span data-ttu-id="35f87-118">Параметры: CdnOrigin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="35f87-118">Parameters: CdnOrigin (ByValue)</span></span>

## <span data-ttu-id="35f87-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35f87-119">OUTPUTS</span></span>

### <span data-ttu-id="35f87-120">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="35f87-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="35f87-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="35f87-121">NOTES</span></span>

## <span data-ttu-id="35f87-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35f87-122">RELATED LINKS</span></span>

[<span data-ttu-id="35f87-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="35f87-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


