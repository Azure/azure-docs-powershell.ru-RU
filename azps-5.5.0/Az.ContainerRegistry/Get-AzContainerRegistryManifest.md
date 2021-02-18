---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 2fa58235c0ba18042fde13ce9f8d3fb396940d07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230985"
---
# <span data-ttu-id="725ab-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="725ab-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="725ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="725ab-102">SYNOPSIS</span></span>
<span data-ttu-id="725ab-103">Получить или высвеять манифест ACR.</span><span class="sxs-lookup"><span data-stu-id="725ab-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="725ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="725ab-104">SYNTAX</span></span>

### <span data-ttu-id="725ab-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="725ab-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="725ab-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="725ab-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="725ab-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="725ab-107">DESCRIPTION</span></span>
<span data-ttu-id="725ab-108">Получить или высвеять манифест ACR.</span><span class="sxs-lookup"><span data-stu-id="725ab-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="725ab-109">Чтобы использовать этот cmdlet, запустите `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="725ab-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="725ab-110">в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="725ab-110">first.</span></span>

## <span data-ttu-id="725ab-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="725ab-111">EXAMPLES</span></span>

### <span data-ttu-id="725ab-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="725ab-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="725ab-113">Манифесты списков для репозиториев в реестре.</span><span class="sxs-lookup"><span data-stu-id="725ab-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="725ab-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="725ab-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="725ab-115">Получите манифесты sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 для репозитория alpine в реестре.</span><span class="sxs-lookup"><span data-stu-id="725ab-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="725ab-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="725ab-116">PARAMETERS</span></span>

### <span data-ttu-id="725ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="725ab-117">-DefaultProfile</span></span>
<span data-ttu-id="725ab-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="725ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="725ab-119">-Name</span><span class="sxs-lookup"><span data-stu-id="725ab-119">-Name</span></span>
<span data-ttu-id="725ab-120">Ссылка на манифест.</span><span class="sxs-lookup"><span data-stu-id="725ab-120">Manifest reference.</span></span>

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

### <span data-ttu-id="725ab-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="725ab-121">-RegistryName</span></span>
<span data-ttu-id="725ab-122">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="725ab-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="725ab-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="725ab-123">-RepositoryName</span></span>
<span data-ttu-id="725ab-124">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="725ab-124">Repository Name.</span></span>

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

### <span data-ttu-id="725ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="725ab-125">CommonParameters</span></span>
<span data-ttu-id="725ab-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="725ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="725ab-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="725ab-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="725ab-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="725ab-128">INPUTS</span></span>

### <span data-ttu-id="725ab-129">System.String</span><span class="sxs-lookup"><span data-stu-id="725ab-129">System.String</span></span>

## <span data-ttu-id="725ab-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="725ab-130">OUTPUTS</span></span>

### <span data-ttu-id="725ab-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="725ab-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="725ab-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span><span class="sxs-lookup"><span data-stu-id="725ab-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="725ab-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="725ab-133">NOTES</span></span>

## <span data-ttu-id="725ab-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="725ab-134">RELATED LINKS</span></span>
