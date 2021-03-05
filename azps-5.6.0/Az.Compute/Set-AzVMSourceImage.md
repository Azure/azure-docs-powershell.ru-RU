---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: ac02e3c54500e1ba104c4deb323bb7257fa3e71b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985214"
---
# <span data-ttu-id="92660-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="92660-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="92660-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92660-102">SYNOPSIS</span></span>
<span data-ttu-id="92660-103">Определяет изображение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92660-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="92660-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92660-104">SYNTAX</span></span>

### <span data-ttu-id="92660-105">ImageReferenceSkuParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92660-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92660-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92660-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92660-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92660-107">DESCRIPTION</span></span>
<span data-ttu-id="92660-108">Cmdlet **Set-AzVMSourceImage** определяет изображение платформы, которое будет использовать для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92660-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="92660-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92660-109">EXAMPLES</span></span>

### <span data-ttu-id="92660-110">Пример 1. Настройка значений для изображения</span><span class="sxs-lookup"><span data-stu-id="92660-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="92660-111">Первая команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в переменной $AvailabilitySet ресурса.</span><span class="sxs-lookup"><span data-stu-id="92660-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="92660-112">Вторая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="92660-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="92660-113">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="92660-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="92660-114">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="92660-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="92660-115">Конечная команда задает значения для имени, предложения, SKU и версии издателя.</span><span class="sxs-lookup"><span data-stu-id="92660-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="92660-116">Эти параметры могут обнаружиться с помощью параметров **Get-AzVMImagePublisher,** **Get-AzVMImageOffer, Get-AzVMImagePublisher, Get-AzVMImageOffer, Get-AzVMageOffer,** **Get-AzVMimageSku** и **Get-AzVMImage.**</span><span class="sxs-lookup"><span data-stu-id="92660-116">The **Get-AzVMImagePublisher**, **Get-AzVMImageOffer**, **Get-AzVMImageSku**, and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="92660-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92660-117">PARAMETERS</span></span>

### <span data-ttu-id="92660-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92660-118">-DefaultProfile</span></span>
<span data-ttu-id="92660-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92660-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92660-120">-Id</span><span class="sxs-lookup"><span data-stu-id="92660-120">-Id</span></span>
<span data-ttu-id="92660-121">Определяет ИД.</span><span class="sxs-lookup"><span data-stu-id="92660-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="92660-122">-Offer</span><span class="sxs-lookup"><span data-stu-id="92660-122">-Offer</span></span>
<span data-ttu-id="92660-123">Тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="92660-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="92660-124">Чтобы получить предложение для изображения, воспользуйтесь Get-AzVMImageOffer- и рисунками.</span><span class="sxs-lookup"><span data-stu-id="92660-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="92660-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="92660-125">-PublisherName</span></span>
<span data-ttu-id="92660-126">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="92660-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="92660-127">Чтобы получить издателя, воспользуйтесь Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="92660-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="92660-128">-Skus</span><span class="sxs-lookup"><span data-stu-id="92660-128">-Skus</span></span>
<span data-ttu-id="92660-129">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="92660-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="92660-130">Чтобы получить skus, используйте Get-AzVMImageSku-код.</span><span class="sxs-lookup"><span data-stu-id="92660-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="92660-131">-Version</span><span class="sxs-lookup"><span data-stu-id="92660-131">-Version</span></span>
<span data-ttu-id="92660-132">Определяет версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="92660-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="92660-133">Чтобы использовать последнюю версию, укажите последнюю версию, а не конкретную.</span><span class="sxs-lookup"><span data-stu-id="92660-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="92660-134">-VM</span><span class="sxs-lookup"><span data-stu-id="92660-134">-VM</span></span>
<span data-ttu-id="92660-135">Указывает настраиваемый объект локальной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92660-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="92660-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92660-136">CommonParameters</span></span>
<span data-ttu-id="92660-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92660-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92660-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92660-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92660-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92660-139">INPUTS</span></span>

### <span data-ttu-id="92660-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="92660-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="92660-141">System.String</span><span class="sxs-lookup"><span data-stu-id="92660-141">System.String</span></span>

## <span data-ttu-id="92660-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92660-142">OUTPUTS</span></span>

### <span data-ttu-id="92660-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="92660-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="92660-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92660-144">NOTES</span></span>

## <span data-ttu-id="92660-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92660-145">RELATED LINKS</span></span>

[<span data-ttu-id="92660-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92660-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="92660-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="92660-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="92660-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="92660-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="92660-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="92660-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="92660-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="92660-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="92660-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="92660-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


