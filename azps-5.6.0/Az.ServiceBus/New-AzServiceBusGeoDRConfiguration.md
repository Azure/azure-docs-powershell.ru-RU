---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 02335868ca9984d4da57be905b9600b81333b484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956627"
---
# <span data-ttu-id="30590-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="30590-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="30590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30590-102">SYNOPSIS</span></span>
<span data-ttu-id="30590-103">Создание нового псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="30590-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="30590-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30590-104">SYNTAX</span></span>

### <span data-ttu-id="30590-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30590-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30590-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="30590-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30590-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30590-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30590-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30590-108">DESCRIPTION</span></span>
<span data-ttu-id="30590-109">Новый псевдоним (конфигурация аварийного восстановления) для **New-AzServiceBusGeoDRConfiguration**</span><span class="sxs-lookup"><span data-stu-id="30590-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="30590-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30590-110">EXAMPLES</span></span>

### <span data-ttu-id="30590-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30590-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="30590-112">Создание псевдонима SampleDRConfigName с основным пространством имен "SampleNamespace_Primary" и дополнительным пространством имен "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="30590-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="30590-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30590-113">PARAMETERS</span></span>

### <span data-ttu-id="30590-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="30590-114">-AlternateName</span></span>
<span data-ttu-id="30590-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="30590-115">AlternateName</span></span>

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

### <span data-ttu-id="30590-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30590-116">-AsJob</span></span>
<span data-ttu-id="30590-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="30590-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30590-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30590-118">-DefaultProfile</span></span>
<span data-ttu-id="30590-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30590-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30590-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30590-120">-InputObject</span></span>
<span data-ttu-id="30590-121">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="30590-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30590-122">-Name</span><span class="sxs-lookup"><span data-stu-id="30590-122">-Name</span></span>
<span data-ttu-id="30590-123">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="30590-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="30590-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="30590-124">-Namespace</span></span>
<span data-ttu-id="30590-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="30590-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30590-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="30590-126">-PartnerNamespace</span></span>
<span data-ttu-id="30590-127">DR Configuration PartnerNamespace (ARM ИД PartnerNamespace [дополнительное пространство имен])</span><span class="sxs-lookup"><span data-stu-id="30590-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="30590-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30590-128">-ResourceGroupName</span></span>
<span data-ttu-id="30590-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="30590-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30590-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30590-130">-ResourceId</span></span>
<span data-ttu-id="30590-131">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="30590-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="30590-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30590-132">-Confirm</span></span>
<span data-ttu-id="30590-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30590-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30590-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30590-134">-WhatIf</span></span>
<span data-ttu-id="30590-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30590-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30590-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30590-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30590-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30590-137">CommonParameters</span></span>
<span data-ttu-id="30590-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30590-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30590-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30590-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30590-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30590-140">INPUTS</span></span>

### <span data-ttu-id="30590-141">System.String</span><span class="sxs-lookup"><span data-stu-id="30590-141">System.String</span></span>

### <span data-ttu-id="30590-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="30590-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="30590-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30590-143">OUTPUTS</span></span>

### <span data-ttu-id="30590-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="30590-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="30590-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30590-145">NOTES</span></span>

## <span data-ttu-id="30590-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30590-146">RELATED LINKS</span></span>
