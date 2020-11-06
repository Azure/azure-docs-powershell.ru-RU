---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: e2ac72ba5d563b4be902d424ad30c19b40bff9d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558415"
---
# <span data-ttu-id="2f601-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f601-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="2f601-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f601-102">SYNOPSIS</span></span>
<span data-ttu-id="2f601-103">Создание нового псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="2f601-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f601-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f601-104">SYNTAX</span></span>

### <span data-ttu-id="2f601-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f601-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f601-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2f601-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f601-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f601-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f601-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f601-108">DESCRIPTION</span></span>
<span data-ttu-id="2f601-109">Командлет **New-AzureRmEventHubGeoDRConfiguration** создает новый псевдоним (конфигурация аварийного восстановления).</span><span class="sxs-lookup"><span data-stu-id="2f601-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2f601-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f601-110">EXAMPLES</span></span>

### <span data-ttu-id="2f601-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f601-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="2f601-112">Создание псевдонима "SampleDRCongifName" с основным пространством имен "SampleNamespace_Primary" с дополнительным пространством имен "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="2f601-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="2f601-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f601-113">PARAMETERS</span></span>

### <span data-ttu-id="2f601-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="2f601-114">-AlternateName</span></span>
<span data-ttu-id="2f601-115">AlternateName требуется в том случае, если имя конфигурации DR совпадает с основным пространством имен</span><span class="sxs-lookup"><span data-stu-id="2f601-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f601-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f601-116">-AsJob</span></span>
<span data-ttu-id="2f601-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2f601-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f601-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f601-118">-DefaultProfile</span></span>
<span data-ttu-id="2f601-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f601-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f601-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f601-120">-InputObject</span></span>
<span data-ttu-id="2f601-121">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="2f601-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f601-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f601-122">-Name</span></span>
<span data-ttu-id="2f601-123">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="2f601-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f601-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2f601-124">-Namespace</span></span>
<span data-ttu-id="2f601-125">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="2f601-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f601-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="2f601-126">-PartnerNamespace</span></span>
<span data-ttu-id="2f601-127">Настройка DR PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="2f601-127">DR Configuration PartnerNamespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f601-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f601-128">-ResourceGroupName</span></span>
<span data-ttu-id="2f601-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2f601-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f601-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f601-130">-ResourceId</span></span>
<span data-ttu-id="2f601-131">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="2f601-131">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f601-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f601-132">-Confirm</span></span>
<span data-ttu-id="2f601-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f601-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f601-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f601-134">-WhatIf</span></span>
<span data-ttu-id="2f601-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f601-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f601-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f601-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f601-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f601-137">CommonParameters</span></span>
<span data-ttu-id="2f601-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f601-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f601-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f601-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f601-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f601-140">INPUTS</span></span>

### <span data-ttu-id="2f601-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2f601-141">System.String</span></span>

### <span data-ttu-id="2f601-142">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2f601-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="2f601-143">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f601-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2f601-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f601-144">OUTPUTS</span></span>

### <span data-ttu-id="2f601-145">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2f601-145">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="2f601-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f601-146">NOTES</span></span>

## <span data-ttu-id="2f601-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f601-147">RELATED LINKS</span></span>
