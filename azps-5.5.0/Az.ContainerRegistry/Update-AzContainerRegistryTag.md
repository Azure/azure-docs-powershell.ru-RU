---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 48fb77eb9c718a09a7e13e6d6ab5af5bfc60c912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238573"
---
# <span data-ttu-id="ced4f-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="ced4f-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="ced4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ced4f-102">SYNOPSIS</span></span>
<span data-ttu-id="ced4f-103">Обновить тег ACR.</span><span class="sxs-lookup"><span data-stu-id="ced4f-103">Update ACR tag.</span></span>

## <span data-ttu-id="ced4f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ced4f-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ced4f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ced4f-105">DESCRIPTION</span></span>
<span data-ttu-id="ced4f-106">Обновить тег ACR.</span><span class="sxs-lookup"><span data-stu-id="ced4f-106">Update ACR tag.</span></span>
<span data-ttu-id="ced4f-107">Чтобы использовать этот cmdlet, запустите `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="ced4f-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="ced4f-108">в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="ced4f-108">first.</span></span>

## <span data-ttu-id="ced4f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ced4f-109">EXAMPLES</span></span>

### <span data-ttu-id="ced4f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ced4f-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="ced4f-111">Обновление атрибутов для тегов последней версии в реестре.</span><span class="sxs-lookup"><span data-stu-id="ced4f-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="ced4f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ced4f-112">PARAMETERS</span></span>

### <span data-ttu-id="ced4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced4f-113">-DefaultProfile</span></span>
<span data-ttu-id="ced4f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ced4f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced4f-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="ced4f-115">-DeleteEnabled</span></span>
<span data-ttu-id="ced4f-116">"Включить удаление".</span><span class="sxs-lookup"><span data-stu-id="ced4f-116">Delete enable.</span></span>

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

### <span data-ttu-id="ced4f-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="ced4f-117">-ListEnabled</span></span>
<span data-ttu-id="ced4f-118">Список включается.</span><span class="sxs-lookup"><span data-stu-id="ced4f-118">List enable.</span></span>

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

### <span data-ttu-id="ced4f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ced4f-119">-Name</span></span>
<span data-ttu-id="ced4f-120">Тег.</span><span class="sxs-lookup"><span data-stu-id="ced4f-120">Tag.</span></span>

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

### <span data-ttu-id="ced4f-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="ced4f-121">-ReadEnabled</span></span>
<span data-ttu-id="ced4f-122">Включить чтение.</span><span class="sxs-lookup"><span data-stu-id="ced4f-122">Read enable.</span></span>

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

### <span data-ttu-id="ced4f-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ced4f-123">-RegistryName</span></span>
<span data-ttu-id="ced4f-124">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="ced4f-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="ced4f-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="ced4f-125">-RepositoryName</span></span>
<span data-ttu-id="ced4f-126">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="ced4f-126">Repository Name.</span></span>

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

### <span data-ttu-id="ced4f-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="ced4f-127">-WriteEnabled</span></span>
<span data-ttu-id="ced4f-128">"Включить написание".</span><span class="sxs-lookup"><span data-stu-id="ced4f-128">Write enable.</span></span>

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

### <span data-ttu-id="ced4f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ced4f-129">-Confirm</span></span>
<span data-ttu-id="ced4f-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ced4f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced4f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced4f-131">-WhatIf</span></span>
<span data-ttu-id="ced4f-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ced4f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced4f-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ced4f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced4f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced4f-134">CommonParameters</span></span>
<span data-ttu-id="ced4f-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced4f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced4f-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ced4f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced4f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ced4f-137">INPUTS</span></span>

### <span data-ttu-id="ced4f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ced4f-138">System.String</span></span>

## <span data-ttu-id="ced4f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ced4f-139">OUTPUTS</span></span>

### <span data-ttu-id="ced4f-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="ced4f-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="ced4f-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ced4f-141">NOTES</span></span>

## <span data-ttu-id="ced4f-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ced4f-142">RELATED LINKS</span></span>
