---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211393"
---
# <span data-ttu-id="b7ed8-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b7ed8-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="b7ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ed8-103">Обновляет веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="b7ed8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7ed8-104">SYNTAX</span></span>

### <span data-ttu-id="b7ed8-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7ed8-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ed8-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ed8-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ed8-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ed8-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ed8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7ed8-108">DESCRIPTION</span></span>
<span data-ttu-id="b7ed8-109">Новый Update-AzContainerRegistryWebhook обновляет веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="b7ed8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7ed8-110">EXAMPLES</span></span>

### <span data-ttu-id="b7ed8-111">Пример 1. Обновление веб-приложения реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="b7ed8-112">Обновив существующий веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="b7ed8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7ed8-113">PARAMETERS</span></span>

### <span data-ttu-id="b7ed8-114">-Action</span><span class="sxs-lookup"><span data-stu-id="b7ed8-114">-Action</span></span>
<span data-ttu-id="b7ed8-115">Разделенный пробелом список действий, которые запускают веб-сайт для публикации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ed8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ed8-116">-DefaultProfile</span></span>
<span data-ttu-id="b7ed8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7ed8-118">-Header</span><span class="sxs-lookup"><span data-stu-id="b7ed8-118">-Header</span></span>
<span data-ttu-id="b7ed8-119">Разделять пробелы пользовательскими headers в формате key =value, который будет добавляться в уведомления \[ \] webhook.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="b7ed8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b7ed8-120">-Name</span></span>
<span data-ttu-id="b7ed8-121">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-121">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ed8-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b7ed8-122">-RegistryName</span></span>
<span data-ttu-id="b7ed8-123">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="b7ed8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ed8-124">-ResourceGroupName</span></span>
<span data-ttu-id="b7ed8-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7ed8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ed8-126">-ResourceId</span></span>
<span data-ttu-id="b7ed8-127">ИД ресурса Webhook реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="b7ed8-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="b7ed8-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="b7ed8-128">-Scope</span></span>
<span data-ttu-id="b7ed8-129">Область webhook.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-129">Webhook scope.</span></span>

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

### <span data-ttu-id="b7ed8-130">-Status</span><span class="sxs-lookup"><span data-stu-id="b7ed8-130">-Status</span></span>
<span data-ttu-id="b7ed8-131">Состояние Webhook</span><span class="sxs-lookup"><span data-stu-id="b7ed8-131">Webhook status</span></span>

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

### <span data-ttu-id="b7ed8-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7ed8-132">-Tag</span></span>
<span data-ttu-id="b7ed8-133">Пробел, разделенный тегами в формате key \[ \] =value.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="b7ed8-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="b7ed8-134">-Uri</span></span>
<span data-ttu-id="b7ed8-135">URI службы для веб-приложения для публикации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ed8-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="b7ed8-136">-Webhook</span></span>
<span data-ttu-id="b7ed8-137">Объект Container Registry Webhook.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-137">Container Registry Webhook Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ed8-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7ed8-138">-Confirm</span></span>
<span data-ttu-id="b7ed8-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ed8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ed8-140">-WhatIf</span></span>
<span data-ttu-id="b7ed8-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7ed8-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7ed8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ed8-143">CommonParameters</span></span>
<span data-ttu-id="b7ed8-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ed8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ed8-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7ed8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ed8-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7ed8-146">INPUTS</span></span>

### <span data-ttu-id="b7ed8-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b7ed8-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="b7ed8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b7ed8-148">System.String</span></span>

## <span data-ttu-id="b7ed8-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7ed8-149">OUTPUTS</span></span>

### <span data-ttu-id="b7ed8-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b7ed8-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="b7ed8-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7ed8-151">NOTES</span></span>

## <span data-ttu-id="b7ed8-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7ed8-152">RELATED LINKS</span></span>

[<span data-ttu-id="b7ed8-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b7ed8-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b7ed8-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b7ed8-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b7ed8-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b7ed8-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b7ed8-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b7ed8-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)