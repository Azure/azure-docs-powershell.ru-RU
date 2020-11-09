---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311888"
---
# <span data-ttu-id="f9395-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="f9395-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="f9395-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9395-102">SYNOPSIS</span></span>
<span data-ttu-id="f9395-103">Импорт изображения из общедоступного раздела или реестра Azure в реестр контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="f9395-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="f9395-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9395-104">SYNTAX</span></span>

### <span data-ttu-id="f9395-105">ImportImageByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f9395-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9395-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="f9395-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9395-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="f9395-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9395-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="f9395-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9395-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9395-109">DESCRIPTION</span></span>
<span data-ttu-id="f9395-110">Импорт изображения из общедоступного раздела или реестра Azure в реестр контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="f9395-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="f9395-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9395-111">EXAMPLES</span></span>

### <span data-ttu-id="f9395-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9395-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="f9395-113">Импорт busybox в запись контроля доступа.</span><span class="sxs-lookup"><span data-stu-id="f9395-113">Import busybox to ACR.</span></span> <span data-ttu-id="f9395-114">Обратите внимание</span><span class="sxs-lookup"><span data-stu-id="f9395-114">Note:</span></span> 
* <span data-ttu-id="f9395-115">"Library/" необходимо добавить перед исходным изображением.</span><span class="sxs-lookup"><span data-stu-id="f9395-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="f9395-116">"busybox: latest" => "Library/busybox: latest"</span><span class="sxs-lookup"><span data-stu-id="f9395-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="f9395-117">Учетные данные необходимы, если исходный реестр недоступен для общего доступа</span><span class="sxs-lookup"><span data-stu-id="f9395-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="f9395-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f9395-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="f9395-119">Импортируйте BusyBox из исходной контроля доступа на целевую запись контроля доступа.</span><span class="sxs-lookup"><span data-stu-id="f9395-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="f9395-120">Обратите внимание</span><span class="sxs-lookup"><span data-stu-id="f9395-120">Note:</span></span> 
* <span data-ttu-id="f9395-121">Учетные данные необходимы, если пользователь администратора для исходного реестра отключен.</span><span class="sxs-lookup"><span data-stu-id="f9395-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="f9395-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9395-122">PARAMETERS</span></span>

### <span data-ttu-id="f9395-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9395-123">-DefaultProfile</span></span>
<span data-ttu-id="f9395-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9395-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9395-125">Режим</span><span class="sxs-lookup"><span data-stu-id="f9395-125">-Mode</span></span>
<span data-ttu-id="f9395-126">В случае принудительного применения все существующие целевые теги будут переписаны.</span><span class="sxs-lookup"><span data-stu-id="f9395-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="f9395-127">Если значение "непринудительно", любые существующие целевые теги не смогут выполнить операцию перед началом копирования.</span><span class="sxs-lookup"><span data-stu-id="f9395-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

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

### <span data-ttu-id="f9395-128">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="f9395-128">-Password</span></span>
<span data-ttu-id="f9395-129">Пароль, используемый для проверки подлинности в исходном реестре.</span><span class="sxs-lookup"><span data-stu-id="f9395-129">The password used to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="f9395-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f9395-130">-RegistryName</span></span>
<span data-ttu-id="f9395-131">Целевое имя реестра.</span><span class="sxs-lookup"><span data-stu-id="f9395-131">Target registry name.</span></span>

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

### <span data-ttu-id="f9395-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9395-132">-ResourceGroupName</span></span>
<span data-ttu-id="f9395-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9395-133">Resource group name.</span></span>

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

### <span data-ttu-id="f9395-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="f9395-134">-SourceImage</span></span>
<span data-ttu-id="f9395-135">Имя репозитория исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="f9395-135">Repository name of the source image.</span></span>

<span data-ttu-id="f9395-136">Укажите изображение в репозитории ("Hello-World").</span><span class="sxs-lookup"><span data-stu-id="f9395-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="f9395-137">В этом случае будет использоваться тег "последние".</span><span class="sxs-lookup"><span data-stu-id="f9395-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="f9395-138">Укажите изображение по тегу ("Hello-World: latest").</span><span class="sxs-lookup"><span data-stu-id="f9395-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="f9395-139">Указание изображения с помощью дайджеста манифеста на основе SHA256 (" hello-world@sha256:abc123 ").</span><span class="sxs-lookup"><span data-stu-id="f9395-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="f9395-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="f9395-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="f9395-141">Идентификатор ресурса для реестра исходного контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="f9395-141">The resource identifier of the source Azure Container Registry.</span></span>

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

### <span data-ttu-id="f9395-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="f9395-142">-SourceRegistryUri</span></span>
<span data-ttu-id="f9395-143">Адрес исходного реестра (например, "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="f9395-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

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

### <span data-ttu-id="f9395-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="f9395-144">-TargetTag</span></span>
<span data-ttu-id="f9395-145">Список строк тега "репозиторий" формы \[ \] .</span><span class="sxs-lookup"><span data-stu-id="f9395-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="f9395-146">Если указан тег, будет использоваться источник (или "последние", если исходный тег также не указан).</span><span class="sxs-lookup"><span data-stu-id="f9395-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

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

### <span data-ttu-id="f9395-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="f9395-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="f9395-148">Список строк с именами репозитория, для которых требуется скопировать только манифест.</span><span class="sxs-lookup"><span data-stu-id="f9395-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="f9395-149">Тег не будет создан.</span><span class="sxs-lookup"><span data-stu-id="f9395-149">No tag will be created.</span></span>

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

### <span data-ttu-id="f9395-150">-Username</span><span class="sxs-lookup"><span data-stu-id="f9395-150">-Username</span></span>
<span data-ttu-id="f9395-151">Имя пользователя для проверки подлинности в исходном реестре.</span><span class="sxs-lookup"><span data-stu-id="f9395-151">The username to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="f9395-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9395-152">-Confirm</span></span>
<span data-ttu-id="f9395-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9395-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9395-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9395-154">-WhatIf</span></span>
<span data-ttu-id="f9395-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9395-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9395-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9395-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9395-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9395-157">CommonParameters</span></span>
<span data-ttu-id="f9395-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9395-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9395-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9395-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9395-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9395-160">INPUTS</span></span>

### <span data-ttu-id="f9395-161">System. String</span><span class="sxs-lookup"><span data-stu-id="f9395-161">System.String</span></span>

## <span data-ttu-id="f9395-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9395-162">OUTPUTS</span></span>

### <span data-ttu-id="f9395-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9395-163">System.Boolean</span></span>

## <span data-ttu-id="f9395-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9395-164">NOTES</span></span>

## <span data-ttu-id="f9395-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9395-165">RELATED LINKS</span></span>
