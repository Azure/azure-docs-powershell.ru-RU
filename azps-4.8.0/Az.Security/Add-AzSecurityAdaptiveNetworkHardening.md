---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235376"
---
# <span data-ttu-id="342e7-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="342e7-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="342e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="342e7-102">SYNOPSIS</span></span>
<span data-ttu-id="342e7-103">Применяет заданные правила для NSG (ов), перечисленных в запросе</span><span class="sxs-lookup"><span data-stu-id="342e7-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="342e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="342e7-104">SYNTAX</span></span>

### <span data-ttu-id="342e7-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="342e7-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342e7-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="342e7-106">DESCRIPTION</span></span>
<span data-ttu-id="342e7-107">Адаптивные ограничения сети автоматически рассчитываются центром безопасности Azure, используйте этот командлет для принудительного применения заданных правил на NSG (-ов), перечисленных в запросе.</span><span class="sxs-lookup"><span data-stu-id="342e7-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="342e7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="342e7-108">EXAMPLES</span></span>

### <span data-ttu-id="342e7-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="342e7-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="342e7-110">Применяет заданные правила для NSG (ов), перечисленных в запросе</span><span class="sxs-lookup"><span data-stu-id="342e7-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="342e7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="342e7-111">PARAMETERS</span></span>

### <span data-ttu-id="342e7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342e7-112">-DefaultProfile</span></span>
<span data-ttu-id="342e7-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="342e7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="342e7-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="342e7-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="342e7-115">Имя адаптивного ресурса усиления защиты сети.</span><span class="sxs-lookup"><span data-stu-id="342e7-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342e7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="342e7-116">-ResourceGroupName</span></span>
<span data-ttu-id="342e7-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="342e7-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342e7-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="342e7-118">-ResourceName</span></span>
<span data-ttu-id="342e7-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="342e7-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342e7-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="342e7-120">-ResourceNamespace</span></span>
<span data-ttu-id="342e7-121">Пространство имен ресурса.</span><span class="sxs-lookup"><span data-stu-id="342e7-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342e7-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="342e7-122">-ResourceType</span></span>
<span data-ttu-id="342e7-123">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="342e7-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342e7-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="342e7-124">-SubscriptionId</span></span>
<span data-ttu-id="342e7-125">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="342e7-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342e7-126">-Правила</span><span class="sxs-lookup"><span data-stu-id="342e7-126">-Rules</span></span>
<span data-ttu-id="342e7-127">Правила для принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="342e7-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="342e7-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="342e7-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="342e7-129">Идентификаторы ресурсов Azure для эффективных сетевых групп безопасности, которые будут обновляться с учетом созданных правил безопасности из адаптивных правил защиты сети.</span><span class="sxs-lookup"><span data-stu-id="342e7-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342e7-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="342e7-130">-PassThru</span></span>
<span data-ttu-id="342e7-131">Возвращение значения, показывающего успешное выполнение или сбой</span><span class="sxs-lookup"><span data-stu-id="342e7-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="342e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342e7-132">CommonParameters</span></span>
<span data-ttu-id="342e7-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="342e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342e7-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="342e7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342e7-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="342e7-135">INPUTS</span></span>

### <span data-ttu-id="342e7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="342e7-136">System.String</span></span>

### <span data-ttu-id="342e7-137">Microsoft. Azure. Commands. SecurityCenter. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="342e7-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="342e7-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="342e7-138">OUTPUTS</span></span>

### <span data-ttu-id="342e7-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="342e7-139">System.Boolean</span></span>

## <span data-ttu-id="342e7-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="342e7-140">NOTES</span></span>

## <span data-ttu-id="342e7-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="342e7-141">RELATED LINKS</span></span>