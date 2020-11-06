---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: d2fee7d402ddf25a2bcc4b32528e31e44f500618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568211"
---
# <span data-ttu-id="41728-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="41728-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="41728-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41728-102">SYNOPSIS</span></span>
<span data-ttu-id="41728-103">Получает веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="41728-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41728-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41728-104">SYNTAX</span></span>

### <span data-ttu-id="41728-105">ListWebhookByNameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41728-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41728-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="41728-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41728-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41728-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41728-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41728-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41728-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41728-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41728-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41728-110">DESCRIPTION</span></span>
<span data-ttu-id="41728-111">Командлет Get-AzureRmContainerRegistryWebhook получает указанный веб-перехватчик реестра контейнера или все веб-перехватчики реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="41728-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="41728-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41728-112">EXAMPLES</span></span>

### <span data-ttu-id="41728-113">Пример 1: получение указанного веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="41728-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="41728-114">Получение указанного веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="41728-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="41728-115">Пример 2: получение всех веб-перехватчиков реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="41728-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="41728-116">Получение всех веб-перехватчиков в реестре контейнера</span><span class="sxs-lookup"><span data-stu-id="41728-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="41728-117">Пример 3: получение указанного веб-перехватчика реестра контейнера с подробными сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="41728-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="41728-118">Получение указанного веб-перехватчика реестра контейнера с подробными сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="41728-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="41728-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41728-119">PARAMETERS</span></span>

### <span data-ttu-id="41728-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41728-120">-DefaultProfile</span></span>
<span data-ttu-id="41728-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41728-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41728-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="41728-122">-IncludeConfiguration</span></span>
<span data-ttu-id="41728-123">Получение сведений о конфигурации для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="41728-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="41728-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41728-124">-Name</span></span>
<span data-ttu-id="41728-125">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="41728-125">Webhook Name.</span></span>

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

### <span data-ttu-id="41728-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="41728-126">-Registry</span></span>
<span data-ttu-id="41728-127">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="41728-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="41728-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="41728-128">-RegistryName</span></span>
<span data-ttu-id="41728-129">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="41728-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="41728-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41728-130">-ResourceGroupName</span></span>
<span data-ttu-id="41728-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41728-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="41728-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41728-132">-ResourceId</span></span>
<span data-ttu-id="41728-133">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="41728-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="41728-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41728-134">CommonParameters</span></span>
<span data-ttu-id="41728-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41728-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41728-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41728-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41728-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41728-137">INPUTS</span></span>

### <span data-ttu-id="41728-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="41728-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="41728-139">Параметры: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41728-139">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="41728-140">System. String</span><span class="sxs-lookup"><span data-stu-id="41728-140">System.String</span></span>

## <span data-ttu-id="41728-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41728-141">OUTPUTS</span></span>

### <span data-ttu-id="41728-142">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="41728-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="41728-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="41728-143">NOTES</span></span>

## <span data-ttu-id="41728-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41728-144">RELATED LINKS</span></span>

[<span data-ttu-id="41728-145">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="41728-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="41728-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="41728-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="41728-147">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="41728-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="41728-148">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="41728-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
