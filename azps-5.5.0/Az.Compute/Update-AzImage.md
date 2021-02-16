---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211468"
---
# <span data-ttu-id="6ad2d-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="6ad2d-101">Update-AzImage</span></span>

## <span data-ttu-id="6ad2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad2d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad2d-103">Обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-103">Updates an image.</span></span>

## <span data-ttu-id="6ad2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ad2d-104">SYNTAX</span></span>

### <span data-ttu-id="6ad2d-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ad2d-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad2d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6ad2d-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad2d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6ad2d-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad2d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ad2d-108">DESCRIPTION</span></span>
<span data-ttu-id="6ad2d-109">При **этом изображение** обновляется с его изображением.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="6ad2d-110">В настоящее время можно обновить только теги.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="6ad2d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ad2d-111">EXAMPLES</span></span>

### <span data-ttu-id="6ad2d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ad2d-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="6ad2d-113">Эта команда обновляет значение тега для существующего изображения "Image01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="6ad2d-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6ad2d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ad2d-114">PARAMETERS</span></span>

### <span data-ttu-id="6ad2d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ad2d-115">-AsJob</span></span>
<span data-ttu-id="6ad2d-116">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-116">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad2d-117">-DefaultProfile</span></span>
<span data-ttu-id="6ad2d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ad2d-119">-Image</span><span class="sxs-lookup"><span data-stu-id="6ad2d-119">-Image</span></span>
<span data-ttu-id="6ad2d-120">Определяет объект локального изображения.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad2d-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6ad2d-121">-ImageName</span></span>
<span data-ttu-id="6ad2d-122">Определяет имя изображения.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad2d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad2d-123">-ResourceGroupName</span></span>
<span data-ttu-id="6ad2d-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad2d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad2d-125">-ResourceId</span></span>
<span data-ttu-id="6ad2d-126">ИД ресурса для изображения</span><span class="sxs-lookup"><span data-stu-id="6ad2d-126">The resource Id for the image</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad2d-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ad2d-127">-Tag</span></span>
<span data-ttu-id="6ad2d-128">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="6ad2d-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad2d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ad2d-129">-Confirm</span></span>
<span data-ttu-id="6ad2d-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad2d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad2d-131">-WhatIf</span></span>
<span data-ttu-id="6ad2d-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad2d-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad2d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad2d-134">CommonParameters</span></span>
<span data-ttu-id="6ad2d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad2d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ad2d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad2d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ad2d-137">INPUTS</span></span>

### <span data-ttu-id="6ad2d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6ad2d-138">System.String</span></span>

### <span data-ttu-id="6ad2d-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="6ad2d-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="6ad2d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ad2d-140">OUTPUTS</span></span>

### <span data-ttu-id="6ad2d-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="6ad2d-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="6ad2d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ad2d-142">NOTES</span></span>

## <span data-ttu-id="6ad2d-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ad2d-143">RELATED LINKS</span></span>
