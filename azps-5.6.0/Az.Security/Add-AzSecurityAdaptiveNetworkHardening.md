---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: e0e634a4947953f65c3fd68c9cc3e40dfca17fd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972531"
---
# <span data-ttu-id="327de-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="327de-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="327de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="327de-102">SYNOPSIS</span></span>
<span data-ttu-id="327de-103">Принудительное выполнение указанных правил для указанных в запросе NSG-запросов.</span><span class="sxs-lookup"><span data-stu-id="327de-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="327de-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="327de-104">SYNTAX</span></span>

### <span data-ttu-id="327de-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="327de-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="327de-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="327de-106">DESCRIPTION</span></span>
<span data-ttu-id="327de-107">Адаптивные сетевые затенения автоматически вычисляются Центром безопасности Azure. Используйте этот cmdlet для применения заданных правил для NSG-кодов, перечисленных в запросе.</span><span class="sxs-lookup"><span data-stu-id="327de-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="327de-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="327de-108">EXAMPLES</span></span>

### <span data-ttu-id="327de-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="327de-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="327de-110">Принудительное выполнение указанных правил для указанных в запросе NSG-запросов.</span><span class="sxs-lookup"><span data-stu-id="327de-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="327de-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="327de-111">PARAMETERS</span></span>

### <span data-ttu-id="327de-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327de-112">-DefaultProfile</span></span>
<span data-ttu-id="327de-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="327de-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="327de-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="327de-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="327de-115">Имя ресурса, который закален с адаптивной сетью.</span><span class="sxs-lookup"><span data-stu-id="327de-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="327de-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="327de-116">-ResourceGroupName</span></span>
<span data-ttu-id="327de-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="327de-117">Resource group name.</span></span>

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

### <span data-ttu-id="327de-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="327de-118">-ResourceName</span></span>
<span data-ttu-id="327de-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="327de-119">Resource name.</span></span>

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

### <span data-ttu-id="327de-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="327de-120">-ResourceNamespace</span></span>
<span data-ttu-id="327de-121">Пространство имен ресурса.</span><span class="sxs-lookup"><span data-stu-id="327de-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="327de-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="327de-122">-ResourceType</span></span>
<span data-ttu-id="327de-123">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="327de-123">The type of the resource.</span></span>

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

### <span data-ttu-id="327de-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="327de-124">-SubscriptionId</span></span>
<span data-ttu-id="327de-125">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="327de-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="327de-126">-Rules</span><span class="sxs-lookup"><span data-stu-id="327de-126">-Rules</span></span>
<span data-ttu-id="327de-127">Правила, которые необходимо применять.</span><span class="sxs-lookup"><span data-stu-id="327de-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="327de-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="327de-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="327de-129">ИД ресурсов Azure для эффективных групп безопасности сети, которые будут обновлены с помощью созданных правил безопасности на ряду правил адаптивного затенения сети.</span><span class="sxs-lookup"><span data-stu-id="327de-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="327de-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="327de-130">-PassThru</span></span>
<span data-ttu-id="327de-131">Возвращает значение, указывающее на успех или неудачу.</span><span class="sxs-lookup"><span data-stu-id="327de-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="327de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327de-132">CommonParameters</span></span>
<span data-ttu-id="327de-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="327de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327de-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="327de-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327de-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="327de-135">INPUTS</span></span>

### <span data-ttu-id="327de-136">System.String</span><span class="sxs-lookup"><span data-stu-id="327de-136">System.String</span></span>

### <span data-ttu-id="327de-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="327de-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="327de-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="327de-138">OUTPUTS</span></span>

### <span data-ttu-id="327de-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="327de-139">System.Boolean</span></span>

## <span data-ttu-id="327de-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="327de-140">NOTES</span></span>

## <span data-ttu-id="327de-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="327de-141">RELATED LINKS</span></span>