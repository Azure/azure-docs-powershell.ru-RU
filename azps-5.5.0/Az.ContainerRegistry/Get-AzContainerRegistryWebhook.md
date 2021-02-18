---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215537"
---
# <span data-ttu-id="5cd30-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5cd30-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="5cd30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd30-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd30-103">Получает веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="5cd30-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="5cd30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cd30-104">SYNTAX</span></span>

### <span data-ttu-id="5cd30-105">ListWebhookByNameResourceGroupParameterSet (default)</span><span class="sxs-lookup"><span data-stu-id="5cd30-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cd30-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cd30-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cd30-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cd30-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cd30-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cd30-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cd30-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cd30-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cd30-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cd30-110">DESCRIPTION</span></span>
<span data-ttu-id="5cd30-111">Этот Get-AzContainerRegistryWebhook получает указанный веб-сайт реестра контейнера или все веб-сайты реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="5cd30-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="5cd30-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cd30-112">EXAMPLES</span></span>

### <span data-ttu-id="5cd30-113">Пример 1. Получить указанный веб-сайт реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="5cd30-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="5cd30-114">Получить указанный веб-сайт реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="5cd30-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="5cd30-115">Пример 2. Получить все веб-сайты реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="5cd30-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="5cd30-116">Получить все веб-сайты реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="5cd30-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="5cd30-117">Пример 3. Получить определенный веб-сайт реестра контейнера со сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="5cd30-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="5cd30-118">Получить указанный веб-сайт реестра контейнера с подробными сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="5cd30-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="5cd30-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cd30-119">PARAMETERS</span></span>

### <span data-ttu-id="5cd30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd30-120">-DefaultProfile</span></span>
<span data-ttu-id="5cd30-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd30-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cd30-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cd30-122">-IncludeConfiguration</span></span>
<span data-ttu-id="5cd30-123">Получите сведения о конфигурации для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="5cd30-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="5cd30-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5cd30-124">-Name</span></span>
<span data-ttu-id="5cd30-125">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="5cd30-125">Webhook Name.</span></span>

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

### <span data-ttu-id="5cd30-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="5cd30-126">-Registry</span></span>
<span data-ttu-id="5cd30-127">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="5cd30-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="5cd30-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5cd30-128">-RegistryName</span></span>
<span data-ttu-id="5cd30-129">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="5cd30-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="5cd30-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd30-130">-ResourceGroupName</span></span>
<span data-ttu-id="5cd30-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5cd30-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="5cd30-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cd30-132">-ResourceId</span></span>
<span data-ttu-id="5cd30-133">ИД ресурса Webhook реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="5cd30-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="5cd30-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd30-134">CommonParameters</span></span>
<span data-ttu-id="5cd30-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd30-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd30-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cd30-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd30-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cd30-137">INPUTS</span></span>

### <span data-ttu-id="5cd30-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5cd30-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="5cd30-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5cd30-139">System.String</span></span>

## <span data-ttu-id="5cd30-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cd30-140">OUTPUTS</span></span>

### <span data-ttu-id="5cd30-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5cd30-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="5cd30-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cd30-142">NOTES</span></span>

## <span data-ttu-id="5cd30-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cd30-143">RELATED LINKS</span></span>

[<span data-ttu-id="5cd30-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5cd30-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="5cd30-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5cd30-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="5cd30-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5cd30-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="5cd30-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="5cd30-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)