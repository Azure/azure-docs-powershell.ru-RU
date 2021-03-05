---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 5e20ae556cba16263d8b650de869b174236ccbd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004424"
---
# <span data-ttu-id="545d3-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="545d3-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="545d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="545d3-102">SYNOPSIS</span></span>
<span data-ttu-id="545d3-103">Получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="545d3-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="545d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="545d3-104">SYNTAX</span></span>

### <span data-ttu-id="545d3-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="545d3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="545d3-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="545d3-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="545d3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="545d3-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="545d3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="545d3-108">DESCRIPTION</span></span>
<span data-ttu-id="545d3-109">Новый Get-AzContainerRegistryCredential получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="545d3-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="545d3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="545d3-110">EXAMPLES</span></span>

### <span data-ttu-id="545d3-111">Пример 1. Получить учетные данные для входа в реестр контейнера</span><span class="sxs-lookup"><span data-stu-id="545d3-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="545d3-112">Эта команда получает учетные данные для указанного реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="545d3-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="545d3-113">Для получения учетных данных для входа в реестр контейнеров myRegistry необходимо включить \` пользователя-администратора. \`</span><span class="sxs-lookup"><span data-stu-id="545d3-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="545d3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="545d3-114">PARAMETERS</span></span>

### <span data-ttu-id="545d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545d3-115">-DefaultProfile</span></span>
<span data-ttu-id="545d3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="545d3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="545d3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="545d3-117">-Name</span></span>
<span data-ttu-id="545d3-118">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="545d3-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d3-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="545d3-119">-Registry</span></span>
<span data-ttu-id="545d3-120">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="545d3-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545d3-121">-ResourceGroupName</span></span>
<span data-ttu-id="545d3-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="545d3-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="545d3-123">-ResourceId</span></span>
<span data-ttu-id="545d3-124">ИД ресурса контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="545d3-124">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="545d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545d3-125">CommonParameters</span></span>
<span data-ttu-id="545d3-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="545d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545d3-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="545d3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545d3-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="545d3-128">INPUTS</span></span>

### <span data-ttu-id="545d3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="545d3-129">System.String</span></span>

## <span data-ttu-id="545d3-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="545d3-130">OUTPUTS</span></span>

### <span data-ttu-id="545d3-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="545d3-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="545d3-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="545d3-132">NOTES</span></span>

## <span data-ttu-id="545d3-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="545d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="545d3-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="545d3-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="545d3-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="545d3-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="545d3-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="545d3-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

