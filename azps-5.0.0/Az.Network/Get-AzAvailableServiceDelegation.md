---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245261"
---
# <span data-ttu-id="0c1fb-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="0c1fb-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="0c1fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c1fb-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1fb-103">Получить доступное делегирование служб в регионе.</span><span class="sxs-lookup"><span data-stu-id="0c1fb-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="0c1fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c1fb-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c1fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c1fb-105">DESCRIPTION</span></span>
<span data-ttu-id="0c1fb-106">Командлет **Get-AzAvailableServiceDelegation** позволяет получить все доступные делегирования служб для подсети в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="0c1fb-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="0c1fb-107">Этот командлет *не* описывает, какие делегирования могут сосуществовать в одной подсети.</span><span class="sxs-lookup"><span data-stu-id="0c1fb-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="0c1fb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c1fb-108">EXAMPLES</span></span>

### <span data-ttu-id="0c1fb-109">1: получить все доступные делегирования служб</span><span class="sxs-lookup"><span data-stu-id="0c1fb-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="0c1fb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c1fb-110">PARAMETERS</span></span>

### <span data-ttu-id="0c1fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1fb-111">-DefaultProfile</span></span>
<span data-ttu-id="0c1fb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c1fb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c1fb-113">-Location</span><span class="sxs-lookup"><span data-stu-id="0c1fb-113">-Location</span></span>
<span data-ttu-id="0c1fb-114">Расположение.</span><span class="sxs-lookup"><span data-stu-id="0c1fb-114">The location.</span></span>

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

### <span data-ttu-id="0c1fb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1fb-115">CommonParameters</span></span>
<span data-ttu-id="0c1fb-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c1fb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1fb-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c1fb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1fb-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c1fb-118">INPUTS</span></span>

### <span data-ttu-id="0c1fb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="0c1fb-119">System.String</span></span>

## <span data-ttu-id="0c1fb-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c1fb-120">OUTPUTS</span></span>

### <span data-ttu-id="0c1fb-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="0c1fb-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="0c1fb-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c1fb-122">NOTES</span></span>

## <span data-ttu-id="0c1fb-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c1fb-123">RELATED LINKS</span></span>

<span data-ttu-id="0c1fb-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="0c1fb-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>