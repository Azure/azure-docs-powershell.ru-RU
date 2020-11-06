---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a23cfb79c341fb4fcee5b5688b0780ba178e978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565541"
---
# <span data-ttu-id="cd68f-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cd68f-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="cd68f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd68f-102">SYNOPSIS</span></span>
<span data-ttu-id="cd68f-103">Создание веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="cd68f-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd68f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd68f-104">SYNTAX</span></span>

### <span data-ttu-id="cd68f-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd68f-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd68f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd68f-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd68f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd68f-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd68f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd68f-108">DESCRIPTION</span></span>
<span data-ttu-id="cd68f-109">Командлет New-AzureRmContainerRegistryWebhook создает веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="cd68f-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="cd68f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd68f-110">EXAMPLES</span></span>

### <span data-ttu-id="cd68f-111">Пример 1: создание веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="cd68f-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="cd68f-112">Создание веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="cd68f-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="cd68f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd68f-113">PARAMETERS</span></span>

### <span data-ttu-id="cd68f-114">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="cd68f-114">-Action</span></span>
<span data-ttu-id="cd68f-115">Список разделенных пробелами действий, которые инициируют веб-перехватчик для отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cd68f-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd68f-116">-Confirm</span></span>
<span data-ttu-id="cd68f-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd68f-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd68f-118">-DefaultProfile</span></span>
<span data-ttu-id="cd68f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd68f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-120">-Верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="cd68f-120">-Header</span></span>
<span data-ttu-id="cd68f-121">Пользовательские заголовки, которые будут добавлены в уведомления веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="cd68f-121">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-122">-Location</span><span class="sxs-lookup"><span data-stu-id="cd68f-122">-Location</span></span>
<span data-ttu-id="cd68f-123">Расположение веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="cd68f-123">Webhook Location.</span></span>
<span data-ttu-id="cd68f-124">По умолчанию — расположение реестра.</span><span class="sxs-lookup"><span data-stu-id="cd68f-124">Default to the location of the registry.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd68f-125">-Name</span></span>
<span data-ttu-id="cd68f-126">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="cd68f-126">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-127">-Registry</span><span class="sxs-lookup"><span data-stu-id="cd68f-127">-Registry</span></span>
<span data-ttu-id="cd68f-128">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="cd68f-128">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-129">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="cd68f-129">-RegistryName</span></span>
<span data-ttu-id="cd68f-130">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="cd68f-130">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd68f-131">-ResourceGroupName</span></span>
<span data-ttu-id="cd68f-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd68f-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd68f-133">-ResourceId</span></span>
<span data-ttu-id="cd68f-134">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="cd68f-134">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="cd68f-135">-Scope</span></span>
<span data-ttu-id="cd68f-136">Область веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="cd68f-136">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-137">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="cd68f-137">-Status</span></span>
<span data-ttu-id="cd68f-138">Состояние веб-перехватчика, значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="cd68f-138">Webhook status, default value is enabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="cd68f-139">-Tag</span></span>
<span data-ttu-id="cd68f-140">Теги веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="cd68f-140">Webhook tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-141">-URI</span><span class="sxs-lookup"><span data-stu-id="cd68f-141">-Uri</span></span>
<span data-ttu-id="cd68f-142">Универсальный код ресурса (URI) службы для веб-перехватчика для отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cd68f-142">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd68f-143">-WhatIf</span></span>
<span data-ttu-id="cd68f-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd68f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd68f-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd68f-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd68f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd68f-146">CommonParameters</span></span>
<span data-ttu-id="cd68f-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd68f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd68f-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd68f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd68f-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd68f-149">INPUTS</span></span>

### <span data-ttu-id="cd68f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cd68f-150">System.String</span></span>

## <span data-ttu-id="cd68f-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd68f-151">OUTPUTS</span></span>

### <span data-ttu-id="cd68f-152">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cd68f-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="cd68f-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd68f-153">NOTES</span></span>

## <span data-ttu-id="cd68f-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd68f-154">RELATED LINKS</span></span>

[<span data-ttu-id="cd68f-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cd68f-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="cd68f-156">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cd68f-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="cd68f-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cd68f-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="cd68f-158">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cd68f-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
