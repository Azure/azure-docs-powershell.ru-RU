---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: b01b2e8152d74fda5faff36221ffa9b6e75ffcbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721601"
---
# <span data-ttu-id="6631b-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6631b-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="6631b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6631b-102">SYNOPSIS</span></span>
<span data-ttu-id="6631b-103">Получает веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="6631b-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="6631b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6631b-104">SYNTAX</span></span>

### <span data-ttu-id="6631b-105">ListWebhookByNameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6631b-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6631b-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6631b-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6631b-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6631b-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6631b-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6631b-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6631b-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6631b-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6631b-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6631b-110">DESCRIPTION</span></span>
<span data-ttu-id="6631b-111">Командлет Get-AzContainerRegistryWebhook получает указанный веб-перехватчик реестра контейнера или все веб-перехватчики реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="6631b-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="6631b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6631b-112">EXAMPLES</span></span>

### <span data-ttu-id="6631b-113">Пример 1: получение указанного веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="6631b-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="6631b-114">Получение указанного веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="6631b-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="6631b-115">Пример 2: получение всех веб-перехватчиков реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="6631b-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="6631b-116">Получение всех веб-перехватчиков в реестре контейнера</span><span class="sxs-lookup"><span data-stu-id="6631b-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="6631b-117">Пример 3: получение указанного веб-перехватчика реестра контейнера с подробными сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="6631b-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="6631b-118">Получение указанного веб-перехватчика реестра контейнера с подробными сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="6631b-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="6631b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6631b-119">PARAMETERS</span></span>

### <span data-ttu-id="6631b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6631b-120">-DefaultProfile</span></span>
<span data-ttu-id="6631b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6631b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6631b-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6631b-122">-IncludeConfiguration</span></span>
<span data-ttu-id="6631b-123">Получение сведений о конфигурации для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="6631b-123">Get the configuration information for a webhook.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6631b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6631b-124">-Name</span></span>
<span data-ttu-id="6631b-125">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="6631b-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6631b-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="6631b-126">-Registry</span></span>
<span data-ttu-id="6631b-127">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="6631b-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6631b-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6631b-128">-RegistryName</span></span>
<span data-ttu-id="6631b-129">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="6631b-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6631b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6631b-130">-ResourceGroupName</span></span>
<span data-ttu-id="6631b-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6631b-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6631b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6631b-132">-ResourceId</span></span>
<span data-ttu-id="6631b-133">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="6631b-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="6631b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6631b-134">CommonParameters</span></span>
<span data-ttu-id="6631b-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6631b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6631b-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6631b-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6631b-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6631b-137">INPUTS</span></span>

### <span data-ttu-id="6631b-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6631b-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="6631b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6631b-139">System.String</span></span>

## <span data-ttu-id="6631b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6631b-140">OUTPUTS</span></span>

### <span data-ttu-id="6631b-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6631b-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="6631b-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="6631b-142">NOTES</span></span>

## <span data-ttu-id="6631b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6631b-143">RELATED LINKS</span></span>

[<span data-ttu-id="6631b-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6631b-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="6631b-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6631b-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="6631b-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6631b-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="6631b-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6631b-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)