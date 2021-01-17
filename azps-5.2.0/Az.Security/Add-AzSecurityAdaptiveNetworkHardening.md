---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396143"
---
# <span data-ttu-id="0dc39-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="0dc39-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="0dc39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dc39-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc39-103">Принудительное выполнение указанных правил для указанных в запросе NSG-запросов.</span><span class="sxs-lookup"><span data-stu-id="0dc39-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="0dc39-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0dc39-104">SYNTAX</span></span>

### <span data-ttu-id="0dc39-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0dc39-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dc39-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0dc39-106">DESCRIPTION</span></span>
<span data-ttu-id="0dc39-107">Адаптивные сетевые затенения автоматически вычисляются Центром безопасности Azure. Используйте этот cmdlet для применения заданных правил для NSG-кодов, перечисленных в запросе.</span><span class="sxs-lookup"><span data-stu-id="0dc39-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="0dc39-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0dc39-108">EXAMPLES</span></span>

### <span data-ttu-id="0dc39-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0dc39-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="0dc39-110">Принудительное выполнение указанных правил для указанных в запросе NSG-запросов.</span><span class="sxs-lookup"><span data-stu-id="0dc39-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="0dc39-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dc39-111">PARAMETERS</span></span>

### <span data-ttu-id="0dc39-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc39-112">-DefaultProfile</span></span>
<span data-ttu-id="0dc39-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc39-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dc39-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="0dc39-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="0dc39-115">Имя ресурса адаптивного закаленного сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="0dc39-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="0dc39-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc39-116">-ResourceGroupName</span></span>
<span data-ttu-id="0dc39-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0dc39-117">Resource group name.</span></span>

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

### <span data-ttu-id="0dc39-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0dc39-118">-ResourceName</span></span>
<span data-ttu-id="0dc39-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="0dc39-119">Resource name.</span></span>

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

### <span data-ttu-id="0dc39-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="0dc39-120">-ResourceNamespace</span></span>
<span data-ttu-id="0dc39-121">Пространство имен ресурса.</span><span class="sxs-lookup"><span data-stu-id="0dc39-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="0dc39-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0dc39-122">-ResourceType</span></span>
<span data-ttu-id="0dc39-123">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="0dc39-123">The type of the resource.</span></span>

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

### <span data-ttu-id="0dc39-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0dc39-124">-SubscriptionId</span></span>
<span data-ttu-id="0dc39-125">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc39-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="0dc39-126">-Rules</span><span class="sxs-lookup"><span data-stu-id="0dc39-126">-Rules</span></span>
<span data-ttu-id="0dc39-127">Правила, которые необходимо применять.</span><span class="sxs-lookup"><span data-stu-id="0dc39-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="0dc39-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="0dc39-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="0dc39-129">ИД ресурсов Azure для эффективных групп безопасности сети, которые будут обновлены с помощью созданных правил безопасности на ряду правил адаптивного затенения сети.</span><span class="sxs-lookup"><span data-stu-id="0dc39-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="0dc39-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dc39-130">-PassThru</span></span>
<span data-ttu-id="0dc39-131">Возвращает значение, указывающее на успех или неудачу.</span><span class="sxs-lookup"><span data-stu-id="0dc39-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="0dc39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc39-132">CommonParameters</span></span>
<span data-ttu-id="0dc39-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc39-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc39-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc39-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0dc39-135">INPUTS</span></span>

### <span data-ttu-id="0dc39-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0dc39-136">System.String</span></span>

### <span data-ttu-id="0dc39-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="0dc39-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="0dc39-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0dc39-138">OUTPUTS</span></span>

### <span data-ttu-id="0dc39-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0dc39-139">System.Boolean</span></span>

## <span data-ttu-id="0dc39-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0dc39-140">NOTES</span></span>

## <span data-ttu-id="0dc39-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0dc39-141">RELATED LINKS</span></span>