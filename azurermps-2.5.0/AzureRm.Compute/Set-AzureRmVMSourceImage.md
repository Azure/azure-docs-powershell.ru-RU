---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsourceimage
schema: 2.0.0
ms.openlocfilehash: 5e07ba8ffceb42a94c41c0b21c62329f9dbe96a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913911"
---
# <span data-ttu-id="7c944-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="7c944-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="7c944-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c944-102">SYNOPSIS</span></span>
<span data-ttu-id="7c944-103">Указывает изображение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7c944-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c944-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c944-104">SYNTAX</span></span>

### <span data-ttu-id="7c944-105">ImageReferenceSkuParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c944-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c944-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c944-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c944-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c944-107">DESCRIPTION</span></span>
<span data-ttu-id="7c944-108">Командлет **Set-AzureRmVMSourceImage** указывает изображение платформы, используемое для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7c944-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="7c944-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c944-109">EXAMPLES</span></span>

### <span data-ttu-id="7c944-110">Пример 1: Настройка значений для изображения</span><span class="sxs-lookup"><span data-stu-id="7c944-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="7c944-111">Первая команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7c944-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="7c944-112">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7c944-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7c944-113">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7c944-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="7c944-114">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7c944-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="7c944-115">Последняя команда задает значения для имени издателя, предложения, SKU и версии.</span><span class="sxs-lookup"><span data-stu-id="7c944-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="7c944-116">Командлеты **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** и **Get-AzureRmVMImage** могут определить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="7c944-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="7c944-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c944-117">PARAMETERS</span></span>

### <span data-ttu-id="7c944-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c944-118">-DefaultProfile</span></span>
<span data-ttu-id="7c944-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c944-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c944-120">-ID</span><span class="sxs-lookup"><span data-stu-id="7c944-120">-Id</span></span>
<span data-ttu-id="7c944-121">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="7c944-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="7c944-122">-Предложение</span><span class="sxs-lookup"><span data-stu-id="7c944-122">-Offer</span></span>
<span data-ttu-id="7c944-123">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="7c944-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="7c944-124">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="7c944-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="7c944-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7c944-125">-PublisherName</span></span>
<span data-ttu-id="7c944-126">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="7c944-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="7c944-127">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="7c944-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="7c944-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="7c944-128">-Skus</span></span>
<span data-ttu-id="7c944-129">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="7c944-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="7c944-130">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="7c944-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="7c944-131">-Version</span><span class="sxs-lookup"><span data-stu-id="7c944-131">-Version</span></span>
<span data-ttu-id="7c944-132">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="7c944-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="7c944-133">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="7c944-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="7c944-134">-VM</span><span class="sxs-lookup"><span data-stu-id="7c944-134">-VM</span></span>
<span data-ttu-id="7c944-135">Указывает локальный объект виртуальной машины для настройки.</span><span class="sxs-lookup"><span data-stu-id="7c944-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="7c944-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c944-136">CommonParameters</span></span>
<span data-ttu-id="7c944-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c944-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c944-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c944-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c944-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c944-139">INPUTS</span></span>

### <span data-ttu-id="7c944-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7c944-140">PSVirtualMachine</span></span>
<span data-ttu-id="7c944-141">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7c944-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="7c944-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c944-142">OUTPUTS</span></span>

### <span data-ttu-id="7c944-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7c944-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7c944-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c944-144">NOTES</span></span>

## <span data-ttu-id="7c944-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c944-145">RELATED LINKS</span></span>

[<span data-ttu-id="7c944-146">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7c944-146">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="7c944-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7c944-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="7c944-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7c944-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="7c944-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7c944-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="7c944-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7c944-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="7c944-151">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="7c944-151">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


