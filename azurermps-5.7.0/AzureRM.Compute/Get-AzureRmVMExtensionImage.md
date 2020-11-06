---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: bae8fb04e71700d1572b8742f8cccbb2ebe8e331
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559204"
---
# <span data-ttu-id="fb8f4-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="fb8f4-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="fb8f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8f4-103">Возвращает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb8f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb8f4-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [<CommonParameters>]
```

## <span data-ttu-id="fb8f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb8f4-105">DESCRIPTION</span></span>
<span data-ttu-id="fb8f4-106">Командлет **Get-AzureRmVMExtensionImage** получает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="fb8f4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb8f4-107">EXAMPLES</span></span>

### <span data-ttu-id="fb8f4-108">Пример 1: получение версий изображения расширения</span><span class="sxs-lookup"><span data-stu-id="fb8f4-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="fb8f4-109">Эта команда получает все версии изображения расширения для указанных места, издателя и типа.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="fb8f4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb8f4-110">PARAMETERS</span></span>

### <span data-ttu-id="fb8f4-111">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="fb8f4-111">-FilterExpression</span></span>
<span data-ttu-id="fb8f4-112">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-112">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8f4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="fb8f4-113">-Location</span></span>
<span data-ttu-id="fb8f4-114">Указывает расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-114">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="fb8f4-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="fb8f4-115">-PublisherName</span></span>
<span data-ttu-id="fb8f4-116">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-116">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="fb8f4-117">Чтобы получить издатель расширения, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-117">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="fb8f4-118">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="fb8f4-118">-Type</span></span>
<span data-ttu-id="fb8f4-119">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-119">Specifies the type of the extension.</span></span>
<span data-ttu-id="fb8f4-120">Чтобы получить тип расширения, используйте командлет Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-120">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="fb8f4-121">-Version</span><span class="sxs-lookup"><span data-stu-id="fb8f4-121">-Version</span></span>
<span data-ttu-id="fb8f4-122">Указывает версию расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-122">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8f4-123">CommonParameters</span></span>
<span data-ttu-id="fb8f4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8f4-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb8f4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8f4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb8f4-126">INPUTS</span></span>

### <span data-ttu-id="fb8f4-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="fb8f4-127">None</span></span>
<span data-ttu-id="fb8f4-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb8f4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb8f4-129">OUTPUTS</span></span>

## <span data-ttu-id="fb8f4-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb8f4-130">NOTES</span></span>

## <span data-ttu-id="fb8f4-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb8f4-131">RELATED LINKS</span></span>

[<span data-ttu-id="fb8f4-132">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="fb8f4-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="fb8f4-133">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fb8f4-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="fb8f4-134">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fb8f4-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


