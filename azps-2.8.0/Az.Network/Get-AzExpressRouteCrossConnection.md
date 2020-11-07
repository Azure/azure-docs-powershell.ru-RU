---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: c15a8b57338a6c5e7c2f054e07a0d26d716627fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902954"
---
# <span data-ttu-id="4df44-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="4df44-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="4df44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4df44-102">SYNOPSIS</span></span>
<span data-ttu-id="4df44-103">Возвращает перекрестное подключение Azure ExpressRoute из Azure.</span><span class="sxs-lookup"><span data-stu-id="4df44-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="4df44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4df44-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4df44-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4df44-105">DESCRIPTION</span></span>
<span data-ttu-id="4df44-106">Командлет **Get-AzExpressRouteCrossConnection** используется для получения объекта перекрестного соединения ExpressRoute из подписки.</span><span class="sxs-lookup"><span data-stu-id="4df44-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="4df44-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="4df44-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="4df44-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4df44-108">EXAMPLES</span></span>

### <span data-ttu-id="4df44-109">Пример 1: получение перекрестного соединения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4df44-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="4df44-110">Пример 2: Список перекрестных подключений ExpressRoute с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="4df44-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="4df44-111">Этот командлет выведет список всех перекрестных подключений ExpressRoute, начинающихся с "Test".</span><span class="sxs-lookup"><span data-stu-id="4df44-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="4df44-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4df44-112">PARAMETERS</span></span>

### <span data-ttu-id="4df44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df44-113">-DefaultProfile</span></span>
<span data-ttu-id="4df44-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4df44-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df44-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4df44-115">-Name</span></span>
<span data-ttu-id="4df44-116">Имя перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4df44-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4df44-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df44-117">-ResourceGroupName</span></span>
<span data-ttu-id="4df44-118">Имя группы ресурсов, содержащей перекрестное соединение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4df44-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4df44-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df44-119">CommonParameters</span></span>
<span data-ttu-id="4df44-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4df44-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df44-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4df44-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df44-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4df44-122">INPUTS</span></span>

### <span data-ttu-id="4df44-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="4df44-123">None</span></span>
<span data-ttu-id="4df44-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4df44-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4df44-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4df44-125">OUTPUTS</span></span>

### <span data-ttu-id="4df44-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="4df44-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="4df44-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="4df44-127">NOTES</span></span>

## <span data-ttu-id="4df44-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4df44-128">RELATED LINKS</span></span>

[<span data-ttu-id="4df44-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="4df44-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)