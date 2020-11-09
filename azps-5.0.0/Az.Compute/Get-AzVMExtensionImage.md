---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318083"
---
# <span data-ttu-id="40672-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="40672-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="40672-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40672-102">SYNOPSIS</span></span>
<span data-ttu-id="40672-103">Возвращает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="40672-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="40672-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40672-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40672-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40672-105">DESCRIPTION</span></span>
<span data-ttu-id="40672-106">Командлет **Get-AzVMExtensionImage** получает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="40672-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="40672-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40672-107">EXAMPLES</span></span>

### <span data-ttu-id="40672-108">Пример 1: получение версий изображения расширения</span><span class="sxs-lookup"><span data-stu-id="40672-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="40672-109">Эта команда получает все версии изображения расширения для указанных места, издателя и типа.</span><span class="sxs-lookup"><span data-stu-id="40672-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="40672-110">Пример 2: получение версий изображения расширения с помощью фильтра более ранней версии</span><span class="sxs-lookup"><span data-stu-id="40672-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="40672-111">Эта команда получает все версии изображения расширения для указанного местоположения, издателя, типа и версии, начиная с 12.</span><span class="sxs-lookup"><span data-stu-id="40672-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="40672-112">Пример 3: получение версий изображения расширения с помощью фильтра для более ранней версии</span><span class="sxs-lookup"><span data-stu-id="40672-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="40672-113">Эта команда получает все версии изображения расширения для указанной папки, издателя, типа и версии.</span><span class="sxs-lookup"><span data-stu-id="40672-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="40672-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40672-114">PARAMETERS</span></span>

### <span data-ttu-id="40672-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40672-115">-DefaultProfile</span></span>
<span data-ttu-id="40672-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40672-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40672-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="40672-117">-FilterExpression</span></span>
<span data-ttu-id="40672-118">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="40672-118">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40672-119">-Location</span><span class="sxs-lookup"><span data-stu-id="40672-119">-Location</span></span>
<span data-ttu-id="40672-120">Указывает расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="40672-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="40672-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="40672-121">-PublisherName</span></span>
<span data-ttu-id="40672-122">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="40672-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="40672-123">Чтобы получить издатель расширения, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="40672-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="40672-124">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="40672-124">-Type</span></span>
<span data-ttu-id="40672-125">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="40672-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="40672-126">Чтобы получить тип расширения, используйте командлет Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="40672-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="40672-127">-Version</span><span class="sxs-lookup"><span data-stu-id="40672-127">-Version</span></span>
<span data-ttu-id="40672-128">Указывает версию расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="40672-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="40672-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40672-129">CommonParameters</span></span>
<span data-ttu-id="40672-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40672-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40672-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40672-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40672-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40672-132">INPUTS</span></span>

### <span data-ttu-id="40672-133">System. String</span><span class="sxs-lookup"><span data-stu-id="40672-133">System.String</span></span>

## <span data-ttu-id="40672-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40672-134">OUTPUTS</span></span>

### <span data-ttu-id="40672-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="40672-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="40672-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="40672-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="40672-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="40672-137">NOTES</span></span>

## <span data-ttu-id="40672-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40672-138">RELATED LINKS</span></span>

[<span data-ttu-id="40672-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="40672-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="40672-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="40672-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="40672-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="40672-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


