---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519552"
---
# <span data-ttu-id="6fd50-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="6fd50-101">Remove-AzGallery</span></span>

## <span data-ttu-id="6fd50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fd50-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd50-103">Удаление коллекции.</span><span class="sxs-lookup"><span data-stu-id="6fd50-103">Delete a gallery.</span></span>

## <span data-ttu-id="6fd50-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6fd50-104">SYNTAX</span></span>

### <span data-ttu-id="6fd50-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6fd50-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd50-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6fd50-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd50-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6fd50-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd50-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fd50-108">DESCRIPTION</span></span>
<span data-ttu-id="6fd50-109">Удаление коллекции.</span><span class="sxs-lookup"><span data-stu-id="6fd50-109">Delete a gallery.</span></span>

## <span data-ttu-id="6fd50-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6fd50-110">EXAMPLES</span></span>

### <span data-ttu-id="6fd50-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6fd50-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="6fd50-112">Удалите предоставленную галерею.</span><span class="sxs-lookup"><span data-stu-id="6fd50-112">Delete the given gallery.</span></span>

## <span data-ttu-id="6fd50-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fd50-113">PARAMETERS</span></span>

### <span data-ttu-id="6fd50-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fd50-114">-AsJob</span></span>
<span data-ttu-id="6fd50-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6fd50-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fd50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd50-116">-DefaultProfile</span></span>
<span data-ttu-id="6fd50-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd50-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd50-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6fd50-118">-Force</span></span>
<span data-ttu-id="6fd50-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6fd50-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6fd50-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fd50-120">-InputObject</span></span>
<span data-ttu-id="6fd50-121">Объект коллекции PS</span><span class="sxs-lookup"><span data-stu-id="6fd50-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="6fd50-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6fd50-122">-Name</span></span>
<span data-ttu-id="6fd50-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="6fd50-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="6fd50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd50-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fd50-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fd50-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="6fd50-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd50-126">-ResourceId</span></span>
<span data-ttu-id="6fd50-127">ИД ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="6fd50-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="6fd50-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fd50-128">-Confirm</span></span>
<span data-ttu-id="6fd50-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fd50-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd50-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd50-130">-WhatIf</span></span>
<span data-ttu-id="6fd50-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fd50-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd50-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6fd50-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd50-133">CommonParameters</span></span>
<span data-ttu-id="6fd50-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd50-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fd50-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd50-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fd50-136">INPUTS</span></span>

### <span data-ttu-id="6fd50-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6fd50-137">System.String</span></span>

### <span data-ttu-id="6fd50-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="6fd50-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="6fd50-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6fd50-139">OUTPUTS</span></span>

### <span data-ttu-id="6fd50-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6fd50-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6fd50-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6fd50-141">NOTES</span></span>

## <span data-ttu-id="6fd50-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fd50-142">RELATED LINKS</span></span>
