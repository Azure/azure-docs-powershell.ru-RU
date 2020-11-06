---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1745e3a87d91917e762c9b0e441110b4b6945601
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560291"
---
# <span data-ttu-id="38806-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38806-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="38806-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38806-102">SYNOPSIS</span></span>
<span data-ttu-id="38806-103">Возвращает виртуальную сеть в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38806-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38806-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38806-104">SYNTAX</span></span>

### <span data-ttu-id="38806-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="38806-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38806-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="38806-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38806-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38806-107">DESCRIPTION</span></span>
<span data-ttu-id="38806-108">Командлет **Get-AzureRmVirtualNetwork** получает одну или несколько виртуальных сетей n группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38806-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="38806-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38806-109">EXAMPLES</span></span>

### <span data-ttu-id="38806-110">1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="38806-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="38806-111">Эта команда возвращает виртуальную сеть с именем MyVirtualNetwork в группе ресурсов TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38806-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="38806-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38806-112">PARAMETERS</span></span>

### <span data-ttu-id="38806-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38806-113">-DefaultProfile</span></span>
<span data-ttu-id="38806-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38806-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38806-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="38806-115">-ExpandResource</span></span>
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

### <span data-ttu-id="38806-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38806-116">-Name</span></span>
<span data-ttu-id="38806-117">Указывает имя виртуальной сети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="38806-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="38806-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38806-118">-ResourceGroupName</span></span>
<span data-ttu-id="38806-119">Указывает имя группы ресурсов, к которой принадлежит виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="38806-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="38806-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38806-120">CommonParameters</span></span>
<span data-ttu-id="38806-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38806-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38806-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38806-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38806-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38806-123">INPUTS</span></span>

### <span data-ttu-id="38806-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="38806-124">None</span></span>
<span data-ttu-id="38806-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="38806-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38806-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38806-126">OUTPUTS</span></span>

### <span data-ttu-id="38806-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38806-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="38806-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="38806-128">NOTES</span></span>

## <span data-ttu-id="38806-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38806-129">RELATED LINKS</span></span>

[<span data-ttu-id="38806-130">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38806-130">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="38806-131">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38806-131">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="38806-132">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38806-132">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


