---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: fef6f1615bb2e3dd9d3bb19738ea6cef393235aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244028"
---
# <span data-ttu-id="adfd0-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="adfd0-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="adfd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="adfd0-102">SYNOPSIS</span></span>
<span data-ttu-id="adfd0-103">Получает список префиксов службы пиринга для подписки.</span><span class="sxs-lookup"><span data-stu-id="adfd0-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="adfd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="adfd0-104">SYNTAX</span></span>

### <span data-ttu-id="adfd0-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adfd0-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adfd0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="adfd0-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adfd0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="adfd0-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adfd0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adfd0-108">DESCRIPTION</span></span>
<span data-ttu-id="adfd0-109">Список префиксов службы пиринга для объектов службы пиринга</span><span class="sxs-lookup"><span data-stu-id="adfd0-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="adfd0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="adfd0-110">EXAMPLES</span></span>

### <span data-ttu-id="adfd0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="adfd0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="adfd0-112">Получает префиксы для службы пиринга на основе команд трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="adfd0-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="adfd0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="adfd0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="adfd0-114">Получает определенный префикс для службы пиринга по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="adfd0-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="adfd0-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="adfd0-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="adfd0-116">Получает определенный префикс для службы пиринга по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="adfd0-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="adfd0-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="adfd0-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="adfd0-118">Возвращает определенный префикс для службы пиринга с развернутыми атрибутами.</span><span class="sxs-lookup"><span data-stu-id="adfd0-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="adfd0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="adfd0-119">PARAMETERS</span></span>

### <span data-ttu-id="adfd0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adfd0-120">-DefaultProfile</span></span>
<span data-ttu-id="adfd0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adfd0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adfd0-122">-Expand</span><span class="sxs-lookup"><span data-stu-id="adfd0-122">-Expand</span></span>
<span data-ttu-id="adfd0-123">Просмотр событий для префикса службы пиринга</span><span class="sxs-lookup"><span data-stu-id="adfd0-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="adfd0-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="adfd0-124">-Name</span></span>
<span data-ttu-id="adfd0-125">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="adfd0-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfd0-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="adfd0-126">-PeeringServiceName</span></span>
<span data-ttu-id="adfd0-127">Имя службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="adfd0-127">The peering service name.</span></span> <span data-ttu-id="adfd0-128">Используйте New-AzPeeringService командлет для новой службы пиринга или Get-AzPeeringService для списка.</span><span class="sxs-lookup"><span data-stu-id="adfd0-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfd0-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="adfd0-129">-PeeringServiceObject</span></span>
<span data-ttu-id="adfd0-130">Использование Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="adfd0-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adfd0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adfd0-131">-ResourceGroupName</span></span>
<span data-ttu-id="adfd0-132">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="adfd0-132">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfd0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adfd0-133">-ResourceId</span></span>
<span data-ttu-id="adfd0-134">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="adfd0-134">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adfd0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adfd0-135">CommonParameters</span></span>
<span data-ttu-id="adfd0-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="adfd0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adfd0-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adfd0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adfd0-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="adfd0-138">INPUTS</span></span>

### <span data-ttu-id="adfd0-139">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringService)</span><span class="sxs-lookup"><span data-stu-id="adfd0-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="adfd0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="adfd0-140">System.String</span></span>

## <span data-ttu-id="adfd0-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="adfd0-141">OUTPUTS</span></span>

### <span data-ttu-id="adfd0-142">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringServicePrefix)</span><span class="sxs-lookup"><span data-stu-id="adfd0-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="adfd0-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="adfd0-143">NOTES</span></span>

## <span data-ttu-id="adfd0-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adfd0-144">RELATED LINKS</span></span>