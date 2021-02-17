---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233196"
---
# <span data-ttu-id="23e58-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="23e58-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="23e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23e58-102">SYNOPSIS</span></span>
<span data-ttu-id="23e58-103">Создает веб-сайт контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="23e58-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="23e58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23e58-104">SYNTAX</span></span>

### <span data-ttu-id="23e58-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23e58-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23e58-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e58-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e58-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e58-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e58-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23e58-108">DESCRIPTION</span></span>
<span data-ttu-id="23e58-109">С New-AzContainerRegistryWebhook создается веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="23e58-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="23e58-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23e58-110">EXAMPLES</span></span>

### <span data-ttu-id="23e58-111">Пример 1. Создание веб-приложения реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="23e58-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="23e58-112">Создайте веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="23e58-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="23e58-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23e58-113">PARAMETERS</span></span>

### <span data-ttu-id="23e58-114">-Action</span><span class="sxs-lookup"><span data-stu-id="23e58-114">-Action</span></span>
<span data-ttu-id="23e58-115">Разделенный пробелом список действий, которые запускают веб-сайт для публикации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="23e58-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e58-116">-DefaultProfile</span></span>
<span data-ttu-id="23e58-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23e58-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23e58-118">-Header</span><span class="sxs-lookup"><span data-stu-id="23e58-118">-Header</span></span>
<span data-ttu-id="23e58-119">Настраиваемые headers, которые будут добавлены в уведомления веб-службы.</span><span class="sxs-lookup"><span data-stu-id="23e58-119">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-120">-Location</span><span class="sxs-lookup"><span data-stu-id="23e58-120">-Location</span></span>
<span data-ttu-id="23e58-121">Расположение Webhook.</span><span class="sxs-lookup"><span data-stu-id="23e58-121">Webhook Location.</span></span>
<span data-ttu-id="23e58-122">Значение по умолчанию для расположения реестра.</span><span class="sxs-lookup"><span data-stu-id="23e58-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-123">-Name</span><span class="sxs-lookup"><span data-stu-id="23e58-123">-Name</span></span>
<span data-ttu-id="23e58-124">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="23e58-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="23e58-125">-Registry</span></span>
<span data-ttu-id="23e58-126">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="23e58-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="23e58-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="23e58-127">-RegistryName</span></span>
<span data-ttu-id="23e58-128">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="23e58-128">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e58-129">-ResourceGroupName</span></span>
<span data-ttu-id="23e58-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23e58-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23e58-131">-ResourceId</span></span>
<span data-ttu-id="23e58-132">ИД ресурса контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="23e58-132">The container registry resource id</span></span>

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

### <span data-ttu-id="23e58-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="23e58-133">-Scope</span></span>
<span data-ttu-id="23e58-134">Область действия Webhook.</span><span class="sxs-lookup"><span data-stu-id="23e58-134">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-135">-Status</span><span class="sxs-lookup"><span data-stu-id="23e58-135">-Status</span></span>
<span data-ttu-id="23e58-136">Состояние Webhook, значение по умолчанию включено</span><span class="sxs-lookup"><span data-stu-id="23e58-136">Webhook status, default value is enabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="23e58-137">-Tag</span></span>
<span data-ttu-id="23e58-138">Теги Webhook.</span><span class="sxs-lookup"><span data-stu-id="23e58-138">Webhook tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="23e58-139">-Uri</span></span>
<span data-ttu-id="23e58-140">URI службы для веб-приложения для публикации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="23e58-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e58-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23e58-141">-Confirm</span></span>
<span data-ttu-id="23e58-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="23e58-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e58-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e58-143">-WhatIf</span></span>
<span data-ttu-id="23e58-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e58-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e58-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="23e58-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e58-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e58-146">CommonParameters</span></span>
<span data-ttu-id="23e58-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e58-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e58-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23e58-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e58-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23e58-149">INPUTS</span></span>

### <span data-ttu-id="23e58-150">System.String</span><span class="sxs-lookup"><span data-stu-id="23e58-150">System.String</span></span>

## <span data-ttu-id="23e58-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23e58-151">OUTPUTS</span></span>

### <span data-ttu-id="23e58-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="23e58-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="23e58-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23e58-153">NOTES</span></span>

## <span data-ttu-id="23e58-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23e58-154">RELATED LINKS</span></span>

[<span data-ttu-id="23e58-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="23e58-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="23e58-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="23e58-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="23e58-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="23e58-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="23e58-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="23e58-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)