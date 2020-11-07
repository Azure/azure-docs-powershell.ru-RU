---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a5894a411f4ffb5b3bde28db68961d321584e1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732314"
---
# <span data-ttu-id="501d7-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="501d7-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="501d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="501d7-102">SYNOPSIS</span></span>
<span data-ttu-id="501d7-103">Запускает событие ping для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="501d7-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="501d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="501d7-104">SYNTAX</span></span>

### <span data-ttu-id="501d7-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="501d7-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="501d7-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="501d7-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="501d7-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="501d7-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="501d7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="501d7-108">DESCRIPTION</span></span>
<span data-ttu-id="501d7-109">Командлет Test-AzureRmContainerRegistryWebhook инициирует событие ping для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="501d7-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="501d7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="501d7-110">EXAMPLES</span></span>

### <span data-ttu-id="501d7-111">Пример 1: запускает событие ping для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="501d7-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="501d7-112">Запускает событие ping для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="501d7-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="501d7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="501d7-113">PARAMETERS</span></span>

### <span data-ttu-id="501d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="501d7-114">-DefaultProfile</span></span>
<span data-ttu-id="501d7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="501d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="501d7-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="501d7-116">-Name</span></span>
<span data-ttu-id="501d7-117">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="501d7-117">Webhook Name.</span></span>

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

### <span data-ttu-id="501d7-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="501d7-118">-RegistryName</span></span>
<span data-ttu-id="501d7-119">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="501d7-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="501d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="501d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="501d7-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="501d7-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="501d7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="501d7-122">-ResourceId</span></span>
<span data-ttu-id="501d7-123">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="501d7-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="501d7-124">-Перехватчик</span><span class="sxs-lookup"><span data-stu-id="501d7-124">-Webhook</span></span>
<span data-ttu-id="501d7-125">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="501d7-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="501d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="501d7-126">CommonParameters</span></span>
<span data-ttu-id="501d7-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="501d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="501d7-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="501d7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="501d7-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="501d7-129">INPUTS</span></span>

### <span data-ttu-id="501d7-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="501d7-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="501d7-131">Параметры: веб-перехватчик (ByValue)</span><span class="sxs-lookup"><span data-stu-id="501d7-131">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="501d7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="501d7-132">System.String</span></span>

## <span data-ttu-id="501d7-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="501d7-133">OUTPUTS</span></span>

### <span data-ttu-id="501d7-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="501d7-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="501d7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="501d7-135">NOTES</span></span>

## <span data-ttu-id="501d7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="501d7-136">RELATED LINKS</span></span>

[<span data-ttu-id="501d7-137">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="501d7-137">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="501d7-138">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="501d7-138">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="501d7-139">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="501d7-139">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="501d7-140">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="501d7-140">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
