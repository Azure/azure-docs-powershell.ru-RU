---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246380"
---
# <span data-ttu-id="5f16c-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="5f16c-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="5f16c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f16c-102">SYNOPSIS</span></span>
<span data-ttu-id="5f16c-103">Возвращает или перечисляет зарегистрированный префикс для одноранговых элементов.</span><span class="sxs-lookup"><span data-stu-id="5f16c-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="5f16c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f16c-104">SYNTAX</span></span>

### <span data-ttu-id="5f16c-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f16c-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f16c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5f16c-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f16c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f16c-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f16c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f16c-108">DESCRIPTION</span></span>
<span data-ttu-id="5f16c-109">Возвращает или перечисляет зарегистрированный префикс для одноранговых элементов.</span><span class="sxs-lookup"><span data-stu-id="5f16c-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="5f16c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f16c-110">EXAMPLES</span></span>

### <span data-ttu-id="5f16c-111">Список зарегистрированных ASNs для пиринга</span><span class="sxs-lookup"><span data-stu-id="5f16c-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="5f16c-112">Список зарегистрированных ASN.</span><span class="sxs-lookup"><span data-stu-id="5f16c-112">Lists registered asn.</span></span>

### <span data-ttu-id="5f16c-113">Получает регистрацию ASN для пиринга по имени.</span><span class="sxs-lookup"><span data-stu-id="5f16c-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="5f16c-114">Получает регистрацию ASN однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="5f16c-114">Gets registered peering asn.</span></span>

<span data-ttu-id="5f16c-115">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="5f16c-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="5f16c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f16c-116">PARAMETERS</span></span>

### <span data-ttu-id="5f16c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f16c-117">-DefaultProfile</span></span>
<span data-ttu-id="5f16c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f16c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f16c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f16c-119">-InputObject</span></span>
<span data-ttu-id="5f16c-120">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="5f16c-120">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f16c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f16c-121">-Name</span></span>
<span data-ttu-id="5f16c-122">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="5f16c-122">The name of prefix.</span></span>

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

### <span data-ttu-id="5f16c-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="5f16c-123">-PeeringName</span></span>
<span data-ttu-id="5f16c-124">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="5f16c-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="5f16c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f16c-125">-ResourceGroupName</span></span>
<span data-ttu-id="5f16c-126">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f16c-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="5f16c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f16c-127">-ResourceId</span></span>
<span data-ttu-id="5f16c-128">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="5f16c-128">The resource id string name.</span></span>

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

### <span data-ttu-id="5f16c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f16c-129">CommonParameters</span></span>
<span data-ttu-id="5f16c-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f16c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f16c-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f16c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f16c-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f16c-132">INPUTS</span></span>

### <span data-ttu-id="5f16c-133">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="5f16c-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="5f16c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5f16c-134">System.String</span></span>

## <span data-ttu-id="5f16c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f16c-135">OUTPUTS</span></span>

### <span data-ttu-id="5f16c-136">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringRegisteredPrefix)</span><span class="sxs-lookup"><span data-stu-id="5f16c-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="5f16c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f16c-137">NOTES</span></span>

## <span data-ttu-id="5f16c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f16c-138">RELATED LINKS</span></span>
