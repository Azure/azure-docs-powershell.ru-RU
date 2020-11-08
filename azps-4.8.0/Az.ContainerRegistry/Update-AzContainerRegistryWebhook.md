---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242882"
---
# <span data-ttu-id="b407a-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b407a-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="b407a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b407a-102">SYNOPSIS</span></span>
<span data-ttu-id="b407a-103">Обновление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b407a-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="b407a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b407a-104">SYNTAX</span></span>

### <span data-ttu-id="b407a-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b407a-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b407a-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b407a-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b407a-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b407a-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b407a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b407a-108">DESCRIPTION</span></span>
<span data-ttu-id="b407a-109">Командлет Update-AzContainerRegistryWebhook обновляет веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b407a-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="b407a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b407a-110">EXAMPLES</span></span>

### <span data-ttu-id="b407a-111">Пример 1: обновление существующего веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b407a-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="b407a-112">Обновите существующий веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b407a-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="b407a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b407a-113">PARAMETERS</span></span>

### <span data-ttu-id="b407a-114">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="b407a-114">-Action</span></span>
<span data-ttu-id="b407a-115">Список разделенных пробелами действий, которые инициируют веб-перехватчик для отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b407a-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="b407a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b407a-116">-DefaultProfile</span></span>
<span data-ttu-id="b407a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b407a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b407a-118">-Верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="b407a-118">-Header</span></span>
<span data-ttu-id="b407a-119">Пользовательские заголовки, разделенные пробелами \[ , в формате "Key = Value \] ", которые будут добавлены в уведомления веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="b407a-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="b407a-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b407a-120">-Name</span></span>
<span data-ttu-id="b407a-121">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="b407a-121">Webhook Name.</span></span>

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

### <span data-ttu-id="b407a-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b407a-122">-RegistryName</span></span>
<span data-ttu-id="b407a-123">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="b407a-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="b407a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b407a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b407a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b407a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b407a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b407a-126">-ResourceId</span></span>
<span data-ttu-id="b407a-127">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="b407a-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="b407a-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="b407a-128">-Scope</span></span>
<span data-ttu-id="b407a-129">Область веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="b407a-129">Webhook scope.</span></span>

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

### <span data-ttu-id="b407a-130">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="b407a-130">-Status</span></span>
<span data-ttu-id="b407a-131">Состояние веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="b407a-131">Webhook status</span></span>

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

### <span data-ttu-id="b407a-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="b407a-132">-Tag</span></span>
<span data-ttu-id="b407a-133">Теги, разделенные пробелами \[ , в формате "Key = Value \] ".</span><span class="sxs-lookup"><span data-stu-id="b407a-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="b407a-134">-URI</span><span class="sxs-lookup"><span data-stu-id="b407a-134">-Uri</span></span>
<span data-ttu-id="b407a-135">Универсальный код ресурса (URI) службы для веб-перехватчика для отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b407a-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="b407a-136">-Перехватчик</span><span class="sxs-lookup"><span data-stu-id="b407a-136">-Webhook</span></span>
<span data-ttu-id="b407a-137">Объект веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b407a-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="b407a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b407a-138">-Confirm</span></span>
<span data-ttu-id="b407a-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b407a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b407a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b407a-140">-WhatIf</span></span>
<span data-ttu-id="b407a-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b407a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b407a-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b407a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b407a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b407a-143">CommonParameters</span></span>
<span data-ttu-id="b407a-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b407a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b407a-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b407a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b407a-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b407a-146">INPUTS</span></span>

### <span data-ttu-id="b407a-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b407a-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="b407a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b407a-148">System.String</span></span>

## <span data-ttu-id="b407a-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b407a-149">OUTPUTS</span></span>

### <span data-ttu-id="b407a-150">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b407a-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="b407a-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="b407a-151">NOTES</span></span>

## <span data-ttu-id="b407a-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b407a-152">RELATED LINKS</span></span>

[<span data-ttu-id="b407a-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b407a-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b407a-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b407a-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b407a-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b407a-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b407a-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b407a-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)