---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: d955cb51d92d9d0f3c156900d847e903d642e9af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565604"
---
# <span data-ttu-id="9e700-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e700-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="9e700-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e700-102">SYNOPSIS</span></span>
<span data-ttu-id="9e700-103">Возвращает виртуальную сеть в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e700-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e700-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e700-104">SYNTAX</span></span>

### <span data-ttu-id="9e700-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="9e700-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e700-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="9e700-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e700-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e700-107">DESCRIPTION</span></span>
<span data-ttu-id="9e700-108">Командлет **Get-AzureRmVirtualNetwork** получает одну или несколько виртуальных сетей n группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e700-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="9e700-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e700-109">EXAMPLES</span></span>

### <span data-ttu-id="9e700-110">1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="9e700-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="9e700-111">Эта команда возвращает виртуальную сеть с именем MyVirtualNetwork в группе ресурсов TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e700-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="9e700-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e700-112">PARAMETERS</span></span>

### <span data-ttu-id="9e700-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="9e700-113">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e700-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e700-114">-Name</span></span>
<span data-ttu-id="9e700-115">Указывает имя виртуальной сети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9e700-115">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e700-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e700-116">-ResourceGroupName</span></span>
<span data-ttu-id="9e700-117">Указывает имя группы ресурсов, к которой принадлежит виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="9e700-117">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e700-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e700-118">-DefaultProfile</span></span>
<span data-ttu-id="9e700-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e700-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e700-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e700-120">CommonParameters</span></span>
<span data-ttu-id="9e700-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e700-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e700-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e700-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e700-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e700-123">INPUTS</span></span>

## <span data-ttu-id="9e700-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e700-124">OUTPUTS</span></span>

### <span data-ttu-id="9e700-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e700-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9e700-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e700-126">NOTES</span></span>

## <span data-ttu-id="9e700-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e700-127">RELATED LINKS</span></span>

[<span data-ttu-id="9e700-128">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e700-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9e700-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e700-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9e700-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e700-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


