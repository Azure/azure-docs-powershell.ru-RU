---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236883"
---
# <span data-ttu-id="9e36d-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="9e36d-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="9e36d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e36d-102">SYNOPSIS</span></span>
<span data-ttu-id="9e36d-103">Указывает изображение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9e36d-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="9e36d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e36d-104">SYNTAX</span></span>

### <span data-ttu-id="9e36d-105">ImageReferenceSkuParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e36d-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e36d-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e36d-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e36d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e36d-107">DESCRIPTION</span></span>
<span data-ttu-id="9e36d-108">Командлет **Set-AzVMSourceImage** указывает изображение платформы, используемое для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9e36d-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="9e36d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e36d-109">EXAMPLES</span></span>

### <span data-ttu-id="9e36d-110">Пример 1: Настройка значений для изображения</span><span class="sxs-lookup"><span data-stu-id="9e36d-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="9e36d-111">Первая команда получает группу доступности с именем AvailabilitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9e36d-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="9e36d-112">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9e36d-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9e36d-113">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9e36d-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9e36d-114">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9e36d-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="9e36d-115">Последняя команда задает значения для имени издателя, предложения, SKU и версии.</span><span class="sxs-lookup"><span data-stu-id="9e36d-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="9e36d-116">Командлеты **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** и **Get-AzVMImage** могут определить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="9e36d-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="9e36d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e36d-117">PARAMETERS</span></span>

### <span data-ttu-id="9e36d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e36d-118">-DefaultProfile</span></span>
<span data-ttu-id="9e36d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e36d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e36d-120">-ID</span><span class="sxs-lookup"><span data-stu-id="9e36d-120">-Id</span></span>
<span data-ttu-id="9e36d-121">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9e36d-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="9e36d-122">-Предложение</span><span class="sxs-lookup"><span data-stu-id="9e36d-122">-Offer</span></span>
<span data-ttu-id="9e36d-123">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="9e36d-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="9e36d-124">Чтобы получить предложение с изображением, используйте командлет Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="9e36d-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="9e36d-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9e36d-125">-PublisherName</span></span>
<span data-ttu-id="9e36d-126">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="9e36d-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="9e36d-127">Чтобы получить издатель, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9e36d-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9e36d-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="9e36d-128">-Skus</span></span>
<span data-ttu-id="9e36d-129">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="9e36d-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="9e36d-130">Чтобы получить SKU, используйте командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="9e36d-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="9e36d-131">-Version</span><span class="sxs-lookup"><span data-stu-id="9e36d-131">-Version</span></span>
<span data-ttu-id="9e36d-132">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="9e36d-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="9e36d-133">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="9e36d-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="9e36d-134">-VM</span><span class="sxs-lookup"><span data-stu-id="9e36d-134">-VM</span></span>
<span data-ttu-id="9e36d-135">Указывает локальный объект виртуальной машины для настройки.</span><span class="sxs-lookup"><span data-stu-id="9e36d-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="9e36d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e36d-136">CommonParameters</span></span>
<span data-ttu-id="9e36d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e36d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e36d-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e36d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e36d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e36d-139">INPUTS</span></span>

### <span data-ttu-id="9e36d-140">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9e36d-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="9e36d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9e36d-141">System.String</span></span>

## <span data-ttu-id="9e36d-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e36d-142">OUTPUTS</span></span>

### <span data-ttu-id="9e36d-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9e36d-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9e36d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e36d-144">NOTES</span></span>

## <span data-ttu-id="9e36d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e36d-145">RELATED LINKS</span></span>

[<span data-ttu-id="9e36d-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9e36d-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="9e36d-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9e36d-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="9e36d-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9e36d-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="9e36d-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9e36d-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9e36d-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9e36d-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9e36d-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="9e36d-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


