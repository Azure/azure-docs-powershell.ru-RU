---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246745"
---
# <span data-ttu-id="2da3d-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2da3d-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="2da3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2da3d-102">SYNOPSIS</span></span>
<span data-ttu-id="2da3d-103">Получает веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="2da3d-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="2da3d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2da3d-104">SYNTAX</span></span>

### <span data-ttu-id="2da3d-105">ListWebhookByNameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2da3d-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da3d-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da3d-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da3d-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da3d-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da3d-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da3d-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da3d-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da3d-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2da3d-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2da3d-110">DESCRIPTION</span></span>
<span data-ttu-id="2da3d-111">Командлет Get-AzContainerRegistryWebhook получает указанный веб-перехватчик реестра контейнера или все веб-перехватчики реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="2da3d-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="2da3d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2da3d-112">EXAMPLES</span></span>

### <span data-ttu-id="2da3d-113">Пример 1: получение указанного веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="2da3d-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="2da3d-114">Получение указанного веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="2da3d-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="2da3d-115">Пример 2: получение всех веб-перехватчиков реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="2da3d-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="2da3d-116">Получение всех веб-перехватчиков в реестре контейнера</span><span class="sxs-lookup"><span data-stu-id="2da3d-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="2da3d-117">Пример 3: получение указанного веб-перехватчика реестра контейнера с подробными сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="2da3d-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="2da3d-118">Получение указанного веб-перехватчика реестра контейнера с подробными сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="2da3d-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="2da3d-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2da3d-119">PARAMETERS</span></span>

### <span data-ttu-id="2da3d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da3d-120">-DefaultProfile</span></span>
<span data-ttu-id="2da3d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2da3d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2da3d-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2da3d-122">-IncludeConfiguration</span></span>
<span data-ttu-id="2da3d-123">Получение сведений о конфигурации для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="2da3d-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="2da3d-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2da3d-124">-Name</span></span>
<span data-ttu-id="2da3d-125">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="2da3d-125">Webhook Name.</span></span>

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

### <span data-ttu-id="2da3d-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="2da3d-126">-Registry</span></span>
<span data-ttu-id="2da3d-127">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="2da3d-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="2da3d-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2da3d-128">-RegistryName</span></span>
<span data-ttu-id="2da3d-129">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="2da3d-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="2da3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="2da3d-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2da3d-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="2da3d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2da3d-132">-ResourceId</span></span>
<span data-ttu-id="2da3d-133">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="2da3d-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="2da3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da3d-134">CommonParameters</span></span>
<span data-ttu-id="2da3d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2da3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da3d-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2da3d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da3d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2da3d-137">INPUTS</span></span>

### <span data-ttu-id="2da3d-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2da3d-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="2da3d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2da3d-139">System.String</span></span>

## <span data-ttu-id="2da3d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2da3d-140">OUTPUTS</span></span>

### <span data-ttu-id="2da3d-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2da3d-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="2da3d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2da3d-142">NOTES</span></span>

## <span data-ttu-id="2da3d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2da3d-143">RELATED LINKS</span></span>

[<span data-ttu-id="2da3d-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2da3d-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="2da3d-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2da3d-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="2da3d-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2da3d-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="2da3d-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="2da3d-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)