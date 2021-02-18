---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 2b102274b35d5f4f477376d3da8ad51bc6f0e694
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215548"
---
# <span data-ttu-id="ee0aa-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ee0aa-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="ee0aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee0aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ee0aa-103">Получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="ee0aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee0aa-104">SYNTAX</span></span>

### <span data-ttu-id="ee0aa-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee0aa-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee0aa-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee0aa-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee0aa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee0aa-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee0aa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee0aa-108">DESCRIPTION</span></span>
<span data-ttu-id="ee0aa-109">Этот Get-AzContainerRegistryCredential получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="ee0aa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee0aa-110">EXAMPLES</span></span>

### <span data-ttu-id="ee0aa-111">Пример 1. Получить учетные данные для входа в реестр контейнера</span><span class="sxs-lookup"><span data-stu-id="ee0aa-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="ee0aa-112">Эта команда получает учетные данные для указанного реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="ee0aa-113">Для получения учетных данных для входа в реестр контейнеров myRegistry необходимо включить \` \` пользователя-администратора.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="ee0aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee0aa-114">PARAMETERS</span></span>

### <span data-ttu-id="ee0aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee0aa-115">-DefaultProfile</span></span>
<span data-ttu-id="ee0aa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ee0aa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee0aa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ee0aa-117">-Name</span></span>
<span data-ttu-id="ee0aa-118">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="ee0aa-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="ee0aa-119">-Registry</span></span>
<span data-ttu-id="ee0aa-120">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="ee0aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee0aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="ee0aa-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee0aa-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee0aa-123">-ResourceId</span></span>
<span data-ttu-id="ee0aa-124">ИД контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="ee0aa-124">The container registry resource id</span></span>

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

### <span data-ttu-id="ee0aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee0aa-125">CommonParameters</span></span>
<span data-ttu-id="ee0aa-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee0aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee0aa-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee0aa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee0aa-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee0aa-128">INPUTS</span></span>

### <span data-ttu-id="ee0aa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ee0aa-129">System.String</span></span>

## <span data-ttu-id="ee0aa-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee0aa-130">OUTPUTS</span></span>

### <span data-ttu-id="ee0aa-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ee0aa-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="ee0aa-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee0aa-132">NOTES</span></span>

## <span data-ttu-id="ee0aa-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee0aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="ee0aa-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ee0aa-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="ee0aa-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ee0aa-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="ee0aa-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ee0aa-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

