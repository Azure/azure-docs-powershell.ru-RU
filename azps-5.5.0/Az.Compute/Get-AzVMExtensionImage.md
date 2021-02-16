---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233380"
---
# <span data-ttu-id="5c945-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5c945-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="5c945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c945-102">SYNOPSIS</span></span>
<span data-ttu-id="5c945-103">Получает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="5c945-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="5c945-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c945-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c945-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c945-105">DESCRIPTION</span></span>
<span data-ttu-id="5c945-106">Для расширения Azure можно получить все версии для cmdlet **Get-AzVMExtensionImage.**</span><span class="sxs-lookup"><span data-stu-id="5c945-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="5c945-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c945-107">EXAMPLES</span></span>

### <span data-ttu-id="5c945-108">Пример 1. Просмотр версий расширения</span><span class="sxs-lookup"><span data-stu-id="5c945-108">Example 1: Get the versions of an extension image</span></span>
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

<span data-ttu-id="5c945-109">Эта команда получает все версии изображения расширения для указанного расположения, издателя и типа.</span><span class="sxs-lookup"><span data-stu-id="5c945-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="5c945-110">Пример 2. Просмотр версий изображения расширения с фильтрацией по версии</span><span class="sxs-lookup"><span data-stu-id="5c945-110">Example 2: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="5c945-111">Эта команда получает все версии изображения расширения для указанного расположения, издателя, типа и версии, начиная с 12.</span><span class="sxs-lookup"><span data-stu-id="5c945-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="5c945-112">Пример 3. Просмотр версий расширения с фильтрацией по версии</span><span class="sxs-lookup"><span data-stu-id="5c945-112">Example 3: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="5c945-113">Эта команда получает все версии изображения расширения для указанного расположения, издателя, типа и версии.</span><span class="sxs-lookup"><span data-stu-id="5c945-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="5c945-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c945-114">PARAMETERS</span></span>

### <span data-ttu-id="5c945-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c945-115">-DefaultProfile</span></span>
<span data-ttu-id="5c945-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c945-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c945-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="5c945-117">-FilterExpression</span></span>
<span data-ttu-id="5c945-118">Определяет выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="5c945-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="5c945-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5c945-119">-Location</span></span>
<span data-ttu-id="5c945-120">Определяет расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="5c945-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="5c945-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="5c945-121">-PublisherName</span></span>
<span data-ttu-id="5c945-122">Указывает имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="5c945-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="5c945-123">Чтобы получить издателя расширения, воспользуйтесь Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="5c945-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="5c945-124">-Type</span><span class="sxs-lookup"><span data-stu-id="5c945-124">-Type</span></span>
<span data-ttu-id="5c945-125">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="5c945-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="5c945-126">Чтобы получить тип расширения, воспользуйтесь Get-AzVMExtensionImageType..</span><span class="sxs-lookup"><span data-stu-id="5c945-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="5c945-127">-Version</span><span class="sxs-lookup"><span data-stu-id="5c945-127">-Version</span></span>
<span data-ttu-id="5c945-128">Определяет версию расширения, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c945-128">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5c945-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c945-129">CommonParameters</span></span>
<span data-ttu-id="5c945-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c945-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c945-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c945-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c945-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c945-132">INPUTS</span></span>

### <span data-ttu-id="5c945-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5c945-133">System.String</span></span>

## <span data-ttu-id="5c945-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c945-134">OUTPUTS</span></span>

### <span data-ttu-id="5c945-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5c945-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="5c945-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="5c945-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="5c945-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c945-137">NOTES</span></span>

## <span data-ttu-id="5c945-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c945-138">RELATED LINKS</span></span>

[<span data-ttu-id="5c945-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="5c945-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="5c945-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5c945-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="5c945-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="5c945-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


