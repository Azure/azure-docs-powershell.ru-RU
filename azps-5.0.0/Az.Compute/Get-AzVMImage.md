---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 350e03d6e238eb0cf1aa6b27da6b9a321603a664
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247634"
---
# <span data-ttu-id="b53ce-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b53ce-101">Get-AzVMImage</span></span>

## <span data-ttu-id="b53ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b53ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b53ce-103">Возвращает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="b53ce-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="b53ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b53ce-104">SYNTAX</span></span>

### <span data-ttu-id="b53ce-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="b53ce-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b53ce-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="b53ce-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b53ce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b53ce-107">DESCRIPTION</span></span>
<span data-ttu-id="b53ce-108">Командлет **Get-AzVMImage** получает все версии VMImage.</span><span class="sxs-lookup"><span data-stu-id="b53ce-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="b53ce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b53ce-109">EXAMPLES</span></span>

### <span data-ttu-id="b53ce-110">Пример 1: получение объектов VMImage</span><span class="sxs-lookup"><span data-stu-id="b53ce-110">Example 1: Get VMImage objects</span></span>
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

<span data-ttu-id="b53ce-111">Эта команда возвращает все версии VMImage, соответствующие указанным значениям.</span><span class="sxs-lookup"><span data-stu-id="b53ce-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="b53ce-112">Пример 2: получение объекта VMImage</span><span class="sxs-lookup"><span data-stu-id="b53ce-112">Example 2: Get VMImage object</span></span>
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

<span data-ttu-id="b53ce-113">Эта команда возвращает определенную версию VMImage, совпадающую с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="b53ce-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="b53ce-114">Пример 3: получение объектов VMImage</span><span class="sxs-lookup"><span data-stu-id="b53ce-114">Example 3: Get VMImage objects</span></span>
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

<span data-ttu-id="b53ce-115">Эта команда получает все версии VMImage, соответствующие указанным значениям, с фильтрацией по версии.</span><span class="sxs-lookup"><span data-stu-id="b53ce-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="b53ce-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b53ce-116">PARAMETERS</span></span>

### <span data-ttu-id="b53ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53ce-117">-DefaultProfile</span></span>
<span data-ttu-id="b53ce-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b53ce-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b53ce-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b53ce-119">-Location</span></span>
<span data-ttu-id="b53ce-120">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="b53ce-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="b53ce-121">-Предложение</span><span class="sxs-lookup"><span data-stu-id="b53ce-121">-Offer</span></span>
<span data-ttu-id="b53ce-122">Указывает тип предложения VMImage.</span><span class="sxs-lookup"><span data-stu-id="b53ce-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="b53ce-123">Чтобы получить предложение с изображением, используйте командлет Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="b53ce-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="b53ce-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b53ce-124">-OrderBy</span></span>
<span data-ttu-id="b53ce-125">Указывает порядок возвращаемых результатов.</span><span class="sxs-lookup"><span data-stu-id="b53ce-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="b53ce-126">Отформатированный как запрос OData.</span><span class="sxs-lookup"><span data-stu-id="b53ce-126">Formatted as an OData query.</span></span>

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

### <span data-ttu-id="b53ce-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b53ce-127">-PublisherName</span></span>
<span data-ttu-id="b53ce-128">Указывает издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="b53ce-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="b53ce-129">Чтобы получить издатель изображений, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="b53ce-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="b53ce-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="b53ce-130">-Skus</span></span>
<span data-ttu-id="b53ce-131">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="b53ce-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="b53ce-132">Чтобы получить SKU, используйте командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="b53ce-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="b53ce-133">-Top</span><span class="sxs-lookup"><span data-stu-id="b53ce-133">-Top</span></span>
<span data-ttu-id="b53ce-134">Указывает максимальное количество возвращенных изображений виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b53ce-134">Specifies the maximum number of virtual machine images returned.</span></span> 

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

### <span data-ttu-id="b53ce-135">-Version</span><span class="sxs-lookup"><span data-stu-id="b53ce-135">-Version</span></span>
<span data-ttu-id="b53ce-136">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="b53ce-136">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="b53ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53ce-137">CommonParameters</span></span>
<span data-ttu-id="b53ce-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b53ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53ce-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b53ce-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53ce-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b53ce-140">INPUTS</span></span>

### <span data-ttu-id="b53ce-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b53ce-141">System.String</span></span>

## <span data-ttu-id="b53ce-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b53ce-142">OUTPUTS</span></span>

### <span data-ttu-id="b53ce-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="b53ce-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="b53ce-144">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="b53ce-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="b53ce-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="b53ce-145">NOTES</span></span>

## <span data-ttu-id="b53ce-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b53ce-146">RELATED LINKS</span></span>

[<span data-ttu-id="b53ce-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="b53ce-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="b53ce-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b53ce-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="b53ce-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b53ce-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="b53ce-150">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b53ce-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


