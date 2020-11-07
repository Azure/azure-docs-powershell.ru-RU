---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 92bea9777d29a3cdf13007e743b1e7d929c8df40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903837"
---
# <span data-ttu-id="d8daa-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8daa-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="d8daa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8daa-102">SYNOPSIS</span></span>
<span data-ttu-id="d8daa-103">Создание нового псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="d8daa-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d8daa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8daa-104">SYNTAX</span></span>

### <span data-ttu-id="d8daa-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8daa-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8daa-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d8daa-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8daa-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8daa-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8daa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8daa-108">DESCRIPTION</span></span>
<span data-ttu-id="d8daa-109">Командлет **New-AzServiceBusGeoDRConfiguration** создает новый псевдоним (конфигурация аварийного восстановления).</span><span class="sxs-lookup"><span data-stu-id="d8daa-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d8daa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8daa-110">EXAMPLES</span></span>

### <span data-ttu-id="d8daa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8daa-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="d8daa-112">Создание псевдонима "SampleDRConfigName" с основным пространством имен "SampleNamespace_Primary" с дополнительным пространством имен "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="d8daa-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="d8daa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8daa-113">PARAMETERS</span></span>

### <span data-ttu-id="d8daa-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="d8daa-114">-AlternateName</span></span>
<span data-ttu-id="d8daa-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="d8daa-115">AlternateName</span></span>

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

### <span data-ttu-id="d8daa-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8daa-116">-AsJob</span></span>
<span data-ttu-id="d8daa-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d8daa-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8daa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8daa-118">-DefaultProfile</span></span>
<span data-ttu-id="d8daa-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8daa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8daa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8daa-120">-InputObject</span></span>
<span data-ttu-id="d8daa-121">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="d8daa-121">Namespace Object</span></span>

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

### <span data-ttu-id="d8daa-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8daa-122">-Name</span></span>
<span data-ttu-id="d8daa-123">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="d8daa-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="d8daa-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d8daa-124">-Namespace</span></span>
<span data-ttu-id="d8daa-125">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="d8daa-125">Namespace Name</span></span>

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

### <span data-ttu-id="d8daa-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="d8daa-126">-PartnerNamespace</span></span>
<span data-ttu-id="d8daa-127">PartnerNamespace конфигурации DR (идентификатор ARM для PartnerNamespace [дополнительное пространство имен])</span><span class="sxs-lookup"><span data-stu-id="d8daa-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="d8daa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8daa-128">-ResourceGroupName</span></span>
<span data-ttu-id="d8daa-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d8daa-129">Resource Group Name</span></span>

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

### <span data-ttu-id="d8daa-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8daa-130">-ResourceId</span></span>
<span data-ttu-id="d8daa-131">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="d8daa-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="d8daa-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8daa-132">-Confirm</span></span>
<span data-ttu-id="d8daa-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8daa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8daa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8daa-134">-WhatIf</span></span>
<span data-ttu-id="d8daa-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8daa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8daa-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8daa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8daa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8daa-137">CommonParameters</span></span>
<span data-ttu-id="d8daa-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8daa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8daa-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8daa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8daa-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8daa-140">INPUTS</span></span>

### <span data-ttu-id="d8daa-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d8daa-141">System.String</span></span>

### <span data-ttu-id="d8daa-142">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d8daa-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d8daa-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8daa-143">OUTPUTS</span></span>

### <span data-ttu-id="d8daa-144">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d8daa-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="d8daa-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8daa-145">NOTES</span></span>

## <span data-ttu-id="d8daa-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8daa-146">RELATED LINKS</span></span>
