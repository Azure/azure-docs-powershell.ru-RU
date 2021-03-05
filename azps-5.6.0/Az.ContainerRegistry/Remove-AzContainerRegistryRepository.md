---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: 1c0ad2ae46987a526be4e8fda110dada914bd27e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975448"
---
# <span data-ttu-id="9a060-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="9a060-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="9a060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a060-102">SYNOPSIS</span></span>
<span data-ttu-id="9a060-103">Удалите репозиторий из ACR.</span><span class="sxs-lookup"><span data-stu-id="9a060-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="9a060-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a060-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a060-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a060-105">DESCRIPTION</span></span>
<span data-ttu-id="9a060-106">Удалите репозиторий из ACR.</span><span class="sxs-lookup"><span data-stu-id="9a060-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="9a060-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a060-107">EXAMPLES</span></span>

### <span data-ttu-id="9a060-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a060-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="9a060-109">Удалить тест репозитория/busybox15 в реестре.</span><span class="sxs-lookup"><span data-stu-id="9a060-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="9a060-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a060-110">PARAMETERS</span></span>

### <span data-ttu-id="9a060-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a060-111">-DefaultProfile</span></span>
<span data-ttu-id="9a060-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a060-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a060-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9a060-113">-Name</span></span>
<span data-ttu-id="9a060-114">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="9a060-114">Repository Name.</span></span>

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

### <span data-ttu-id="9a060-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="9a060-115">-RegistryName</span></span>
<span data-ttu-id="9a060-116">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="9a060-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="9a060-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a060-117">-Confirm</span></span>
<span data-ttu-id="9a060-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a060-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a060-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a060-119">-WhatIf</span></span>
<span data-ttu-id="9a060-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a060-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a060-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a060-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a060-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a060-122">CommonParameters</span></span>
<span data-ttu-id="9a060-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a060-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a060-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a060-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a060-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a060-125">INPUTS</span></span>

### <span data-ttu-id="9a060-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9a060-126">System.String</span></span>

## <span data-ttu-id="9a060-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a060-127">OUTPUTS</span></span>

### <span data-ttu-id="9a060-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="9a060-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="9a060-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a060-129">NOTES</span></span>

## <span data-ttu-id="9a060-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a060-130">RELATED LINKS</span></span>
