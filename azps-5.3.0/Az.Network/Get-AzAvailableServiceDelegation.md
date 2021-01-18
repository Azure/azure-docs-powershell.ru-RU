---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506110"
---
# <span data-ttu-id="d5abb-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="d5abb-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="d5abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5abb-102">SYNOPSIS</span></span>
<span data-ttu-id="d5abb-103">Получить доступ к делегирования служб в регионе.</span><span class="sxs-lookup"><span data-stu-id="d5abb-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="d5abb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5abb-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5abb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5abb-105">DESCRIPTION</span></span>
<span data-ttu-id="d5abb-106">Для **подсети** в предоставленном расположении можно получить все доступные делегирование службы.</span><span class="sxs-lookup"><span data-stu-id="d5abb-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="d5abb-107">Этот cmdlet *не описывает,* какие делегирования могут сосуществовать в одной подсети.</span><span class="sxs-lookup"><span data-stu-id="d5abb-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="d5abb-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5abb-108">EXAMPLES</span></span>

### <span data-ttu-id="d5abb-109">1. Получение всех доступных делегирования служб</span><span class="sxs-lookup"><span data-stu-id="d5abb-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="d5abb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5abb-110">PARAMETERS</span></span>

### <span data-ttu-id="d5abb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5abb-111">-DefaultProfile</span></span>
<span data-ttu-id="d5abb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5abb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5abb-113">-Location</span><span class="sxs-lookup"><span data-stu-id="d5abb-113">-Location</span></span>
<span data-ttu-id="d5abb-114">Расположение.</span><span class="sxs-lookup"><span data-stu-id="d5abb-114">The location.</span></span>

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

### <span data-ttu-id="d5abb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5abb-115">CommonParameters</span></span>
<span data-ttu-id="d5abb-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5abb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5abb-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5abb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5abb-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5abb-118">INPUTS</span></span>

### <span data-ttu-id="d5abb-119">System.String</span><span class="sxs-lookup"><span data-stu-id="d5abb-119">System.String</span></span>

## <span data-ttu-id="d5abb-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5abb-120">OUTPUTS</span></span>

### <span data-ttu-id="d5abb-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="d5abb-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="d5abb-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5abb-122">NOTES</span></span>

## <span data-ttu-id="d5abb-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5abb-123">RELATED LINKS</span></span>

<span data-ttu-id="d5abb-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="d5abb-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>