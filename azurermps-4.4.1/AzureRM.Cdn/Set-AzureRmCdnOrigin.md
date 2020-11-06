---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: c554caf7230b54db3e1161a20e001f9873f6dfff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565635"
---
# <span data-ttu-id="cf9fa-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="cf9fa-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="cf9fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9fa-103">Обновляет сервер источника CDN.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf9fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf9fa-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf9fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="cf9fa-106">Командлет **Set-AzureRmCdnOrigin** обновляет сервер происхождения сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="cf9fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf9fa-107">EXAMPLES</span></span>

## <span data-ttu-id="cf9fa-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf9fa-108">PARAMETERS</span></span>

### <span data-ttu-id="cf9fa-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="cf9fa-109">-CdnOrigin</span></span>
<span data-ttu-id="cf9fa-110">Указывает исходный сервер, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="cf9fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9fa-111">-DefaultProfile</span></span>
<span data-ttu-id="cf9fa-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf9fa-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9fa-113">CommonParameters</span></span>
<span data-ttu-id="cf9fa-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9fa-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf9fa-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9fa-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf9fa-116">INPUTS</span></span>

### <span data-ttu-id="cf9fa-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="cf9fa-117">PSOrigin</span></span>
<span data-ttu-id="cf9fa-118">Параметр "CdnOrigin'" принимает значение типа "PSOrigin'" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="cf9fa-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf9fa-119">OUTPUTS</span></span>

### <span data-ttu-id="cf9fa-120">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="cf9fa-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="cf9fa-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf9fa-121">NOTES</span></span>

## <span data-ttu-id="cf9fa-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf9fa-122">RELATED LINKS</span></span>

[<span data-ttu-id="cf9fa-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="cf9fa-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


