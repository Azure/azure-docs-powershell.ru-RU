---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234767"
---
# <span data-ttu-id="e8429-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="e8429-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="e8429-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8429-102">SYNOPSIS</span></span>
<span data-ttu-id="e8429-103">Получает список адаптивных ресурсов аппаратной защиты сети в области расширенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8429-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="e8429-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8429-104">SYNTAX</span></span>

### <span data-ttu-id="e8429-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e8429-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="e8429-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8429-106">DESCRIPTION</span></span>
<span data-ttu-id="e8429-107">Адаптивные ограничения сети автоматически рассчитываются центром безопасности Azure с помощью этого командлета, чтобы получить список адаптивных ресурсов усиления защиты сети в области расширенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8429-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="e8429-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8429-108">EXAMPLES</span></span>

### <span data-ttu-id="e8429-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8429-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="e8429-110">Получает список адаптивных ресурсов аппаратной защиты сети в области расширенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8429-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="e8429-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e8429-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="e8429-112">Получение ресурса для одной адаптивной защиты сети</span><span class="sxs-lookup"><span data-stu-id="e8429-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="e8429-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8429-113">PARAMETERS</span></span>

### <span data-ttu-id="e8429-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8429-114">-DefaultProfile</span></span>
<span data-ttu-id="e8429-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8429-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8429-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8429-116">-ResourceGroupName</span></span>
<span data-ttu-id="e8429-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8429-117">Resource group name.</span></span>

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

### <span data-ttu-id="e8429-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e8429-118">-ResourceName</span></span>
<span data-ttu-id="e8429-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8429-119">Resource name.</span></span>

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

### <span data-ttu-id="e8429-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="e8429-120">-ResourceNamespace</span></span>
<span data-ttu-id="e8429-121">Пространство имен ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8429-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="e8429-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e8429-122">-ResourceType</span></span>
<span data-ttu-id="e8429-123">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8429-123">The type of the resource.</span></span>

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

### <span data-ttu-id="e8429-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="e8429-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="e8429-125">Имя адаптивного ресурса усиления защиты сети.</span><span class="sxs-lookup"><span data-stu-id="e8429-125">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="e8429-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8429-126">-SubscriptionId</span></span>
<span data-ttu-id="e8429-127">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="e8429-127">Azure subscription ID.</span></span>

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
### <span data-ttu-id="e8429-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8429-128">CommonParameters</span></span>
<span data-ttu-id="e8429-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8429-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8429-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8429-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8429-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8429-131">INPUTS</span></span>

### <span data-ttu-id="e8429-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e8429-132">System.String</span></span>

## <span data-ttu-id="e8429-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8429-133">OUTPUTS</span></span>

### <span data-ttu-id="e8429-134">Microsoft. Azure. Commands. Security. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="e8429-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="e8429-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8429-135">NOTES</span></span>

## <span data-ttu-id="e8429-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8429-136">RELATED LINKS</span></span>