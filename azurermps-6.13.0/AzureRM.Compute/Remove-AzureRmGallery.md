---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGallery.md
ms.openlocfilehash: 2711b5398f3d10f894214473f6ff68045748af22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564680"
---
# <span data-ttu-id="2fec5-101">Remove-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="2fec5-101">Remove-AzureRmGallery</span></span>

## <span data-ttu-id="2fec5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fec5-102">SYNOPSIS</span></span>
<span data-ttu-id="2fec5-103">Удаление коллекции.</span><span class="sxs-lookup"><span data-stu-id="2fec5-103">Delete a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fec5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fec5-104">SYNTAX</span></span>

### <span data-ttu-id="2fec5-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2fec5-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fec5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2fec5-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fec5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2fec5-107">ObjectParameter</span></span>
```
Remove-AzureRmGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fec5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fec5-108">DESCRIPTION</span></span>
<span data-ttu-id="2fec5-109">Удаление коллекции.</span><span class="sxs-lookup"><span data-stu-id="2fec5-109">Delete a gallery.</span></span>

## <span data-ttu-id="2fec5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fec5-110">EXAMPLES</span></span>

### <span data-ttu-id="2fec5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2fec5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="2fec5-112">Удаление указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="2fec5-112">Delete the given gallery.</span></span>

## <span data-ttu-id="2fec5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fec5-113">PARAMETERS</span></span>

### <span data-ttu-id="2fec5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fec5-114">-AsJob</span></span>
<span data-ttu-id="2fec5-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2fec5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fec5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fec5-116">-DefaultProfile</span></span>
<span data-ttu-id="2fec5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fec5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fec5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2fec5-118">-Force</span></span>
<span data-ttu-id="2fec5-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2fec5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fec5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fec5-120">-InputObject</span></span>
<span data-ttu-id="2fec5-121">Объект коллекции PS</span><span class="sxs-lookup"><span data-stu-id="2fec5-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="2fec5-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fec5-122">-Name</span></span>
<span data-ttu-id="2fec5-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="2fec5-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="2fec5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fec5-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fec5-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fec5-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="2fec5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fec5-126">-ResourceId</span></span>
<span data-ttu-id="2fec5-127">Идентификатор ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="2fec5-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="2fec5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fec5-128">-Confirm</span></span>
<span data-ttu-id="2fec5-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fec5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fec5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fec5-130">-WhatIf</span></span>
<span data-ttu-id="2fec5-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fec5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fec5-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fec5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fec5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fec5-133">CommonParameters</span></span>
<span data-ttu-id="2fec5-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fec5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fec5-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fec5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fec5-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fec5-136">INPUTS</span></span>

### <span data-ttu-id="2fec5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2fec5-137">System.String</span></span>

### <span data-ttu-id="2fec5-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="2fec5-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="2fec5-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fec5-139">OUTPUTS</span></span>

### <span data-ttu-id="2fec5-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2fec5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2fec5-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fec5-141">NOTES</span></span>

## <span data-ttu-id="2fec5-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fec5-142">RELATED LINKS</span></span>
