---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: f299d0f299eaef61ba3655e8ec221cc55f5ab578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734479"
---
# <span data-ttu-id="94389-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="94389-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="94389-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94389-102">SYNOPSIS</span></span>
<span data-ttu-id="94389-103">Получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="94389-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94389-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94389-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [<CommonParameters>]
```

## <span data-ttu-id="94389-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94389-105">DESCRIPTION</span></span>
<span data-ttu-id="94389-106">Командлет **Get-AzureRmVMImagePublisher** получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="94389-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="94389-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94389-107">EXAMPLES</span></span>

### <span data-ttu-id="94389-108">Пример 1: получение VMImageных издателей для региона</span><span class="sxs-lookup"><span data-stu-id="94389-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="94389-109">Эта команда получает издателей экземпляров VMImage для Центральной области США в вашем профиле Azure.</span><span class="sxs-lookup"><span data-stu-id="94389-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="94389-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94389-110">PARAMETERS</span></span>

### <span data-ttu-id="94389-111">-Location</span><span class="sxs-lookup"><span data-stu-id="94389-111">-Location</span></span>
<span data-ttu-id="94389-112">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="94389-112">Specifies the location of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94389-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94389-113">CommonParameters</span></span>
<span data-ttu-id="94389-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94389-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94389-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94389-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94389-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94389-116">INPUTS</span></span>

### <span data-ttu-id="94389-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="94389-117">None</span></span>
<span data-ttu-id="94389-118">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="94389-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94389-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94389-119">OUTPUTS</span></span>

## <span data-ttu-id="94389-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="94389-120">NOTES</span></span>

## <span data-ttu-id="94389-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94389-121">RELATED LINKS</span></span>

[<span data-ttu-id="94389-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="94389-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="94389-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="94389-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="94389-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="94389-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="94389-125">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="94389-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


