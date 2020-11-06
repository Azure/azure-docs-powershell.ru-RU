---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: ccdc7ee8a63c0a633caf162f8549fd1ba737ce8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568631"
---
# <span data-ttu-id="6573e-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="6573e-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="6573e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6573e-102">SYNOPSIS</span></span>
<span data-ttu-id="6573e-103">Возвращает VMImage типы предложения.</span><span class="sxs-lookup"><span data-stu-id="6573e-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6573e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6573e-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="6573e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6573e-105">DESCRIPTION</span></span>
<span data-ttu-id="6573e-106">Командлет **Get-AzureRmVMImageOffer** получает типы предложений VMImage.</span><span class="sxs-lookup"><span data-stu-id="6573e-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="6573e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6573e-107">EXAMPLES</span></span>

### <span data-ttu-id="6573e-108">Пример 1: получение типов предложений для издателя</span><span class="sxs-lookup"><span data-stu-id="6573e-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="6573e-109">Эта команда получает типы предложений для указанного издателя в центральном регионе США.</span><span class="sxs-lookup"><span data-stu-id="6573e-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="6573e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6573e-110">PARAMETERS</span></span>

### <span data-ttu-id="6573e-111">-Location</span><span class="sxs-lookup"><span data-stu-id="6573e-111">-Location</span></span>
<span data-ttu-id="6573e-112">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="6573e-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="6573e-113">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6573e-113">-PublisherName</span></span>
<span data-ttu-id="6573e-114">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="6573e-114">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="6573e-115">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="6573e-115">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="6573e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6573e-116">CommonParameters</span></span>
<span data-ttu-id="6573e-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6573e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6573e-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6573e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6573e-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6573e-119">INPUTS</span></span>

### <span data-ttu-id="6573e-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="6573e-120">None</span></span>
<span data-ttu-id="6573e-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6573e-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6573e-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6573e-122">OUTPUTS</span></span>

## <span data-ttu-id="6573e-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="6573e-123">NOTES</span></span>

## <span data-ttu-id="6573e-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6573e-124">RELATED LINKS</span></span>

[<span data-ttu-id="6573e-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6573e-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="6573e-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6573e-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="6573e-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6573e-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="6573e-128">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6573e-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


