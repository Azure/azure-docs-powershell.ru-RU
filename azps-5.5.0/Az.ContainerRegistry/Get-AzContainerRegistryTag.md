---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 88bf3648f416efa69576c6b09a0d59f0d0d0fa76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215545"
---
# <span data-ttu-id="e5b2d-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="e5b2d-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="e5b2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b2d-103">Получить или перечислить тег ACR.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="e5b2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5b2d-104">SYNTAX</span></span>

### <span data-ttu-id="e5b2d-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5b2d-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5b2d-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b2d-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5b2d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5b2d-107">DESCRIPTION</span></span>
<span data-ttu-id="e5b2d-108">Получить или скрестить тег ACR.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-108">Get or list ACR tag.</span></span>
<span data-ttu-id="e5b2d-109">Чтобы использовать этот cmdlet, запустите `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="e5b2d-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="e5b2d-110">в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-110">first.</span></span>

## <span data-ttu-id="e5b2d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5b2d-111">EXAMPLES</span></span>

### <span data-ttu-id="e5b2d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5b2d-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="e5b2d-113">Теги списка для репозиториев в реестре.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="e5b2d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5b2d-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="e5b2d-115">Получите новейшие теги для репозиториев в реестре.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="e5b2d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5b2d-116">PARAMETERS</span></span>

### <span data-ttu-id="e5b2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b2d-117">-DefaultProfile</span></span>
<span data-ttu-id="e5b2d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5b2d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e5b2d-119">-Name</span></span>
<span data-ttu-id="e5b2d-120">Тег.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-120">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b2d-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e5b2d-121">-RegistryName</span></span>
<span data-ttu-id="e5b2d-122">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="e5b2d-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="e5b2d-123">-RepositoryName</span></span>
<span data-ttu-id="e5b2d-124">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-124">Repository Name.</span></span>

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

### <span data-ttu-id="e5b2d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b2d-125">CommonParameters</span></span>
<span data-ttu-id="e5b2d-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b2d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b2d-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5b2d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b2d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5b2d-128">INPUTS</span></span>

### <span data-ttu-id="e5b2d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e5b2d-129">System.String</span></span>

## <span data-ttu-id="e5b2d-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5b2d-130">OUTPUTS</span></span>

### <span data-ttu-id="e5b2d-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="e5b2d-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="e5b2d-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="e5b2d-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="e5b2d-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5b2d-133">NOTES</span></span>

## <span data-ttu-id="e5b2d-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5b2d-134">RELATED LINKS</span></span>
