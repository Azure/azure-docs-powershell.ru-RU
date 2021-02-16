---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229081"
---
# <span data-ttu-id="45e86-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="45e86-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="45e86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45e86-102">SYNOPSIS</span></span>
<span data-ttu-id="45e86-103">Удаление определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="45e86-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="45e86-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45e86-104">SYNTAX</span></span>

### <span data-ttu-id="45e86-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45e86-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45e86-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="45e86-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45e86-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="45e86-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45e86-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45e86-108">DESCRIPTION</span></span>
<span data-ttu-id="45e86-109">Удаление определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="45e86-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="45e86-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45e86-110">EXAMPLES</span></span>

### <span data-ttu-id="45e86-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45e86-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="45e86-112">Удалите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="45e86-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="45e86-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45e86-113">PARAMETERS</span></span>

### <span data-ttu-id="45e86-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45e86-114">-AsJob</span></span>
<span data-ttu-id="45e86-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="45e86-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45e86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e86-116">-DefaultProfile</span></span>
<span data-ttu-id="45e86-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45e86-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45e86-118">-Force</span><span class="sxs-lookup"><span data-stu-id="45e86-118">-Force</span></span>
<span data-ttu-id="45e86-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="45e86-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45e86-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="45e86-120">-GalleryName</span></span>
<span data-ttu-id="45e86-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="45e86-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e86-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45e86-122">-InputObject</span></span>
<span data-ttu-id="45e86-123">Объект определения изображения коллекции PS</span><span class="sxs-lookup"><span data-stu-id="45e86-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45e86-124">-Name</span><span class="sxs-lookup"><span data-stu-id="45e86-124">-Name</span></span>
<span data-ttu-id="45e86-125">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="45e86-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e86-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e86-126">-ResourceGroupName</span></span>
<span data-ttu-id="45e86-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45e86-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="45e86-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45e86-128">-ResourceId</span></span>
<span data-ttu-id="45e86-129">ИД ресурса для определения изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="45e86-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="45e86-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45e86-130">-Confirm</span></span>
<span data-ttu-id="45e86-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="45e86-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45e86-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e86-132">-WhatIf</span></span>
<span data-ttu-id="45e86-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e86-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45e86-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="45e86-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45e86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e86-135">CommonParameters</span></span>
<span data-ttu-id="45e86-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e86-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45e86-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e86-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45e86-138">INPUTS</span></span>

### <span data-ttu-id="45e86-139">System.String</span><span class="sxs-lookup"><span data-stu-id="45e86-139">System.String</span></span>

### <span data-ttu-id="45e86-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="45e86-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="45e86-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45e86-141">OUTPUTS</span></span>

### <span data-ttu-id="45e86-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="45e86-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="45e86-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45e86-143">NOTES</span></span>

## <span data-ttu-id="45e86-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45e86-144">RELATED LINKS</span></span>
