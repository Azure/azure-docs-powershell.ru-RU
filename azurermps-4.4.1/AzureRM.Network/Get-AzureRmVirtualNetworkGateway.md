---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: ed57a1832e3581d4d49b285fa9e61c93b17be02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565602"
---
# <span data-ttu-id="e207b-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e207b-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="e207b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e207b-102">SYNOPSIS</span></span>
<span data-ttu-id="e207b-103">Получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e207b-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e207b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e207b-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e207b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e207b-105">DESCRIPTION</span></span>
<span data-ttu-id="e207b-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="e207b-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="e207b-107">Командлет **Get-AzureRmVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e207b-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="e207b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e207b-108">EXAMPLES</span></span>

### <span data-ttu-id="e207b-109">1: получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e207b-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="e207b-110">Возвращает объект шлюза виртуальной сети с именем "myGateway" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="e207b-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="e207b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e207b-111">PARAMETERS</span></span>

### <span data-ttu-id="e207b-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e207b-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e207b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e207b-113">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e207b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e207b-114">-DefaultProfile</span></span>
<span data-ttu-id="e207b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e207b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e207b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e207b-116">CommonParameters</span></span>
<span data-ttu-id="e207b-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e207b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e207b-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e207b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e207b-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e207b-119">INPUTS</span></span>

## <span data-ttu-id="e207b-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e207b-120">OUTPUTS</span></span>

### <span data-ttu-id="e207b-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e207b-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e207b-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="e207b-122">NOTES</span></span>

## <span data-ttu-id="e207b-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e207b-123">RELATED LINKS</span></span>

