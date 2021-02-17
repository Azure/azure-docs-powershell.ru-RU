---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 7e6528630c731b15f906d79de45bc50f94b2a715
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233164"
---
# <span data-ttu-id="cf2ef-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="cf2ef-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="cf2ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2ef-103">"Отостановить тег ACR".</span><span class="sxs-lookup"><span data-stu-id="cf2ef-103">Untag ACR tag.</span></span>

## <span data-ttu-id="cf2ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf2ef-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf2ef-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf2ef-105">DESCRIPTION</span></span>
<span data-ttu-id="cf2ef-106">"Отостановить тег ACR".</span><span class="sxs-lookup"><span data-stu-id="cf2ef-106">Untag ACR tag.</span></span>
<span data-ttu-id="cf2ef-107">Чтобы использовать этот cmdlet, запустите `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="cf2ef-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="cf2ef-108">в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-108">first.</span></span>

## <span data-ttu-id="cf2ef-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf2ef-109">EXAMPLES</span></span>

### <span data-ttu-id="cf2ef-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf2ef-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="cf2ef-111">Отвяжь alpine:tag под реестром.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="cf2ef-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf2ef-112">PARAMETERS</span></span>

### <span data-ttu-id="cf2ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2ef-113">-DefaultProfile</span></span>
<span data-ttu-id="cf2ef-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf2ef-115">-Name</span><span class="sxs-lookup"><span data-stu-id="cf2ef-115">-Name</span></span>
<span data-ttu-id="cf2ef-116">Тег.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-116">Tag.</span></span>

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

### <span data-ttu-id="cf2ef-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="cf2ef-117">-RegistryName</span></span>
<span data-ttu-id="cf2ef-118">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="cf2ef-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="cf2ef-119">-RepositoryName</span></span>
<span data-ttu-id="cf2ef-120">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-120">Repository Name.</span></span>

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

### <span data-ttu-id="cf2ef-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf2ef-121">-Confirm</span></span>
<span data-ttu-id="cf2ef-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf2ef-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf2ef-123">-WhatIf</span></span>
<span data-ttu-id="cf2ef-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf2ef-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf2ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2ef-126">CommonParameters</span></span>
<span data-ttu-id="cf2ef-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2ef-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf2ef-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2ef-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf2ef-129">INPUTS</span></span>

### <span data-ttu-id="cf2ef-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cf2ef-130">System.String</span></span>

## <span data-ttu-id="cf2ef-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf2ef-131">OUTPUTS</span></span>

### <span data-ttu-id="cf2ef-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cf2ef-132">System.Boolean</span></span>

## <span data-ttu-id="cf2ef-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf2ef-133">NOTES</span></span>

## <span data-ttu-id="cf2ef-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf2ef-134">RELATED LINKS</span></span>
