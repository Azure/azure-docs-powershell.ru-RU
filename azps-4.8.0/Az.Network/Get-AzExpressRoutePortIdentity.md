---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244156"
---
# <span data-ttu-id="65fa1-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="65fa1-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="65fa1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="65fa1-103">Получение удостоверения, назначенного ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="65fa1-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="65fa1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65fa1-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65fa1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65fa1-105">DESCRIPTION</span></span>
<span data-ttu-id="65fa1-106">Командлет **Get-AzExpressRoutePortIdentity** получает удостоверение, назначенное локальному объекту Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="65fa1-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="65fa1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65fa1-107">EXAMPLES</span></span>

### <span data-ttu-id="65fa1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65fa1-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="65fa1-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65fa1-109">PARAMETERS</span></span>

### <span data-ttu-id="65fa1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fa1-110">-DefaultProfile</span></span>
<span data-ttu-id="65fa1-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65fa1-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65fa1-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="65fa1-112">-ExpressRoutePort</span></span>
<span data-ttu-id="65fa1-113">Порт ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="65fa1-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65fa1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fa1-114">CommonParameters</span></span>
<span data-ttu-id="65fa1-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65fa1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fa1-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65fa1-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fa1-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65fa1-117">INPUTS</span></span>

### <span data-ttu-id="65fa1-118">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="65fa1-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="65fa1-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65fa1-119">OUTPUTS</span></span>

### <span data-ttu-id="65fa1-120">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="65fa1-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="65fa1-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="65fa1-121">NOTES</span></span>

## <span data-ttu-id="65fa1-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65fa1-122">RELATED LINKS</span></span>
[<span data-ttu-id="65fa1-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="65fa1-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="65fa1-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="65fa1-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="65fa1-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="65fa1-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)