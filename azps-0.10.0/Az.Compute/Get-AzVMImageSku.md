---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: fad6c42c53e475343ad518c89dbb1a918a0f1e68
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911516"
---
# <span data-ttu-id="f0621-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f0621-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="f0621-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0621-102">SYNOPSIS</span></span>
<span data-ttu-id="f0621-103">Возвращает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="f0621-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="f0621-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0621-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0621-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0621-105">DESCRIPTION</span></span>
<span data-ttu-id="f0621-106">Командлет **Get-AzVMImageSku** получает VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="f0621-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="f0621-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0621-107">EXAMPLES</span></span>

### <span data-ttu-id="f0621-108">Пример 1: получение конфигураций VMImage</span><span class="sxs-lookup"><span data-stu-id="f0621-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="f0621-109">Эта команда возвращает SKU для указанного издателя и предложения.</span><span class="sxs-lookup"><span data-stu-id="f0621-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="f0621-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0621-110">PARAMETERS</span></span>

### <span data-ttu-id="f0621-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0621-111">-DefaultProfile</span></span>
<span data-ttu-id="f0621-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0621-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0621-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f0621-113">-Location</span></span>
<span data-ttu-id="f0621-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="f0621-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="f0621-115">-Предложение</span><span class="sxs-lookup"><span data-stu-id="f0621-115">-Offer</span></span>
<span data-ttu-id="f0621-116">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="f0621-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="f0621-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f0621-117">-PublisherName</span></span>
<span data-ttu-id="f0621-118">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="f0621-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="f0621-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0621-119">CommonParameters</span></span>
<span data-ttu-id="f0621-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0621-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0621-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0621-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0621-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0621-122">INPUTS</span></span>

### <span data-ttu-id="f0621-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="f0621-123">None</span></span>
<span data-ttu-id="f0621-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f0621-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0621-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0621-125">OUTPUTS</span></span>

### <span data-ttu-id="f0621-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="f0621-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="f0621-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0621-127">NOTES</span></span>

## <span data-ttu-id="f0621-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0621-128">RELATED LINKS</span></span>

[<span data-ttu-id="f0621-129">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f0621-129">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="f0621-130">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f0621-130">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="f0621-131">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f0621-131">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f0621-132">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f0621-132">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


