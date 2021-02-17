---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 85623106a932ba9419da0c07cc4bcb6c52e5e838
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211396"
---
# <span data-ttu-id="7481f-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="7481f-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="7481f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7481f-102">SYNOPSIS</span></span>
<span data-ttu-id="7481f-103">Обновление манифеста ACR.</span><span class="sxs-lookup"><span data-stu-id="7481f-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="7481f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7481f-104">SYNTAX</span></span>

### <span data-ttu-id="7481f-105">ByManifestParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7481f-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7481f-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="7481f-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7481f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7481f-107">DESCRIPTION</span></span>
<span data-ttu-id="7481f-108">Обновление манифеста ACR.</span><span class="sxs-lookup"><span data-stu-id="7481f-108">Update ACR manifest.</span></span>
<span data-ttu-id="7481f-109">Чтобы использовать этот cmdlet, запустите `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="7481f-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="7481f-110">в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="7481f-110">first.</span></span>

## <span data-ttu-id="7481f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7481f-111">EXAMPLES</span></span>

### <span data-ttu-id="7481f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7481f-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="7481f-113">Атрибуты обновления манифеста sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 в реестре.</span><span class="sxs-lookup"><span data-stu-id="7481f-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="7481f-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7481f-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="7481f-115">Обновив атрибуты манифеста, в последних тегах реестра.</span><span class="sxs-lookup"><span data-stu-id="7481f-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="7481f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7481f-116">PARAMETERS</span></span>

### <span data-ttu-id="7481f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7481f-117">-DefaultProfile</span></span>
<span data-ttu-id="7481f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7481f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7481f-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="7481f-119">-DeleteEnabled</span></span>
<span data-ttu-id="7481f-120">"Включить удаление".</span><span class="sxs-lookup"><span data-stu-id="7481f-120">Delete enable.</span></span>

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

### <span data-ttu-id="7481f-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="7481f-121">-ListEnabled</span></span>
<span data-ttu-id="7481f-122">Список включается.</span><span class="sxs-lookup"><span data-stu-id="7481f-122">List enable.</span></span>

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

### <span data-ttu-id="7481f-123">-Manifest</span><span class="sxs-lookup"><span data-stu-id="7481f-123">-Manifest</span></span>
<span data-ttu-id="7481f-124">Ссылка на манифест.</span><span class="sxs-lookup"><span data-stu-id="7481f-124">Manifest reference.</span></span>

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

### <span data-ttu-id="7481f-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="7481f-125">-ReadEnabled</span></span>
<span data-ttu-id="7481f-126">Включить чтение.</span><span class="sxs-lookup"><span data-stu-id="7481f-126">Read enable.</span></span>

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

### <span data-ttu-id="7481f-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7481f-127">-RegistryName</span></span>
<span data-ttu-id="7481f-128">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="7481f-128">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="7481f-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="7481f-129">-RepositoryName</span></span>
<span data-ttu-id="7481f-130">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="7481f-130">Repository Name.</span></span>

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

### <span data-ttu-id="7481f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="7481f-131">-Tag</span></span>
<span data-ttu-id="7481f-132">Тег.</span><span class="sxs-lookup"><span data-stu-id="7481f-132">Tag.</span></span>

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

### <span data-ttu-id="7481f-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="7481f-133">-WriteEnabled</span></span>
<span data-ttu-id="7481f-134">"Включить написание".</span><span class="sxs-lookup"><span data-stu-id="7481f-134">Write enable.</span></span>

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

### <span data-ttu-id="7481f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7481f-135">-Confirm</span></span>
<span data-ttu-id="7481f-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7481f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7481f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7481f-137">-WhatIf</span></span>
<span data-ttu-id="7481f-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7481f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7481f-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7481f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7481f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7481f-140">CommonParameters</span></span>
<span data-ttu-id="7481f-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7481f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7481f-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7481f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7481f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7481f-143">INPUTS</span></span>

### <span data-ttu-id="7481f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7481f-144">System.String</span></span>

## <span data-ttu-id="7481f-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7481f-145">OUTPUTS</span></span>

### <span data-ttu-id="7481f-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="7481f-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="7481f-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7481f-147">NOTES</span></span>

## <span data-ttu-id="7481f-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7481f-148">RELATED LINKS</span></span>
