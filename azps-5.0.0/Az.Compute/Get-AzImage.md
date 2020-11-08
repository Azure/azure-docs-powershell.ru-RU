---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249082"
---
# <span data-ttu-id="ad0aa-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="ad0aa-101">Get-AzImage</span></span>

## <span data-ttu-id="ad0aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad0aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0aa-103">Получает свойства изображения.</span><span class="sxs-lookup"><span data-stu-id="ad0aa-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="ad0aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad0aa-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad0aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad0aa-105">DESCRIPTION</span></span>
<span data-ttu-id="ad0aa-106">Командлет **Get-AzImage** получает свойства изображения.</span><span class="sxs-lookup"><span data-stu-id="ad0aa-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="ad0aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad0aa-107">EXAMPLES</span></span>

### <span data-ttu-id="ad0aa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad0aa-108">Example 1</span></span>
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

<span data-ttu-id="ad0aa-109">Эта команда получает свойства изображения с именем "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ad0aa-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ad0aa-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ad0aa-110">Example 2</span></span>
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

<span data-ttu-id="ad0aa-111">Эта команда получает свойства всех изображений в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ad0aa-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ad0aa-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ad0aa-112">Example 3</span></span>
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

<span data-ttu-id="ad0aa-113">Эта команда получает свойства всех изображений в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="ad0aa-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="ad0aa-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ad0aa-114">Example 4</span></span>
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

<span data-ttu-id="ad0aa-115">Эта команда получает свойства всех изображений в подписке, которые начинаются с "Image".</span><span class="sxs-lookup"><span data-stu-id="ad0aa-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="ad0aa-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad0aa-116">PARAMETERS</span></span>

### <span data-ttu-id="ad0aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0aa-117">-DefaultProfile</span></span>
<span data-ttu-id="ad0aa-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0aa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad0aa-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="ad0aa-119">-Expand</span></span>
<span data-ttu-id="ad0aa-120">Указывает запрос на расширение выражения.</span><span class="sxs-lookup"><span data-stu-id="ad0aa-120">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="ad0aa-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ad0aa-121">-ImageName</span></span>
<span data-ttu-id="ad0aa-122">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="ad0aa-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="ad0aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad0aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad0aa-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad0aa-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad0aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0aa-125">CommonParameters</span></span>
<span data-ttu-id="ad0aa-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad0aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0aa-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad0aa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0aa-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad0aa-128">INPUTS</span></span>

### <span data-ttu-id="ad0aa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ad0aa-129">System.String</span></span>

## <span data-ttu-id="ad0aa-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad0aa-130">OUTPUTS</span></span>

### <span data-ttu-id="ad0aa-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="ad0aa-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ad0aa-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad0aa-132">NOTES</span></span>

## <span data-ttu-id="ad0aa-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad0aa-133">RELATED LINKS</span></span>
