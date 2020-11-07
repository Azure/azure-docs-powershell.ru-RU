---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909869"
---
# <span data-ttu-id="e92bd-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e92bd-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="e92bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e92bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e92bd-103">Возвращает виртуальную сеть в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e92bd-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="e92bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e92bd-104">SYNTAX</span></span>

### <span data-ttu-id="e92bd-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="e92bd-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e92bd-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="e92bd-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e92bd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e92bd-107">DESCRIPTION</span></span>
<span data-ttu-id="e92bd-108">Командлет **Get-AzVirtualNetwork** получает одну или несколько виртуальных сетей n группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e92bd-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="e92bd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e92bd-109">EXAMPLES</span></span>

### <span data-ttu-id="e92bd-110">1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e92bd-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="e92bd-111">Эта команда возвращает виртуальную сеть с именем MyVirtualNetwork в группе ресурсов TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e92bd-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="e92bd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e92bd-112">PARAMETERS</span></span>

### <span data-ttu-id="e92bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e92bd-113">-DefaultProfile</span></span>
<span data-ttu-id="e92bd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e92bd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e92bd-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e92bd-115">-ExpandResource</span></span>
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

### <span data-ttu-id="e92bd-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e92bd-116">-Name</span></span>
<span data-ttu-id="e92bd-117">Указывает имя виртуальной сети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e92bd-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e92bd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e92bd-118">-ResourceGroupName</span></span>
<span data-ttu-id="e92bd-119">Указывает имя группы ресурсов, к которой принадлежит виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="e92bd-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="e92bd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92bd-120">CommonParameters</span></span>
<span data-ttu-id="e92bd-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e92bd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92bd-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e92bd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92bd-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e92bd-123">INPUTS</span></span>

## <span data-ttu-id="e92bd-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e92bd-124">OUTPUTS</span></span>

### <span data-ttu-id="e92bd-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e92bd-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e92bd-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e92bd-126">NOTES</span></span>

## <span data-ttu-id="e92bd-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e92bd-127">RELATED LINKS</span></span>

[<span data-ttu-id="e92bd-128">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e92bd-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="e92bd-129">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e92bd-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="e92bd-130">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e92bd-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


