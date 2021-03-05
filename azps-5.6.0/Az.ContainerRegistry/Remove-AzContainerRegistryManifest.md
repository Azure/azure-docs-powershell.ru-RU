---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: def99b11efa5070881cc3226b9ec85449b4cc0b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963160"
---
# <span data-ttu-id="ed47f-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="ed47f-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="ed47f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed47f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed47f-103">Удаление манифеста ACR.</span><span class="sxs-lookup"><span data-stu-id="ed47f-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="ed47f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed47f-104">SYNTAX</span></span>

### <span data-ttu-id="ed47f-105">ByManifestParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed47f-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed47f-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed47f-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed47f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed47f-107">DESCRIPTION</span></span>
<span data-ttu-id="ed47f-108">Удаление манифеста ACR.</span><span class="sxs-lookup"><span data-stu-id="ed47f-108">Delete ACR manifest.</span></span>
<span data-ttu-id="ed47f-109">Чтобы использовать этот cmdlet, запустите `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="ed47f-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="ed47f-110">в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="ed47f-110">first.</span></span>

## <span data-ttu-id="ed47f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed47f-111">EXAMPLES</span></span>

### <span data-ttu-id="ed47f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed47f-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="ed47f-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span><span class="sxs-lookup"><span data-stu-id="ed47f-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="ed47f-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ed47f-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="ed47f-115">Удалить манифест с новейшим тегом для проверки репозитория /busybox27 в реестре</span><span class="sxs-lookup"><span data-stu-id="ed47f-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="ed47f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed47f-116">PARAMETERS</span></span>

### <span data-ttu-id="ed47f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed47f-117">-DefaultProfile</span></span>
<span data-ttu-id="ed47f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed47f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed47f-119">-Manifest</span><span class="sxs-lookup"><span data-stu-id="ed47f-119">-Manifest</span></span>
<span data-ttu-id="ed47f-120">Ссылка на манифест.</span><span class="sxs-lookup"><span data-stu-id="ed47f-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed47f-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ed47f-121">-RegistryName</span></span>
<span data-ttu-id="ed47f-122">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="ed47f-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="ed47f-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="ed47f-123">-RepositoryName</span></span>
<span data-ttu-id="ed47f-124">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="ed47f-124">Repository Name.</span></span>

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

### <span data-ttu-id="ed47f-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed47f-125">-Tag</span></span>
<span data-ttu-id="ed47f-126">Тег.</span><span class="sxs-lookup"><span data-stu-id="ed47f-126">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed47f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed47f-127">-Confirm</span></span>
<span data-ttu-id="ed47f-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed47f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed47f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed47f-129">-WhatIf</span></span>
<span data-ttu-id="ed47f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed47f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed47f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ed47f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed47f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed47f-132">CommonParameters</span></span>
<span data-ttu-id="ed47f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed47f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed47f-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed47f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed47f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed47f-135">INPUTS</span></span>

### <span data-ttu-id="ed47f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ed47f-136">System.String</span></span>

## <span data-ttu-id="ed47f-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed47f-137">OUTPUTS</span></span>

### <span data-ttu-id="ed47f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed47f-138">System.Boolean</span></span>

## <span data-ttu-id="ed47f-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed47f-139">NOTES</span></span>

## <span data-ttu-id="ed47f-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed47f-140">RELATED LINKS</span></span>
