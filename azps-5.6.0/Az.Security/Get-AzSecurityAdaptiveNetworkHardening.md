---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: 87b53048ede0a5b2484da18ccd0a2f6a531aa92b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008568"
---
# <span data-ttu-id="4b454-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="4b454-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="4b454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b454-102">SYNOPSIS</span></span>
<span data-ttu-id="4b454-103">Возвращает список ресурсов, имеющих адаптивные сетевые возможности, в области действия расширенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b454-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="4b454-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b454-104">SYNTAX</span></span>

### <span data-ttu-id="4b454-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="4b454-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="4b454-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b454-106">DESCRIPTION</span></span>
<span data-ttu-id="4b454-107">Центр безопасности Azure автоматически вычисляет адаптивные сетевые затенения. Используйте этот cmdlet, чтобы получить список ресурсов адаптивной сетевых заявок в области расширенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b454-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="4b454-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b454-108">EXAMPLES</span></span>

### <span data-ttu-id="4b454-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b454-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="4b454-110">Возвращает список ресурсов, имеющих адаптивные сетевые возможности, в области действия расширенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b454-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="4b454-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4b454-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="4b454-112">Получить один ресурс с адаптивными сетевыми затенениями</span><span class="sxs-lookup"><span data-stu-id="4b454-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="4b454-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b454-113">PARAMETERS</span></span>

### <span data-ttu-id="4b454-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b454-114">-DefaultProfile</span></span>
<span data-ttu-id="4b454-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b454-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b454-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b454-116">-ResourceGroupName</span></span>
<span data-ttu-id="4b454-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b454-117">Resource group name.</span></span>

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

### <span data-ttu-id="4b454-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4b454-118">-ResourceName</span></span>
<span data-ttu-id="4b454-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b454-119">Resource name.</span></span>

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

### <span data-ttu-id="4b454-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="4b454-120">-ResourceNamespace</span></span>
<span data-ttu-id="4b454-121">Пространство имен ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b454-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="4b454-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4b454-122">-ResourceType</span></span>
<span data-ttu-id="4b454-123">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b454-123">The type of the resource.</span></span>

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

### <span data-ttu-id="4b454-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="4b454-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="4b454-125">Имя ресурса адаптивного закаленного сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b454-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b454-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b454-126">-SubscriptionId</span></span>
<span data-ttu-id="4b454-127">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="4b454-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="4b454-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b454-128">CommonParameters</span></span>
<span data-ttu-id="4b454-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b454-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b454-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b454-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b454-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b454-131">INPUTS</span></span>

### <span data-ttu-id="4b454-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4b454-132">System.String</span></span>

## <span data-ttu-id="4b454-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b454-133">OUTPUTS</span></span>

### <span data-ttu-id="4b454-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="4b454-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="4b454-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b454-135">NOTES</span></span>

## <span data-ttu-id="4b454-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b454-136">RELATED LINKS</span></span>