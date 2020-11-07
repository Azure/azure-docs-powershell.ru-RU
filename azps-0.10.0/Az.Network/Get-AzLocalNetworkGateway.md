---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 88c17626da87608a1086331289cb99f8e7668e5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909954"
---
# <span data-ttu-id="7e013-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e013-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="7e013-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e013-102">SYNOPSIS</span></span>
<span data-ttu-id="7e013-103">Получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="7e013-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="7e013-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e013-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e013-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e013-105">DESCRIPTION</span></span>
<span data-ttu-id="7e013-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="7e013-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="7e013-107">Командлет **Get-AzLocalNetworkGateway** возвращает объект, представляющий локальный шлюз на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e013-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="7e013-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e013-108">EXAMPLES</span></span>

### <span data-ttu-id="7e013-109">1: получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="7e013-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="7e013-110">Возвращает объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="7e013-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="7e013-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e013-111">PARAMETERS</span></span>

### <span data-ttu-id="7e013-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e013-112">-DefaultProfile</span></span>
<span data-ttu-id="7e013-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e013-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e013-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e013-114">-Name</span></span>
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

### <span data-ttu-id="7e013-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e013-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7e013-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e013-116">CommonParameters</span></span>
<span data-ttu-id="7e013-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e013-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e013-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e013-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e013-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e013-119">INPUTS</span></span>

## <span data-ttu-id="7e013-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e013-120">OUTPUTS</span></span>

### <span data-ttu-id="7e013-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e013-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="7e013-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e013-122">NOTES</span></span>

## <span data-ttu-id="7e013-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e013-123">RELATED LINKS</span></span>

