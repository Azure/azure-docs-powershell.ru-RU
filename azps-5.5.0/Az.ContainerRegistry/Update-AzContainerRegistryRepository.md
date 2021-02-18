---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: ce6f235669ebe4a32958229422f4612f3b8cb340
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230953"
---
# <span data-ttu-id="2e69a-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="2e69a-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="2e69a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e69a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e69a-103">Обновить репозиторий ACR.</span><span class="sxs-lookup"><span data-stu-id="2e69a-103">Update ACR repository.</span></span>

## <span data-ttu-id="2e69a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2e69a-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e69a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e69a-105">DESCRIPTION</span></span>
<span data-ttu-id="2e69a-106">Обновить репозиторий ACR.</span><span class="sxs-lookup"><span data-stu-id="2e69a-106">Update ACR repository.</span></span>

## <span data-ttu-id="2e69a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2e69a-107">EXAMPLES</span></span>

### <span data-ttu-id="2e69a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e69a-108">Example 1</span></span>
```powershell
Update-AzContainerRegistryRepository -RegistryName registry -Name test/busybox8 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry             : registry.azurecr.io
ImageName            : test/busybox8
CreatedTime          : 2020-12-11T08:57:56.2070002Z
LastUpdateTime       : 2020-12-11T08:57:56.5188237Z
ManifestCount        : 1
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="2e69a-109">"Обновить атрибуты для репозитория в реестре".</span><span class="sxs-lookup"><span data-stu-id="2e69a-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="2e69a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e69a-110">PARAMETERS</span></span>

### <span data-ttu-id="2e69a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e69a-111">-DefaultProfile</span></span>
<span data-ttu-id="2e69a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e69a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e69a-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="2e69a-113">-DeleteEnabled</span></span>
<span data-ttu-id="2e69a-114">"Включить удаление".</span><span class="sxs-lookup"><span data-stu-id="2e69a-114">Delete enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e69a-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="2e69a-115">-ListEnabled</span></span>
<span data-ttu-id="2e69a-116">Список включается.</span><span class="sxs-lookup"><span data-stu-id="2e69a-116">List enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e69a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2e69a-117">-Name</span></span>
<span data-ttu-id="2e69a-118">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="2e69a-118">Repository Name.</span></span>

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

### <span data-ttu-id="2e69a-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="2e69a-119">-ReadEnabled</span></span>
<span data-ttu-id="2e69a-120">Включить чтение.</span><span class="sxs-lookup"><span data-stu-id="2e69a-120">Read enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e69a-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2e69a-121">-RegistryName</span></span>
<span data-ttu-id="2e69a-122">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="2e69a-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="2e69a-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="2e69a-123">-WriteEnabled</span></span>
<span data-ttu-id="2e69a-124">"Включить написание".</span><span class="sxs-lookup"><span data-stu-id="2e69a-124">Write enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e69a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e69a-125">-Confirm</span></span>
<span data-ttu-id="2e69a-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e69a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e69a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e69a-127">-WhatIf</span></span>
<span data-ttu-id="2e69a-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e69a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e69a-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2e69a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e69a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e69a-130">CommonParameters</span></span>
<span data-ttu-id="2e69a-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e69a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e69a-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e69a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e69a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e69a-133">INPUTS</span></span>

### <span data-ttu-id="2e69a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2e69a-134">System.String</span></span>

## <span data-ttu-id="2e69a-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2e69a-135">OUTPUTS</span></span>

### <span data-ttu-id="2e69a-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="2e69a-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="2e69a-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2e69a-137">NOTES</span></span>

## <span data-ttu-id="2e69a-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e69a-138">RELATED LINKS</span></span>
