---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: efcd7fb518f66c99fab8b4cd456e8f8cea424ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990394"
---
# <span data-ttu-id="8051d-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="8051d-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="8051d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8051d-102">SYNOPSIS</span></span>
<span data-ttu-id="8051d-103">Получите репозитории ACR или со списком.</span><span class="sxs-lookup"><span data-stu-id="8051d-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="8051d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8051d-104">SYNTAX</span></span>

### <span data-ttu-id="8051d-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8051d-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8051d-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="8051d-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8051d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8051d-107">DESCRIPTION</span></span>
<span data-ttu-id="8051d-108">Получите репозитории ACR или со списком.</span><span class="sxs-lookup"><span data-stu-id="8051d-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="8051d-109">Список возвращает только имена репозитория.</span><span class="sxs-lookup"><span data-stu-id="8051d-109">List returns repository names only.</span></span>

## <span data-ttu-id="8051d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8051d-110">EXAMPLES</span></span>

### <span data-ttu-id="8051d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8051d-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="8051d-112">Список всех репозиториев в реестре.</span><span class="sxs-lookup"><span data-stu-id="8051d-112">List all repositories in registry.</span></span>

### <span data-ttu-id="8051d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8051d-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="8051d-114">Укаймь первые 3 репозитория в реестре.</span><span class="sxs-lookup"><span data-stu-id="8051d-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="8051d-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8051d-115">Example 3</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -Name alpine

Registry             : registry.azurecr.io
ImageName            : alpine
CreatedTime          : 2020-10-13T05:45:25.5896115Z
LastUpdateTime       : 2021-01-04T08:31:46.2406505Z
ManifestCount        : 7
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="8051d-116">Получите альпийский репозиторий в реестре.</span><span class="sxs-lookup"><span data-stu-id="8051d-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="8051d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8051d-117">PARAMETERS</span></span>

### <span data-ttu-id="8051d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8051d-118">-DefaultProfile</span></span>
<span data-ttu-id="8051d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8051d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8051d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8051d-120">-Name</span></span>
<span data-ttu-id="8051d-121">Имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="8051d-121">Repository Name.</span></span>

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

### <span data-ttu-id="8051d-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8051d-122">-RegistryName</span></span>
<span data-ttu-id="8051d-123">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="8051d-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="8051d-124">-First</span><span class="sxs-lookup"><span data-stu-id="8051d-124">-First</span></span>
<span data-ttu-id="8051d-125">Первые n результатов.</span><span class="sxs-lookup"><span data-stu-id="8051d-125">First n results.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8051d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8051d-126">CommonParameters</span></span>
<span data-ttu-id="8051d-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8051d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8051d-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8051d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8051d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8051d-129">INPUTS</span></span>

### <span data-ttu-id="8051d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8051d-130">System.String</span></span>

## <span data-ttu-id="8051d-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8051d-131">OUTPUTS</span></span>

### <span data-ttu-id="8051d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8051d-132">System.String</span></span>

### <span data-ttu-id="8051d-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="8051d-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="8051d-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8051d-134">NOTES</span></span>

## <span data-ttu-id="8051d-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8051d-135">RELATED LINKS</span></span>
