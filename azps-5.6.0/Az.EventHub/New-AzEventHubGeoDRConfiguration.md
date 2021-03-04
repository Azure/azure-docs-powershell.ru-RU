---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: d545883f1c4ce51d4e3efce15787a2e0fa144378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957107"
---
# <span data-ttu-id="3029f-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="3029f-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="3029f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3029f-102">SYNOPSIS</span></span>
<span data-ttu-id="3029f-103">Создание нового псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="3029f-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="3029f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3029f-104">SYNTAX</span></span>

### <span data-ttu-id="3029f-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3029f-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3029f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3029f-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3029f-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3029f-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3029f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3029f-108">DESCRIPTION</span></span>
<span data-ttu-id="3029f-109">Новый псевдоним (конфигурация аварийного восстановления) для **New-AzEventHubGeoDRConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3029f-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="3029f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3029f-110">EXAMPLES</span></span>

### <span data-ttu-id="3029f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3029f-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="3029f-112">Создание псевдонима SampleDRConfigName с основным пространством имен "SampleNamespace_Primary" и дополнительным пространством имен "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="3029f-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="3029f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3029f-113">PARAMETERS</span></span>

### <span data-ttu-id="3029f-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="3029f-114">-AlternateName</span></span>
<span data-ttu-id="3029f-115">Имя, требуемая, если имя конфигурации DR такое же, как в основном пространстве имен</span><span class="sxs-lookup"><span data-stu-id="3029f-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="3029f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3029f-116">-AsJob</span></span>
<span data-ttu-id="3029f-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3029f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3029f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3029f-118">-DefaultProfile</span></span>
<span data-ttu-id="3029f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3029f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3029f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3029f-120">-InputObject</span></span>
<span data-ttu-id="3029f-121">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="3029f-121">Namespace Object</span></span>

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

### <span data-ttu-id="3029f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3029f-122">-Name</span></span>
<span data-ttu-id="3029f-123">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="3029f-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="3029f-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3029f-124">-Namespace</span></span>
<span data-ttu-id="3029f-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3029f-125">Namespace Name</span></span>

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

### <span data-ttu-id="3029f-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="3029f-126">-PartnerNamespace</span></span>
<span data-ttu-id="3029f-127">DR Configuration PartnerNamespace ARM ID</span><span class="sxs-lookup"><span data-stu-id="3029f-127">DR Configuration PartnerNamespace ARM ID</span></span>

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

### <span data-ttu-id="3029f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3029f-128">-ResourceGroupName</span></span>
<span data-ttu-id="3029f-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3029f-129">Resource Group Name</span></span>

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

### <span data-ttu-id="3029f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3029f-130">-ResourceId</span></span>
<span data-ttu-id="3029f-131">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="3029f-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="3029f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3029f-132">-Confirm</span></span>
<span data-ttu-id="3029f-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3029f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3029f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3029f-134">-WhatIf</span></span>
<span data-ttu-id="3029f-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3029f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3029f-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3029f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3029f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3029f-137">CommonParameters</span></span>
<span data-ttu-id="3029f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3029f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3029f-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3029f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3029f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3029f-140">INPUTS</span></span>

### <span data-ttu-id="3029f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3029f-141">System.String</span></span>

### <span data-ttu-id="3029f-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3029f-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3029f-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3029f-143">OUTPUTS</span></span>

### <span data-ttu-id="3029f-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3029f-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="3029f-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3029f-145">NOTES</span></span>

## <span data-ttu-id="3029f-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3029f-146">RELATED LINKS</span></span>
