---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: d96d583f871e0d037c72018339d44952562bac35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559143"
---
# <span data-ttu-id="9c3eb-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="9c3eb-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="9c3eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3eb-103">Указывает изображение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c3eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c3eb-104">SYNTAX</span></span>

### <span data-ttu-id="9c3eb-105">ImageReferenceSkuParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c3eb-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [<CommonParameters>]
```

### <span data-ttu-id="9c3eb-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c3eb-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="9c3eb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c3eb-107">DESCRIPTION</span></span>
<span data-ttu-id="9c3eb-108">Командлет **Set-AzureRmVMSourceImage** указывает изображение платформы, используемое для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="9c3eb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c3eb-109">EXAMPLES</span></span>

### <span data-ttu-id="9c3eb-110">Пример 1: Настройка значений для изображения</span><span class="sxs-lookup"><span data-stu-id="9c3eb-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="9c3eb-111">Первая команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="9c3eb-112">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9c3eb-113">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9c3eb-114">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="9c3eb-115">Последняя команда задает значения для имени издателя, предложения, SKU и версии.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="9c3eb-116">Командлеты **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** и **Get-AzureRmVMImage** могут определить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="9c3eb-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c3eb-117">PARAMETERS</span></span>

### <span data-ttu-id="9c3eb-118">-ID</span><span class="sxs-lookup"><span data-stu-id="9c3eb-118">-Id</span></span>
<span data-ttu-id="9c3eb-119">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceIdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3eb-120">-Предложение</span><span class="sxs-lookup"><span data-stu-id="9c3eb-120">-Offer</span></span>
<span data-ttu-id="9c3eb-121">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-121">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="9c3eb-122">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3eb-123">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9c3eb-123">-PublisherName</span></span>
<span data-ttu-id="9c3eb-124">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="9c3eb-125">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3eb-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="9c3eb-126">-Skus</span></span>
<span data-ttu-id="9c3eb-127">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-127">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="9c3eb-128">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3eb-129">-Version</span><span class="sxs-lookup"><span data-stu-id="9c3eb-129">-Version</span></span>
<span data-ttu-id="9c3eb-130">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-130">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="9c3eb-131">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3eb-132">-VM</span><span class="sxs-lookup"><span data-stu-id="9c3eb-132">-VM</span></span>
<span data-ttu-id="9c3eb-133">Указывает локальный объект виртуальной машины для настройки.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-133">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3eb-134">CommonParameters</span></span>
<span data-ttu-id="9c3eb-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3eb-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c3eb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3eb-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c3eb-137">INPUTS</span></span>

### <span data-ttu-id="9c3eb-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c3eb-138">None</span></span>
<span data-ttu-id="9c3eb-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9c3eb-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c3eb-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c3eb-140">OUTPUTS</span></span>

## <span data-ttu-id="9c3eb-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c3eb-141">NOTES</span></span>

## <span data-ttu-id="9c3eb-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c3eb-142">RELATED LINKS</span></span>

[<span data-ttu-id="9c3eb-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9c3eb-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="9c3eb-144">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9c3eb-144">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="9c3eb-145">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9c3eb-145">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="9c3eb-146">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9c3eb-146">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="9c3eb-147">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9c3eb-147">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="9c3eb-148">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9c3eb-148">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


