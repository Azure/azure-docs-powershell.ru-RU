---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 68d4eab2088bc1091d812399aade67659d7db31b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956275"
---
# <span data-ttu-id="7735d-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="7735d-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="7735d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7735d-102">SYNOPSIS</span></span>
<span data-ttu-id="7735d-103">Обновить тег ACR.</span><span class="sxs-lookup"><span data-stu-id="7735d-103">Update ACR tag.</span></span>

## <span data-ttu-id="7735d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7735d-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7735d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7735d-105">DESCRIPTION</span></span>
<span data-ttu-id="7735d-106">Обновить тег ACR.</span><span class="sxs-lookup"><span data-stu-id="7735d-106">Update ACR tag.</span></span>
<span data-ttu-id="7735d-107">Чтобы использовать этот cmdlet, запустите `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="7735d-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="7735d-108">в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="7735d-108">first.</span></span>

## <span data-ttu-id="7735d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7735d-109">EXAMPLES</span></span>

### <span data-ttu-id="7735d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7735d-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="7735d-111">Обновив атрибуты для тегов последней версии в реестре.</span><span class="sxs-lookup"><span data-stu-id="7735d-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="7735d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7735d-112">PARAMETERS</span></span>

### <span data-ttu-id="7735d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7735d-113">-DefaultProfile</span></span>
<span data-ttu-id="7735d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7735d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7735d-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="7735d-115">-DeleteEnabled</span></span>
<span data-ttu-id="7735d-116">"Включить удаление".</span><span class="sxs-lookup"><span data-stu-id="7735d-116">Delete enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7735d-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="7735d-117">-ListEnabled</span></span>
<span data-ttu-id="7735d-118">Список включается.</span><span class="sxs-lookup"><span data-stu-id="7735d-118">List enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7735d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7735d-119">-Name</span></span>
<span data-ttu-id="7735d-120">Тег.</span><span class="sxs-lookup"><span data-stu-id="7735d-120">Tag.</span></span>

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

### <span data-ttu-id="7735d-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="7735d-121">-ReadEnabled</span></span>
<span data-ttu-id="7735d-122">Включить чтение.</span><span class="sxs-lookup"><span data-stu-id="7735d-122">Read enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7735d-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7735d-123">-RegistryName</span></span>
<span data-ttu-id="7735d-124">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="7735d-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="7735d-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="7735d-125">-RepositoryName</span></span>
<span data-ttu-id="7735d-126">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="7735d-126">Repository Name.</span></span>

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

### <span data-ttu-id="7735d-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="7735d-127">-WriteEnabled</span></span>
<span data-ttu-id="7735d-128">"Включить написание".</span><span class="sxs-lookup"><span data-stu-id="7735d-128">Write enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7735d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7735d-129">-Confirm</span></span>
<span data-ttu-id="7735d-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7735d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7735d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7735d-131">-WhatIf</span></span>
<span data-ttu-id="7735d-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7735d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7735d-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7735d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7735d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7735d-134">CommonParameters</span></span>
<span data-ttu-id="7735d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7735d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7735d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7735d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7735d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7735d-137">INPUTS</span></span>

### <span data-ttu-id="7735d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7735d-138">System.String</span></span>

## <span data-ttu-id="7735d-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7735d-139">OUTPUTS</span></span>

### <span data-ttu-id="7735d-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="7735d-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="7735d-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7735d-141">NOTES</span></span>

## <span data-ttu-id="7735d-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7735d-142">RELATED LINKS</span></span>
