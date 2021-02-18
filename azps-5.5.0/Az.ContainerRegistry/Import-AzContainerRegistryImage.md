---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230977"
---
# <span data-ttu-id="5dd70-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="5dd70-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="5dd70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dd70-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd70-103">Импорт изображения из общеугорного или azure реестра в реестр контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="5dd70-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="5dd70-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5dd70-104">SYNTAX</span></span>

### <span data-ttu-id="5dd70-105">ImportImageByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5dd70-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dd70-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="5dd70-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dd70-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="5dd70-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dd70-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="5dd70-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dd70-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dd70-109">DESCRIPTION</span></span>
<span data-ttu-id="5dd70-110">Импорт изображения из общеугорного или azure реестра в реестр контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="5dd70-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="5dd70-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5dd70-111">EXAMPLES</span></span>

### <span data-ttu-id="5dd70-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5dd70-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="5dd70-113">Импорт занятого почтового ящика в ACR.</span><span class="sxs-lookup"><span data-stu-id="5dd70-113">Import busybox to ACR.</span></span> <span data-ttu-id="5dd70-114">Примечание.</span><span class="sxs-lookup"><span data-stu-id="5dd70-114">Note:</span></span> 
* <span data-ttu-id="5dd70-115">Перед исходным изображением нужно добавить "библиотека/".</span><span class="sxs-lookup"><span data-stu-id="5dd70-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="5dd70-116">"busybox:latest" => "library/busybox:latest"</span><span class="sxs-lookup"><span data-stu-id="5dd70-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="5dd70-117">Учетные данные необходимы, если исходный реестр не является общедоступным</span><span class="sxs-lookup"><span data-stu-id="5dd70-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="5dd70-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5dd70-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="5dd70-119">Импортировать занятое время из источника ACR, чтобы нацелить ACR.</span><span class="sxs-lookup"><span data-stu-id="5dd70-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="5dd70-120">Примечание.</span><span class="sxs-lookup"><span data-stu-id="5dd70-120">Note:</span></span> 
* <span data-ttu-id="5dd70-121">Учетные данные необходимы, если пользователь администратора для реестра источника отключен.</span><span class="sxs-lookup"><span data-stu-id="5dd70-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="5dd70-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dd70-122">PARAMETERS</span></span>

### <span data-ttu-id="5dd70-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dd70-123">-DefaultProfile</span></span>
<span data-ttu-id="5dd70-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dd70-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dd70-125">-Mode</span><span class="sxs-lookup"><span data-stu-id="5dd70-125">-Mode</span></span>
<span data-ttu-id="5dd70-126">При принудительном перезаписи всех существующих целевых тегов.</span><span class="sxs-lookup"><span data-stu-id="5dd70-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="5dd70-127">При работе с NoForce все существующие целевые теги не будут работать до начала копирования.</span><span class="sxs-lookup"><span data-stu-id="5dd70-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd70-128">-Password</span><span class="sxs-lookup"><span data-stu-id="5dd70-128">-Password</span></span>
<span data-ttu-id="5dd70-129">Пароль, используемый для проверки подлинности в реестре источника.</span><span class="sxs-lookup"><span data-stu-id="5dd70-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd70-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5dd70-130">-RegistryName</span></span>
<span data-ttu-id="5dd70-131">Имя целевого реестра.</span><span class="sxs-lookup"><span data-stu-id="5dd70-131">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd70-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dd70-132">-ResourceGroupName</span></span>
<span data-ttu-id="5dd70-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5dd70-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd70-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="5dd70-134">-SourceImage</span></span>
<span data-ttu-id="5dd70-135">Имя репозитория для изображения источника.</span><span class="sxs-lookup"><span data-stu-id="5dd70-135">Repository name of the source image.</span></span>

<span data-ttu-id="5dd70-136">Укажите изображение по репозиторию (привет, мир).)</span><span class="sxs-lookup"><span data-stu-id="5dd70-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="5dd70-137">Будет применяться новейший тег.</span><span class="sxs-lookup"><span data-stu-id="5dd70-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="5dd70-138">Укажите изображение по тегу ('hello-world:latest').</span><span class="sxs-lookup"><span data-stu-id="5dd70-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="5dd70-139">Указание изображения с помощью дайджеста манифеста на основе sha256 (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="5dd70-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="5dd70-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="5dd70-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="5dd70-141">Идентификатор ресурса в реестре контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="5dd70-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd70-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="5dd70-142">-SourceRegistryUri</span></span>
<span data-ttu-id="5dd70-143">Адрес реестра источника (например, "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="5dd70-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd70-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="5dd70-144">-TargetTag</span></span>
<span data-ttu-id="5dd70-145">Список строк repo формы \[ \] :tag.</span><span class="sxs-lookup"><span data-stu-id="5dd70-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="5dd70-146">Если этот тег опущен, источник будет использоваться (или "последний", если также опущен исходный тег).</span><span class="sxs-lookup"><span data-stu-id="5dd70-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd70-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="5dd70-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="5dd70-148">Список строк с именами репозитория, которые нужно скопировать только для манифеста.</span><span class="sxs-lookup"><span data-stu-id="5dd70-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="5dd70-149">Тег не будет создан.</span><span class="sxs-lookup"><span data-stu-id="5dd70-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd70-150">-Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="5dd70-150">-Username</span></span>
<span data-ttu-id="5dd70-151">Имя пользователя для проверки подлинности в реестре источника.</span><span class="sxs-lookup"><span data-stu-id="5dd70-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd70-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dd70-152">-Confirm</span></span>
<span data-ttu-id="5dd70-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5dd70-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dd70-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dd70-154">-WhatIf</span></span>
<span data-ttu-id="5dd70-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dd70-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dd70-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5dd70-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dd70-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd70-157">CommonParameters</span></span>
<span data-ttu-id="5dd70-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dd70-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd70-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5dd70-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd70-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5dd70-160">INPUTS</span></span>

### <span data-ttu-id="5dd70-161">System.String</span><span class="sxs-lookup"><span data-stu-id="5dd70-161">System.String</span></span>

## <span data-ttu-id="5dd70-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5dd70-162">OUTPUTS</span></span>

### <span data-ttu-id="5dd70-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5dd70-163">System.Boolean</span></span>

## <span data-ttu-id="5dd70-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5dd70-164">NOTES</span></span>

## <span data-ttu-id="5dd70-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dd70-165">RELATED LINKS</span></span>
