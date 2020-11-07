---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733444"
---
# <span data-ttu-id="b44f9-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="b44f9-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="b44f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b44f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b44f9-103">Получить доступное делегирование служб в регионе.</span><span class="sxs-lookup"><span data-stu-id="b44f9-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b44f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b44f9-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b44f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b44f9-105">DESCRIPTION</span></span>
<span data-ttu-id="b44f9-106">Командлет **Get-AzureRmAvailableServiceDelegation** позволяет получить все доступные делегирования служб для подсети в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="b44f9-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="b44f9-107">Этот командлет *не* описывает, какие делегирования могут сосуществовать в одной подсети.</span><span class="sxs-lookup"><span data-stu-id="b44f9-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="b44f9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b44f9-108">EXAMPLES</span></span>

### <span data-ttu-id="b44f9-109">1: получить все доступные делегирования служб</span><span class="sxs-lookup"><span data-stu-id="b44f9-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="b44f9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b44f9-110">PARAMETERS</span></span>

### <span data-ttu-id="b44f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44f9-111">-DefaultProfile</span></span>
<span data-ttu-id="b44f9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b44f9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b44f9-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b44f9-113">-Location</span></span>
<span data-ttu-id="b44f9-114">Расположение.</span><span class="sxs-lookup"><span data-stu-id="b44f9-114">The location.</span></span>

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

### <span data-ttu-id="b44f9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44f9-115">CommonParameters</span></span>
<span data-ttu-id="b44f9-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b44f9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b44f9-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b44f9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44f9-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b44f9-118">INPUTS</span></span>

### <span data-ttu-id="b44f9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="b44f9-119">System.String</span></span>

## <span data-ttu-id="b44f9-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b44f9-120">OUTPUTS</span></span>

### <span data-ttu-id="b44f9-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="b44f9-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="b44f9-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="b44f9-122">NOTES</span></span>

## <span data-ttu-id="b44f9-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b44f9-123">RELATED LINKS</span></span>
<span data-ttu-id="b44f9-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="b44f9-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>
