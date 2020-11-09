---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315113"
---
# <span data-ttu-id="76502-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="76502-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="76502-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76502-102">SYNOPSIS</span></span>
<span data-ttu-id="76502-103">Обновление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="76502-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="76502-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76502-104">SYNTAX</span></span>

### <span data-ttu-id="76502-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76502-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76502-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="76502-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76502-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76502-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76502-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76502-108">DESCRIPTION</span></span>
<span data-ttu-id="76502-109">Командлет Update-AzContainerRegistryWebhook обновляет веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="76502-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="76502-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76502-110">EXAMPLES</span></span>

### <span data-ttu-id="76502-111">Пример 1: обновление существующего веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="76502-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="76502-112">Обновите существующий веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="76502-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="76502-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76502-113">PARAMETERS</span></span>

### <span data-ttu-id="76502-114">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="76502-114">-Action</span></span>
<span data-ttu-id="76502-115">Список разделенных пробелами действий, которые инициируют веб-перехватчик для отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="76502-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="76502-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76502-116">-DefaultProfile</span></span>
<span data-ttu-id="76502-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76502-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76502-118">-Верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="76502-118">-Header</span></span>
<span data-ttu-id="76502-119">Пользовательские заголовки, разделенные пробелами \[ , в формате "Key = Value \] ", которые будут добавлены в уведомления веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="76502-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="76502-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76502-120">-Name</span></span>
<span data-ttu-id="76502-121">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="76502-121">Webhook Name.</span></span>

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

### <span data-ttu-id="76502-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="76502-122">-RegistryName</span></span>
<span data-ttu-id="76502-123">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="76502-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="76502-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76502-124">-ResourceGroupName</span></span>
<span data-ttu-id="76502-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76502-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="76502-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76502-126">-ResourceId</span></span>
<span data-ttu-id="76502-127">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="76502-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="76502-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="76502-128">-Scope</span></span>
<span data-ttu-id="76502-129">Область веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="76502-129">Webhook scope.</span></span>

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

### <span data-ttu-id="76502-130">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="76502-130">-Status</span></span>
<span data-ttu-id="76502-131">Состояние веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="76502-131">Webhook status</span></span>

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

### <span data-ttu-id="76502-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="76502-132">-Tag</span></span>
<span data-ttu-id="76502-133">Теги, разделенные пробелами \[ , в формате "Key = Value \] ".</span><span class="sxs-lookup"><span data-stu-id="76502-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="76502-134">-URI</span><span class="sxs-lookup"><span data-stu-id="76502-134">-Uri</span></span>
<span data-ttu-id="76502-135">Универсальный код ресурса (URI) службы для веб-перехватчика для отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="76502-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="76502-136">-Перехватчик</span><span class="sxs-lookup"><span data-stu-id="76502-136">-Webhook</span></span>
<span data-ttu-id="76502-137">Объект веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="76502-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="76502-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76502-138">-Confirm</span></span>
<span data-ttu-id="76502-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76502-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76502-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76502-140">-WhatIf</span></span>
<span data-ttu-id="76502-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76502-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76502-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76502-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76502-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76502-143">CommonParameters</span></span>
<span data-ttu-id="76502-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76502-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76502-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76502-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76502-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76502-146">INPUTS</span></span>

### <span data-ttu-id="76502-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="76502-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="76502-148">System. String</span><span class="sxs-lookup"><span data-stu-id="76502-148">System.String</span></span>

## <span data-ttu-id="76502-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76502-149">OUTPUTS</span></span>

### <span data-ttu-id="76502-150">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="76502-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="76502-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="76502-151">NOTES</span></span>

## <span data-ttu-id="76502-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76502-152">RELATED LINKS</span></span>

[<span data-ttu-id="76502-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="76502-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="76502-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="76502-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="76502-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="76502-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="76502-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="76502-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)