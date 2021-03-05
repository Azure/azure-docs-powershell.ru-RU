---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 5477dc0402d79228a9283f9c9e88b0fd34e425ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004419"
---
# <span data-ttu-id="a2305-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="a2305-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="a2305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2305-102">SYNOPSIS</span></span>
<span data-ttu-id="a2305-103">Получить или перечислить манифест ACR.</span><span class="sxs-lookup"><span data-stu-id="a2305-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="a2305-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2305-104">SYNTAX</span></span>

### <span data-ttu-id="a2305-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2305-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2305-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2305-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2305-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2305-107">DESCRIPTION</span></span>
<span data-ttu-id="a2305-108">Получить или перечислить манифест ACR.</span><span class="sxs-lookup"><span data-stu-id="a2305-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="a2305-109">Чтобы использовать этот cmdlet, запустите `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="a2305-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="a2305-110">в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="a2305-110">first.</span></span>

## <span data-ttu-id="a2305-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2305-111">EXAMPLES</span></span>

### <span data-ttu-id="a2305-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2305-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="a2305-113">Манифесты списков для репозиториев в реестре.</span><span class="sxs-lookup"><span data-stu-id="a2305-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="a2305-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a2305-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="a2305-115">Получите манифесты sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 для репозитория alpine в реестре.</span><span class="sxs-lookup"><span data-stu-id="a2305-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="a2305-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2305-116">PARAMETERS</span></span>

### <span data-ttu-id="a2305-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2305-117">-DefaultProfile</span></span>
<span data-ttu-id="a2305-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2305-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2305-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a2305-119">-Name</span></span>
<span data-ttu-id="a2305-120">Ссылка на манифест.</span><span class="sxs-lookup"><span data-stu-id="a2305-120">Manifest reference.</span></span>

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

### <span data-ttu-id="a2305-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="a2305-121">-RegistryName</span></span>
<span data-ttu-id="a2305-122">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="a2305-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="a2305-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="a2305-123">-RepositoryName</span></span>
<span data-ttu-id="a2305-124">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="a2305-124">Repository Name.</span></span>

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

### <span data-ttu-id="a2305-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2305-125">CommonParameters</span></span>
<span data-ttu-id="a2305-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2305-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2305-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2305-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2305-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2305-128">INPUTS</span></span>

### <span data-ttu-id="a2305-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a2305-129">System.String</span></span>

## <span data-ttu-id="a2305-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2305-130">OUTPUTS</span></span>

### <span data-ttu-id="a2305-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="a2305-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="a2305-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span><span class="sxs-lookup"><span data-stu-id="a2305-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="a2305-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2305-133">NOTES</span></span>

## <span data-ttu-id="a2305-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2305-134">RELATED LINKS</span></span>
