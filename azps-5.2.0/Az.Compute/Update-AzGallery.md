---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322352"
---
# <span data-ttu-id="fb949-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="fb949-101">Update-AzGallery</span></span>

## <span data-ttu-id="fb949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb949-102">SYNOPSIS</span></span>
<span data-ttu-id="fb949-103">Обновив галерею.</span><span class="sxs-lookup"><span data-stu-id="fb949-103">Update a gallery.</span></span>

## <span data-ttu-id="fb949-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fb949-104">SYNTAX</span></span>

### <span data-ttu-id="fb949-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb949-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb949-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fb949-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb949-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="fb949-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb949-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb949-108">DESCRIPTION</span></span>
<span data-ttu-id="fb949-109">Обновив галерею.</span><span class="sxs-lookup"><span data-stu-id="fb949-109">Update a gallery.</span></span>

## <span data-ttu-id="fb949-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fb949-110">EXAMPLES</span></span>

### <span data-ttu-id="fb949-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fb949-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="fb949-112">Обновив галерею.</span><span class="sxs-lookup"><span data-stu-id="fb949-112">Update a gallery.</span></span>

## <span data-ttu-id="fb949-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb949-113">PARAMETERS</span></span>

### <span data-ttu-id="fb949-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb949-114">-AsJob</span></span>
<span data-ttu-id="fb949-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fb949-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb949-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb949-116">-DefaultProfile</span></span>
<span data-ttu-id="fb949-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb949-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb949-118">-Description</span><span class="sxs-lookup"><span data-stu-id="fb949-118">-Description</span></span>
<span data-ttu-id="fb949-119">Описание ресурса коллекции.</span><span class="sxs-lookup"><span data-stu-id="fb949-119">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb949-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb949-120">-InputObject</span></span>
<span data-ttu-id="fb949-121">Объект коллекции PS.</span><span class="sxs-lookup"><span data-stu-id="fb949-121">The PS Gallery Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb949-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fb949-122">-Name</span></span>
<span data-ttu-id="fb949-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="fb949-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb949-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb949-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb949-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb949-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb949-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb949-126">-ResourceId</span></span>
<span data-ttu-id="fb949-127">ИД ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="fb949-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="fb949-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb949-128">-Tag</span></span>
<span data-ttu-id="fb949-129">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="fb949-129">Resource tags</span></span>

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

### <span data-ttu-id="fb949-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb949-130">-Confirm</span></span>
<span data-ttu-id="fb949-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fb949-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb949-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb949-132">-WhatIf</span></span>
<span data-ttu-id="fb949-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb949-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb949-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fb949-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb949-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb949-135">CommonParameters</span></span>
<span data-ttu-id="fb949-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb949-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb949-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb949-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb949-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb949-138">INPUTS</span></span>

### <span data-ttu-id="fb949-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fb949-139">System.String</span></span>

### <span data-ttu-id="fb949-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="fb949-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="fb949-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb949-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fb949-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb949-142">OUTPUTS</span></span>

### <span data-ttu-id="fb949-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="fb949-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="fb949-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fb949-144">NOTES</span></span>

## <span data-ttu-id="fb949-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb949-145">RELATED LINKS</span></span>
