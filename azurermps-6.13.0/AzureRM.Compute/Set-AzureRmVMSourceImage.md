---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: c164d352256f84ea18c09b775c9a9639dbde7866
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564640"
---
# <span data-ttu-id="4beab-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="4beab-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="4beab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4beab-102">SYNOPSIS</span></span>
<span data-ttu-id="4beab-103">Указывает изображение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4beab-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4beab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4beab-104">SYNTAX</span></span>

### <span data-ttu-id="4beab-105">ImageReferenceSkuParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4beab-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4beab-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4beab-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4beab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4beab-107">DESCRIPTION</span></span>
<span data-ttu-id="4beab-108">Командлет **Set-AzureRmVMSourceImage** указывает изображение платформы, используемое для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4beab-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="4beab-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4beab-109">EXAMPLES</span></span>

### <span data-ttu-id="4beab-110">Пример 1: Настройка значений для изображения</span><span class="sxs-lookup"><span data-stu-id="4beab-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="4beab-111">Первая команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4beab-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4beab-112">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4beab-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4beab-113">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4beab-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4beab-114">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4beab-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4beab-115">Последняя команда задает значения для имени издателя, предложения, SKU и версии.</span><span class="sxs-lookup"><span data-stu-id="4beab-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="4beab-116">Командлеты **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** и **Get-AzureRmVMImage** могут определить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="4beab-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="4beab-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4beab-117">PARAMETERS</span></span>

### <span data-ttu-id="4beab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4beab-118">-DefaultProfile</span></span>
<span data-ttu-id="4beab-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4beab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4beab-120">-ID</span><span class="sxs-lookup"><span data-stu-id="4beab-120">-Id</span></span>
<span data-ttu-id="4beab-121">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="4beab-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4beab-122">-Предложение</span><span class="sxs-lookup"><span data-stu-id="4beab-122">-Offer</span></span>
<span data-ttu-id="4beab-123">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="4beab-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="4beab-124">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="4beab-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4beab-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4beab-125">-PublisherName</span></span>
<span data-ttu-id="4beab-126">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="4beab-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="4beab-127">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="4beab-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4beab-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="4beab-128">-Skus</span></span>
<span data-ttu-id="4beab-129">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="4beab-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="4beab-130">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="4beab-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4beab-131">-Version</span><span class="sxs-lookup"><span data-stu-id="4beab-131">-Version</span></span>
<span data-ttu-id="4beab-132">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="4beab-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="4beab-133">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="4beab-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4beab-134">-VM</span><span class="sxs-lookup"><span data-stu-id="4beab-134">-VM</span></span>
<span data-ttu-id="4beab-135">Указывает локальный объект виртуальной машины для настройки.</span><span class="sxs-lookup"><span data-stu-id="4beab-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4beab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4beab-136">CommonParameters</span></span>
<span data-ttu-id="4beab-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4beab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4beab-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4beab-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4beab-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4beab-139">INPUTS</span></span>

### <span data-ttu-id="4beab-140">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4beab-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4beab-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4beab-141">System.String</span></span>

## <span data-ttu-id="4beab-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4beab-142">OUTPUTS</span></span>

### <span data-ttu-id="4beab-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4beab-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4beab-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="4beab-144">NOTES</span></span>

## <span data-ttu-id="4beab-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4beab-145">RELATED LINKS</span></span>

[<span data-ttu-id="4beab-146">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4beab-146">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="4beab-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4beab-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4beab-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4beab-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4beab-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4beab-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4beab-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4beab-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="4beab-151">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4beab-151">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


