---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 4f20f177b172ab9b5372de6b95d821202e991000
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561876"
---
# <span data-ttu-id="0602a-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0602a-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="0602a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0602a-102">SYNOPSIS</span></span>
<span data-ttu-id="0602a-103">Получает веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="0602a-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0602a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0602a-104">SYNTAX</span></span>

### <span data-ttu-id="0602a-105">ListWebhookByNameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0602a-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0602a-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0602a-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0602a-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0602a-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0602a-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0602a-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0602a-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0602a-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0602a-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0602a-110">DESCRIPTION</span></span>
<span data-ttu-id="0602a-111">Командлет Get-AzureRmContainerRegistryWebhook получает указанный веб-перехватчик реестра контейнера или все веб-перехватчики реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="0602a-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="0602a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0602a-112">EXAMPLES</span></span>

### <span data-ttu-id="0602a-113">Пример 1: получение указанного веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="0602a-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="0602a-114">Получение указанного веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="0602a-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="0602a-115">Пример 2: получение всех веб-перехватчиков реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="0602a-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="0602a-116">Получение всех веб-перехватчиков в реестре контейнера</span><span class="sxs-lookup"><span data-stu-id="0602a-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="0602a-117">Пример 3: получение указанного веб-перехватчика реестра контейнера с подробными сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="0602a-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="0602a-118">Получение указанного веб-перехватчика реестра контейнера с подробными сведениями о конфигурации</span><span class="sxs-lookup"><span data-stu-id="0602a-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="0602a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0602a-119">PARAMETERS</span></span>

### <span data-ttu-id="0602a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0602a-120">-DefaultProfile</span></span>
<span data-ttu-id="0602a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0602a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0602a-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0602a-122">-IncludeConfiguration</span></span>
<span data-ttu-id="0602a-123">Получение сведений о конфигурации для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="0602a-123">Get the configuration information for a webhook.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0602a-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0602a-124">-Name</span></span>
<span data-ttu-id="0602a-125">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="0602a-125">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0602a-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="0602a-126">-Registry</span></span>
<span data-ttu-id="0602a-127">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="0602a-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0602a-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0602a-128">-RegistryName</span></span>
<span data-ttu-id="0602a-129">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="0602a-129">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0602a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0602a-130">-ResourceGroupName</span></span>
<span data-ttu-id="0602a-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0602a-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0602a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0602a-132">-ResourceId</span></span>
<span data-ttu-id="0602a-133">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="0602a-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="0602a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0602a-134">CommonParameters</span></span>
<span data-ttu-id="0602a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0602a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0602a-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0602a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0602a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0602a-137">INPUTS</span></span>

### <span data-ttu-id="0602a-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0602a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="0602a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0602a-139">System.String</span></span>

## <span data-ttu-id="0602a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0602a-140">OUTPUTS</span></span>

### <span data-ttu-id="0602a-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0602a-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="0602a-142">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook, Microsoft. Azure. Commands = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0602a-142">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0602a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0602a-143">NOTES</span></span>

## <span data-ttu-id="0602a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0602a-144">RELATED LINKS</span></span>

[<span data-ttu-id="0602a-145">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0602a-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0602a-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0602a-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0602a-147">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0602a-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="0602a-148">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0602a-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
