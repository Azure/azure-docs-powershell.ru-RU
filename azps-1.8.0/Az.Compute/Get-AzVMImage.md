---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 13871100efbe2fe62de769adcc40ee434e86eb21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901309"
---
# <span data-ttu-id="3e631-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3e631-101">Get-AzVMImage</span></span>

## <span data-ttu-id="3e631-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e631-102">SYNOPSIS</span></span>
<span data-ttu-id="3e631-103">Возвращает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="3e631-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="3e631-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e631-104">SYNTAX</span></span>

### <span data-ttu-id="3e631-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="3e631-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e631-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="3e631-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e631-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e631-107">DESCRIPTION</span></span>
<span data-ttu-id="3e631-108">Командлет **Get-AzVMImage** получает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="3e631-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="3e631-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e631-109">EXAMPLES</span></span>

### <span data-ttu-id="3e631-110">Пример 1: получение объектов VMImage</span><span class="sxs-lookup"><span data-stu-id="3e631-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="3e631-111">Эта команда возвращает все версии VMImage, соответствующие указанным значениям.</span><span class="sxs-lookup"><span data-stu-id="3e631-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="3e631-112">Пример 2: получение объекта VMImage</span><span class="sxs-lookup"><span data-stu-id="3e631-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="3e631-113">Эта команда возвращает определенную версию VMImage, совпадающую с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="3e631-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="3e631-114">Пример 3: получение объектов VMImage</span><span class="sxs-lookup"><span data-stu-id="3e631-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="3e631-115">Эта команда получает все версии VMImage, соответствующие указанным значениям, с фильтрацией по версии.</span><span class="sxs-lookup"><span data-stu-id="3e631-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="3e631-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e631-116">PARAMETERS</span></span>

### <span data-ttu-id="3e631-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e631-117">-DefaultProfile</span></span>
<span data-ttu-id="3e631-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e631-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e631-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="3e631-119">-FilterExpression</span></span>
<span data-ttu-id="3e631-120">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="3e631-120">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e631-121">-Location</span><span class="sxs-lookup"><span data-stu-id="3e631-121">-Location</span></span>
<span data-ttu-id="3e631-122">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="3e631-122">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e631-123">-Предложение</span><span class="sxs-lookup"><span data-stu-id="3e631-123">-Offer</span></span>
<span data-ttu-id="3e631-124">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="3e631-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="3e631-125">Чтобы получить предложение с изображением, используйте командлет Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="3e631-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e631-126">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3e631-126">-PublisherName</span></span>
<span data-ttu-id="3e631-127">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="3e631-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="3e631-128">Чтобы получить издатель изображений, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="3e631-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e631-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="3e631-129">-Skus</span></span>
<span data-ttu-id="3e631-130">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="3e631-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="3e631-131">Чтобы получить SKU, используйте командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="3e631-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e631-132">-Version</span><span class="sxs-lookup"><span data-stu-id="3e631-132">-Version</span></span>
<span data-ttu-id="3e631-133">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="3e631-133">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3e631-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e631-134">CommonParameters</span></span>
<span data-ttu-id="3e631-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e631-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e631-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e631-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e631-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e631-137">INPUTS</span></span>

### <span data-ttu-id="3e631-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3e631-138">System.String</span></span>

## <span data-ttu-id="3e631-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e631-139">OUTPUTS</span></span>

### <span data-ttu-id="3e631-140">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="3e631-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="3e631-141">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="3e631-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="3e631-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e631-142">NOTES</span></span>

## <span data-ttu-id="3e631-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e631-143">RELATED LINKS</span></span>

[<span data-ttu-id="3e631-144">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3e631-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="3e631-145">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3e631-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="3e631-146">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3e631-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="3e631-147">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3e631-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


