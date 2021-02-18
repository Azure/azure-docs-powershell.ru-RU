---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 33446cf9e14175c67e3f2fd2fa5dead33b88f526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215764"
---
# <span data-ttu-id="9f1fd-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9f1fd-101">Get-AzVMImage</span></span>

## <span data-ttu-id="9f1fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1fd-103">Получает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9f1fd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f1fd-104">SYNTAX</span></span>

### <span data-ttu-id="9f1fd-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="9f1fd-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f1fd-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="9f1fd-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f1fd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f1fd-107">DESCRIPTION</span></span>
<span data-ttu-id="9f1fd-108">Для получения всех версий VMImage можно получить все версии **Get-AzVMImage.**</span><span class="sxs-lookup"><span data-stu-id="9f1fd-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9f1fd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f1fd-109">EXAMPLES</span></span>

### <span data-ttu-id="9f1fd-110">Пример 1. Получить объекты VMImage</span><span class="sxs-lookup"><span data-stu-id="9f1fd-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="9f1fd-111">Эта команда возвращает все версии VMImage, которые соответствуют указанным значениям.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="9f1fd-112">Пример 2. Получить объект VMImage</span><span class="sxs-lookup"><span data-stu-id="9f1fd-112">Example 2: Get VMImage object</span></span>
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
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="9f1fd-113">Эта команда получает определенную версию VMImage, которая соответствует указанным значениям.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="9f1fd-114">Пример 3. Получить объекты VMImage</span><span class="sxs-lookup"><span data-stu-id="9f1fd-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="9f1fd-115">Эта команда возвращает все версии VMImage, которые соответствуют указанным значениям с фильтрацией по версии.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="9f1fd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f1fd-116">PARAMETERS</span></span>

### <span data-ttu-id="9f1fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1fd-117">-DefaultProfile</span></span>
<span data-ttu-id="9f1fd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f1fd-119">-Location</span><span class="sxs-lookup"><span data-stu-id="9f1fd-119">-Location</span></span>
<span data-ttu-id="9f1fd-120">Определяет расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="9f1fd-121">-Offer</span><span class="sxs-lookup"><span data-stu-id="9f1fd-121">-Offer</span></span>
<span data-ttu-id="9f1fd-122">Тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="9f1fd-123">Чтобы получить предложение для изображения, воспользуйтесь Get-AzVMImageOffer- и рисунками.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="9f1fd-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="9f1fd-124">-OrderBy</span></span>
<span data-ttu-id="9f1fd-125">Определяет порядок возвращаемого результата.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="9f1fd-126">Отформатирован как запрос OData.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-126">Formatted as an OData query.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1fd-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9f1fd-127">-PublisherName</span></span>
<span data-ttu-id="9f1fd-128">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="9f1fd-129">Чтобы получить издателя изображения, воспользуйтесь Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9f1fd-130">-Skus</span><span class="sxs-lookup"><span data-stu-id="9f1fd-130">-Skus</span></span>
<span data-ttu-id="9f1fd-131">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="9f1fd-132">Чтобы получить SKU, воспользуйтесь Get-AzVMImageSku-кодом.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="9f1fd-133">-Top</span><span class="sxs-lookup"><span data-stu-id="9f1fd-133">-Top</span></span>
<span data-ttu-id="9f1fd-134">Указывает максимальное количество возвращенных изображений виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-134">Specifies the maximum number of virtual machine images returned.</span></span> 

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1fd-135">-Version</span><span class="sxs-lookup"><span data-stu-id="9f1fd-135">-Version</span></span>
<span data-ttu-id="9f1fd-136">Определяет версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-136">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1fd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1fd-137">CommonParameters</span></span>
<span data-ttu-id="9f1fd-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f1fd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1fd-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f1fd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1fd-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f1fd-140">INPUTS</span></span>

### <span data-ttu-id="9f1fd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9f1fd-141">System.String</span></span>

## <span data-ttu-id="9f1fd-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f1fd-142">OUTPUTS</span></span>

### <span data-ttu-id="9f1fd-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseImage</span><span class="sxs-lookup"><span data-stu-id="9f1fd-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="9f1fd-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseImageDetail</span><span class="sxs-lookup"><span data-stu-id="9f1fd-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="9f1fd-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f1fd-145">NOTES</span></span>

## <span data-ttu-id="9f1fd-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f1fd-146">RELATED LINKS</span></span>

[<span data-ttu-id="9f1fd-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9f1fd-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="9f1fd-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9f1fd-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9f1fd-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9f1fd-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9f1fd-150">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9f1fd-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


