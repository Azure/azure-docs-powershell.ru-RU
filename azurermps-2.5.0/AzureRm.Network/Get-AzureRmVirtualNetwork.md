---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 983c23111486a964275a7efb85031b013fb365d2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914866"
---
# <span data-ttu-id="80398-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80398-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="80398-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80398-102">SYNOPSIS</span></span>
<span data-ttu-id="80398-103">Возвращает виртуальную сеть в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80398-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80398-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80398-104">SYNTAX</span></span>

### <span data-ttu-id="80398-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="80398-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80398-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="80398-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80398-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80398-107">DESCRIPTION</span></span>
<span data-ttu-id="80398-108">Командлет **Get-AzureRmVirtualNetwork** получает одну или несколько виртуальных сетей n группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80398-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="80398-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80398-109">EXAMPLES</span></span>

### <span data-ttu-id="80398-110">1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="80398-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="80398-111">Эта команда возвращает виртуальную сеть с именем MyVirtualNetwork в группе ресурсов TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="80398-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="80398-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80398-112">PARAMETERS</span></span>

### <span data-ttu-id="80398-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80398-113">-DefaultProfile</span></span>
<span data-ttu-id="80398-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80398-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80398-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="80398-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80398-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80398-116">-Name</span></span>
<span data-ttu-id="80398-117">Указывает имя виртуальной сети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="80398-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80398-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80398-118">-ResourceGroupName</span></span>
<span data-ttu-id="80398-119">Указывает имя группы ресурсов, к которой принадлежит виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="80398-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80398-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80398-120">CommonParameters</span></span>
<span data-ttu-id="80398-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80398-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80398-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80398-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80398-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80398-123">INPUTS</span></span>

## <span data-ttu-id="80398-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80398-124">OUTPUTS</span></span>

### <span data-ttu-id="80398-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80398-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="80398-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="80398-126">NOTES</span></span>

## <span data-ttu-id="80398-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80398-127">RELATED LINKS</span></span>

[<span data-ttu-id="80398-128">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80398-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="80398-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80398-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="80398-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80398-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


