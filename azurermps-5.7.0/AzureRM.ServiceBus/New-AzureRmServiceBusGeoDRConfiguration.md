---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: b90144fb94dcef874ce67168364aa65782084b4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567917"
---
# <span data-ttu-id="2a469-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a469-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="2a469-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a469-102">SYNOPSIS</span></span>
<span data-ttu-id="2a469-103">Создание нового псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="2a469-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a469-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a469-104">SYNTAX</span></span>

### <span data-ttu-id="2a469-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a469-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a469-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2a469-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a469-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a469-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a469-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a469-108">DESCRIPTION</span></span>
<span data-ttu-id="2a469-109">Командлет **New-AzureRmServiceBusGeoDRConfiguration** создает новый псевдоним (конфигурация аварийного восстановления).</span><span class="sxs-lookup"><span data-stu-id="2a469-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2a469-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a469-110">EXAMPLES</span></span>

### <span data-ttu-id="2a469-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a469-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="2a469-112">Создание псевдонима "SampleDRCongifName" с основным пространством имен "SampleNamespace_Primary" с дополнительным пространством имен "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="2a469-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="2a469-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a469-113">PARAMETERS</span></span>

### <span data-ttu-id="2a469-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="2a469-114">-AlternateName</span></span>
<span data-ttu-id="2a469-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="2a469-115">AlternateName</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a469-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a469-116">-AsJob</span></span>
<span data-ttu-id="2a469-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2a469-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a469-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a469-118">-DefaultProfile</span></span>
<span data-ttu-id="2a469-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a469-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a469-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a469-120">-InputObject</span></span>
<span data-ttu-id="2a469-121">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="2a469-121">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a469-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a469-122">-Name</span></span>
<span data-ttu-id="2a469-123">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="2a469-123">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a469-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2a469-124">-Namespace</span></span>
<span data-ttu-id="2a469-125">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="2a469-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a469-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="2a469-126">-PartnerNamespace</span></span>
<span data-ttu-id="2a469-127">PartnerNamespace конфигурации DR (идентификатор ARM для PartnerNamespace [дополнительное пространство имен])</span><span class="sxs-lookup"><span data-stu-id="2a469-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a469-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a469-128">-ResourceGroupName</span></span>
<span data-ttu-id="2a469-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2a469-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a469-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a469-130">-ResourceId</span></span>
<span data-ttu-id="2a469-131">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="2a469-131">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a469-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a469-132">-Confirm</span></span>
<span data-ttu-id="2a469-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a469-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a469-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a469-134">-WhatIf</span></span>
<span data-ttu-id="2a469-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a469-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a469-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a469-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a469-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a469-137">CommonParameters</span></span>
<span data-ttu-id="2a469-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a469-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2a469-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a469-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a469-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a469-140">INPUTS</span></span>

### <span data-ttu-id="2a469-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2a469-141">System.String</span></span>
<span data-ttu-id="2a469-142">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2a469-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="2a469-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a469-143">OUTPUTS</span></span>

### <span data-ttu-id="2a469-144">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2a469-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="2a469-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a469-145">NOTES</span></span>

## <span data-ttu-id="2a469-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a469-146">RELATED LINKS</span></span>
