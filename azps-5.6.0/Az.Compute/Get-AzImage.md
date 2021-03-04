---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 8261a4ee59d7a29911e7cfde3b28b5d28e3e1ae5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969251"
---
# <span data-ttu-id="dcd6e-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-101">Get-AzImage</span></span>

## <span data-ttu-id="dcd6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd6e-103">Свойства изображения.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="dcd6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dcd6e-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcd6e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcd6e-105">DESCRIPTION</span></span>
<span data-ttu-id="dcd6e-106">Свойства **изображения получает cmdlet Get-AzImage.**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="dcd6e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dcd6e-107">EXAMPLES</span></span>

### <span data-ttu-id="dcd6e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dcd6e-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="dcd6e-109">Эта команда получает свойства изображения с именем "Изображение01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="dcd6e-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="dcd6e-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="dcd6e-111">Эта команда получает свойства всех изображений в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="dcd6e-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="dcd6e-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="dcd6e-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="dcd6e-113">Эта команда получает свойства всех изображений в подписке.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="dcd6e-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="dcd6e-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="dcd6e-115">Эта команда получает свойства всех изображений в подписке, которая начинается с "Изображение".</span><span class="sxs-lookup"><span data-stu-id="dcd6e-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="dcd6e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-116">PARAMETERS</span></span>

### <span data-ttu-id="dcd6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-117">-DefaultProfile</span></span>
<span data-ttu-id="dcd6e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcd6e-119">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="dcd6e-119">-Expand</span></span>
<span data-ttu-id="dcd6e-120">Определяет запрос на расширение выражения.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd6e-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="dcd6e-121">-ImageName</span></span>
<span data-ttu-id="dcd6e-122">Определяет имя изображения.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dcd6e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd6e-123">-ResourceGroupName</span></span>
<span data-ttu-id="dcd6e-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dcd6e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd6e-125">CommonParameters</span></span>
<span data-ttu-id="dcd6e-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd6e-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd6e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-128">INPUTS</span></span>

### <span data-ttu-id="dcd6e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dcd6e-129">System.String</span></span>

## <span data-ttu-id="dcd6e-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-130">OUTPUTS</span></span>

### <span data-ttu-id="dcd6e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="dcd6e-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dcd6e-132">NOTES</span></span>

## <span data-ttu-id="dcd6e-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcd6e-133">RELATED LINKS</span></span>
