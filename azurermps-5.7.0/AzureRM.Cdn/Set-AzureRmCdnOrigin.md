---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 179b4b028c7dd9338e75d07f559a61052b3d2bcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559243"
---
# <span data-ttu-id="b84cb-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b84cb-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="b84cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b84cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b84cb-103">Обновляет сервер источника CDN.</span><span class="sxs-lookup"><span data-stu-id="b84cb-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b84cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b84cb-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b84cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b84cb-105">DESCRIPTION</span></span>
<span data-ttu-id="b84cb-106">Командлет **Set-AzureRmCdnOrigin** обновляет сервер происхождения сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="b84cb-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="b84cb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b84cb-107">EXAMPLES</span></span>

## <span data-ttu-id="b84cb-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b84cb-108">PARAMETERS</span></span>

### <span data-ttu-id="b84cb-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b84cb-109">-CdnOrigin</span></span>
<span data-ttu-id="b84cb-110">Указывает исходный сервер, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b84cb-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: PSOrigin
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b84cb-111">-DefaultProfile</span></span>
<span data-ttu-id="b84cb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b84cb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84cb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84cb-113">CommonParameters</span></span>
<span data-ttu-id="b84cb-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b84cb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84cb-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b84cb-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84cb-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b84cb-116">INPUTS</span></span>

### <span data-ttu-id="b84cb-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="b84cb-117">PSOrigin</span></span>
<span data-ttu-id="b84cb-118">Параметр "CdnOrigin'" принимает значение типа "PSOrigin'" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b84cb-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="b84cb-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b84cb-119">OUTPUTS</span></span>

### <span data-ttu-id="b84cb-120">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="b84cb-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b84cb-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="b84cb-121">NOTES</span></span>

## <span data-ttu-id="b84cb-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b84cb-122">RELATED LINKS</span></span>

[<span data-ttu-id="b84cb-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b84cb-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


