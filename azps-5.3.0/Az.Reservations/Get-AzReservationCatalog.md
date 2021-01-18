---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505973"
---
# <span data-ttu-id="28f83-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="28f83-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="28f83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28f83-102">SYNOPSIS</span></span>
<span data-ttu-id="28f83-103">Получить каталог доступных резервирования</span><span class="sxs-lookup"><span data-stu-id="28f83-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="28f83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28f83-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28f83-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28f83-105">DESCRIPTION</span></span>
<span data-ttu-id="28f83-106">Получите регионы и skus, доступные для покупки зарезервированного экземпляра для указанной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="28f83-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="28f83-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28f83-107">EXAMPLES</span></span>

### <span data-ttu-id="28f83-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28f83-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="28f83-109">Получить каталог VirtualMa в westus для подписки по умолчанию</span><span class="sxs-lookup"><span data-stu-id="28f83-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="28f83-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="28f83-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="28f83-111">Получить каталог SuseLinux для указанной подписки</span><span class="sxs-lookup"><span data-stu-id="28f83-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="28f83-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28f83-112">PARAMETERS</span></span>

### <span data-ttu-id="28f83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f83-113">-DefaultProfile</span></span>
<span data-ttu-id="28f83-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28f83-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28f83-115">-Location</span><span class="sxs-lookup"><span data-stu-id="28f83-115">-Location</span></span>
<span data-ttu-id="28f83-116">Определяет расположение зарезервированных ресурсов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="28f83-116">Specifies the location of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f83-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="28f83-117">-ReservedResourceType</span></span>
<span data-ttu-id="28f83-118">Определяет тип зарезервированных ресурсов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="28f83-118">Specifies the type of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f83-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28f83-119">-SubscriptionId</span></span>
<span data-ttu-id="28f83-120">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="28f83-120">Id of the subscription</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f83-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f83-121">CommonParameters</span></span>
<span data-ttu-id="28f83-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f83-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f83-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28f83-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f83-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28f83-124">INPUTS</span></span>

### <span data-ttu-id="28f83-125">Нет</span><span class="sxs-lookup"><span data-stu-id="28f83-125">None</span></span>

## <span data-ttu-id="28f83-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28f83-126">OUTPUTS</span></span>

### <span data-ttu-id="28f83-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span><span class="sxs-lookup"><span data-stu-id="28f83-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="28f83-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28f83-128">NOTES</span></span>

## <span data-ttu-id="28f83-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28f83-129">RELATED LINKS</span></span>
