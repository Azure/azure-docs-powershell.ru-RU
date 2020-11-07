---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4d3a6cef78a644f5448b2825b77ef1d2beabac63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721583"
---
# <span data-ttu-id="ea580-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea580-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="ea580-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea580-102">SYNOPSIS</span></span>
<span data-ttu-id="ea580-103">Запускает событие ping для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="ea580-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="ea580-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea580-104">SYNTAX</span></span>

### <span data-ttu-id="ea580-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea580-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea580-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea580-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea580-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea580-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea580-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea580-108">DESCRIPTION</span></span>
<span data-ttu-id="ea580-109">Командлет Test-AzContainerRegistryWebhook инициирует событие ping для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="ea580-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="ea580-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea580-110">EXAMPLES</span></span>

### <span data-ttu-id="ea580-111">Пример 1: запускает событие ping для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="ea580-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="ea580-112">Запускает событие ping для веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="ea580-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="ea580-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea580-113">PARAMETERS</span></span>

### <span data-ttu-id="ea580-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea580-114">-DefaultProfile</span></span>
<span data-ttu-id="ea580-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea580-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea580-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea580-116">-Name</span></span>
<span data-ttu-id="ea580-117">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="ea580-117">Webhook Name.</span></span>

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

### <span data-ttu-id="ea580-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ea580-118">-RegistryName</span></span>
<span data-ttu-id="ea580-119">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="ea580-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="ea580-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea580-120">-ResourceGroupName</span></span>
<span data-ttu-id="ea580-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea580-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea580-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea580-122">-ResourceId</span></span>
<span data-ttu-id="ea580-123">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="ea580-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="ea580-124">-Перехватчик</span><span class="sxs-lookup"><span data-stu-id="ea580-124">-Webhook</span></span>
<span data-ttu-id="ea580-125">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="ea580-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="ea580-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea580-126">CommonParameters</span></span>
<span data-ttu-id="ea580-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea580-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea580-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea580-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea580-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea580-129">INPUTS</span></span>

### <span data-ttu-id="ea580-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea580-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="ea580-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ea580-131">System.String</span></span>

## <span data-ttu-id="ea580-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea580-132">OUTPUTS</span></span>

### <span data-ttu-id="ea580-133">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="ea580-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="ea580-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea580-134">NOTES</span></span>

## <span data-ttu-id="ea580-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea580-135">RELATED LINKS</span></span>

[<span data-ttu-id="ea580-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea580-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ea580-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea580-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ea580-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea580-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ea580-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ea580-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)