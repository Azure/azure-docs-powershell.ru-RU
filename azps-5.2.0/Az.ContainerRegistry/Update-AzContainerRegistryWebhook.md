---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406071"
---
# <span data-ttu-id="4d18c-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d18c-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="4d18c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d18c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d18c-103">Обновляет веб-сайт контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="4d18c-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="4d18c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4d18c-104">SYNTAX</span></span>

### <span data-ttu-id="4d18c-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d18c-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d18c-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d18c-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d18c-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d18c-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d18c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d18c-108">DESCRIPTION</span></span>
<span data-ttu-id="4d18c-109">Новый Update-AzContainerRegistryWebhook обновляет веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="4d18c-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="4d18c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4d18c-110">EXAMPLES</span></span>

### <span data-ttu-id="4d18c-111">Пример 1. Обновление существующего веб-приложения реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="4d18c-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="4d18c-112">Обновив существующий веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="4d18c-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="4d18c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d18c-113">PARAMETERS</span></span>

### <span data-ttu-id="4d18c-114">-Action</span><span class="sxs-lookup"><span data-stu-id="4d18c-114">-Action</span></span>
<span data-ttu-id="4d18c-115">Разделенный пробелом список действий, которые запускают веб-сайт для публикации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4d18c-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="4d18c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d18c-116">-DefaultProfile</span></span>
<span data-ttu-id="4d18c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d18c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d18c-118">-Header</span><span class="sxs-lookup"><span data-stu-id="4d18c-118">-Header</span></span>
<span data-ttu-id="4d18c-119">Разделять пробелы пользовательскими headers в формате key =value, который будет добавляться в уведомления \[ \] веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="4d18c-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="4d18c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4d18c-120">-Name</span></span>
<span data-ttu-id="4d18c-121">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="4d18c-121">Webhook Name.</span></span>

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

### <span data-ttu-id="4d18c-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4d18c-122">-RegistryName</span></span>
<span data-ttu-id="4d18c-123">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="4d18c-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="4d18c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d18c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d18c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d18c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4d18c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d18c-126">-ResourceId</span></span>
<span data-ttu-id="4d18c-127">ИД ресурса Webhook реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="4d18c-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="4d18c-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="4d18c-128">-Scope</span></span>
<span data-ttu-id="4d18c-129">Область действия Webhook.</span><span class="sxs-lookup"><span data-stu-id="4d18c-129">Webhook scope.</span></span>

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

### <span data-ttu-id="4d18c-130">-Status</span><span class="sxs-lookup"><span data-stu-id="4d18c-130">-Status</span></span>
<span data-ttu-id="4d18c-131">Состояние Webhook</span><span class="sxs-lookup"><span data-stu-id="4d18c-131">Webhook status</span></span>

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

### <span data-ttu-id="4d18c-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d18c-132">-Tag</span></span>
<span data-ttu-id="4d18c-133">Пробел, разделенный тегами в формате key \[ \] =value.</span><span class="sxs-lookup"><span data-stu-id="4d18c-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="4d18c-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="4d18c-134">-Uri</span></span>
<span data-ttu-id="4d18c-135">URI службы для веб-приложения для публикации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4d18c-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="4d18c-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="4d18c-136">-Webhook</span></span>
<span data-ttu-id="4d18c-137">Объект Container Registry Webhook.</span><span class="sxs-lookup"><span data-stu-id="4d18c-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="4d18c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d18c-138">-Confirm</span></span>
<span data-ttu-id="4d18c-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d18c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d18c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d18c-140">-WhatIf</span></span>
<span data-ttu-id="4d18c-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d18c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d18c-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4d18c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d18c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d18c-143">CommonParameters</span></span>
<span data-ttu-id="4d18c-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d18c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d18c-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d18c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d18c-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d18c-146">INPUTS</span></span>

### <span data-ttu-id="4d18c-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d18c-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="4d18c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="4d18c-148">System.String</span></span>

## <span data-ttu-id="4d18c-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4d18c-149">OUTPUTS</span></span>

### <span data-ttu-id="4d18c-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d18c-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="4d18c-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4d18c-151">NOTES</span></span>

## <span data-ttu-id="4d18c-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d18c-152">RELATED LINKS</span></span>

[<span data-ttu-id="4d18c-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d18c-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4d18c-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d18c-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4d18c-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d18c-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4d18c-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4d18c-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)