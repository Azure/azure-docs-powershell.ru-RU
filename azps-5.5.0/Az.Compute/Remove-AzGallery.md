---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244080"
---
# <span data-ttu-id="71089-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="71089-101">Remove-AzGallery</span></span>

## <span data-ttu-id="71089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71089-102">SYNOPSIS</span></span>
<span data-ttu-id="71089-103">Удаление коллекции.</span><span class="sxs-lookup"><span data-stu-id="71089-103">Delete a gallery.</span></span>

## <span data-ttu-id="71089-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="71089-104">SYNTAX</span></span>

### <span data-ttu-id="71089-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71089-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71089-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="71089-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71089-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="71089-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71089-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71089-108">DESCRIPTION</span></span>
<span data-ttu-id="71089-109">Удаление коллекции.</span><span class="sxs-lookup"><span data-stu-id="71089-109">Delete a gallery.</span></span>

## <span data-ttu-id="71089-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="71089-110">EXAMPLES</span></span>

### <span data-ttu-id="71089-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71089-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="71089-112">Удалите предоставленную галерею.</span><span class="sxs-lookup"><span data-stu-id="71089-112">Delete the given gallery.</span></span>

## <span data-ttu-id="71089-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71089-113">PARAMETERS</span></span>

### <span data-ttu-id="71089-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71089-114">-AsJob</span></span>
<span data-ttu-id="71089-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="71089-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71089-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71089-116">-DefaultProfile</span></span>
<span data-ttu-id="71089-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71089-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71089-118">-Force</span><span class="sxs-lookup"><span data-stu-id="71089-118">-Force</span></span>
<span data-ttu-id="71089-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="71089-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71089-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71089-120">-InputObject</span></span>
<span data-ttu-id="71089-121">Объект коллекции PS</span><span class="sxs-lookup"><span data-stu-id="71089-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="71089-122">-Name</span><span class="sxs-lookup"><span data-stu-id="71089-122">-Name</span></span>
<span data-ttu-id="71089-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="71089-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="71089-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71089-124">-ResourceGroupName</span></span>
<span data-ttu-id="71089-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71089-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="71089-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71089-126">-ResourceId</span></span>
<span data-ttu-id="71089-127">ИД ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="71089-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="71089-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71089-128">-Confirm</span></span>
<span data-ttu-id="71089-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71089-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71089-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71089-130">-WhatIf</span></span>
<span data-ttu-id="71089-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71089-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71089-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="71089-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71089-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71089-133">CommonParameters</span></span>
<span data-ttu-id="71089-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71089-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71089-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71089-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71089-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71089-136">INPUTS</span></span>

### <span data-ttu-id="71089-137">System.String</span><span class="sxs-lookup"><span data-stu-id="71089-137">System.String</span></span>

### <span data-ttu-id="71089-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="71089-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="71089-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="71089-139">OUTPUTS</span></span>

### <span data-ttu-id="71089-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="71089-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="71089-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="71089-141">NOTES</span></span>

## <span data-ttu-id="71089-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71089-142">RELATED LINKS</span></span>
