---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246381"
---
# <span data-ttu-id="c4e8e-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="c4e8e-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="c4e8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e8e-103">Возвращает зарегистрированный ASN для соединения типа сервера маршрутизации Интернет Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="c4e8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4e8e-104">SYNTAX</span></span>

### <span data-ttu-id="c4e8e-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4e8e-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4e8e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c4e8e-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4e8e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e8e-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4e8e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4e8e-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e8e-109">Получить или просмотреть зарегистрированный ASN.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="c4e8e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4e8e-110">EXAMPLES</span></span>

### <span data-ttu-id="c4e8e-111">Список зарегистрированных ASNs для пиринга</span><span class="sxs-lookup"><span data-stu-id="c4e8e-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="c4e8e-112">Список зарегистрированных ASN.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-112">Lists registered asn.</span></span>

### <span data-ttu-id="c4e8e-113">Получает регистрацию ASN для пиринга по имени.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="c4e8e-114">Получает регистрацию ASN однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="c4e8e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4e8e-115">PARAMETERS</span></span>

### <span data-ttu-id="c4e8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e8e-116">-DefaultProfile</span></span>
<span data-ttu-id="c4e8e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4e8e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4e8e-118">-InputObject</span></span>
<span data-ttu-id="c4e8e-119">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c4e8e-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="c4e8e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4e8e-120">-Name</span></span>
<span data-ttu-id="c4e8e-121">Имя зарегистрированного ASN</span><span class="sxs-lookup"><span data-stu-id="c4e8e-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="c4e8e-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="c4e8e-122">-PeeringName</span></span>
<span data-ttu-id="c4e8e-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c4e8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4e8e-125">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="c4e8e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e8e-126">-ResourceId</span></span>
<span data-ttu-id="c4e8e-127">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-127">The resource id string name.</span></span>

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

### <span data-ttu-id="c4e8e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e8e-128">CommonParameters</span></span>
<span data-ttu-id="c4e8e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4e8e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e8e-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4e8e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e8e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4e8e-131">INPUTS</span></span>

### <span data-ttu-id="c4e8e-132">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="c4e8e-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="c4e8e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e8e-133">System.String</span></span>

## <span data-ttu-id="c4e8e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4e8e-134">OUTPUTS</span></span>

### <span data-ttu-id="c4e8e-135">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringRegisteredAsn)</span><span class="sxs-lookup"><span data-stu-id="c4e8e-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="c4e8e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4e8e-136">NOTES</span></span>

## <span data-ttu-id="c4e8e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4e8e-137">RELATED LINKS</span></span>
