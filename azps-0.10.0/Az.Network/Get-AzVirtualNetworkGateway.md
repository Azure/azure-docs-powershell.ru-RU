---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 490e61142bdbc0bcdd64f18aeeb2fa527e5180b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909865"
---
# <span data-ttu-id="91ec2-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="91ec2-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="91ec2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="91ec2-103">Получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="91ec2-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="91ec2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91ec2-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91ec2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91ec2-105">DESCRIPTION</span></span>
<span data-ttu-id="91ec2-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="91ec2-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="91ec2-107">Командлет **Get-AzVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91ec2-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="91ec2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91ec2-108">EXAMPLES</span></span>

### <span data-ttu-id="91ec2-109">1: получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="91ec2-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="91ec2-110">Возвращает объект шлюза виртуальной сети с именем "myGateway" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="91ec2-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="91ec2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91ec2-111">PARAMETERS</span></span>

### <span data-ttu-id="91ec2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ec2-112">-DefaultProfile</span></span>
<span data-ttu-id="91ec2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91ec2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91ec2-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91ec2-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91ec2-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ec2-116">CommonParameters</span></span>
<span data-ttu-id="91ec2-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91ec2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ec2-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ec2-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ec2-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91ec2-119">INPUTS</span></span>

## <span data-ttu-id="91ec2-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91ec2-120">OUTPUTS</span></span>

### <span data-ttu-id="91ec2-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="91ec2-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="91ec2-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="91ec2-122">NOTES</span></span>

## <span data-ttu-id="91ec2-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91ec2-123">RELATED LINKS</span></span>

