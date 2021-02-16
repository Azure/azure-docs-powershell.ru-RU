---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213244"
---
# <span data-ttu-id="b0d5b-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="b0d5b-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="b0d5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d5b-103">Возвращает список местоположений пиринга, предлагаемых корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b0d5b-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="b0d5b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0d5b-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0d5b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0d5b-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d5b-106">Расположения пиринга списков.</span><span class="sxs-lookup"><span data-stu-id="b0d5b-106">List peering locations.</span></span>

## <span data-ttu-id="b0d5b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0d5b-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d5b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0d5b-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="b0d5b-109">Извлекает расположения пиринга для Вашингтона.</span><span class="sxs-lookup"><span data-stu-id="b0d5b-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="b0d5b-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b0d5b-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="b0d5b-111">Извлекает расположения пиринга для Вашингтона.</span><span class="sxs-lookup"><span data-stu-id="b0d5b-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="b0d5b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0d5b-112">PARAMETERS</span></span>

### <span data-ttu-id="b0d5b-113">-Country</span><span class="sxs-lookup"><span data-stu-id="b0d5b-113">-Country</span></span>
<span data-ttu-id="b0d5b-114">Фильтр страны</span><span class="sxs-lookup"><span data-stu-id="b0d5b-114">The country filter</span></span>

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

### <span data-ttu-id="b0d5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d5b-115">-DefaultProfile</span></span>
<span data-ttu-id="b0d5b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d5b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d5b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d5b-117">CommonParameters</span></span>
<span data-ttu-id="b0d5b-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d5b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d5b-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0d5b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d5b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0d5b-120">INPUTS</span></span>

### <span data-ttu-id="b0d5b-121">Нет</span><span class="sxs-lookup"><span data-stu-id="b0d5b-121">None</span></span>

## <span data-ttu-id="b0d5b-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0d5b-122">OUTPUTS</span></span>

### <span data-ttu-id="b0d5b-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="b0d5b-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="b0d5b-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0d5b-124">NOTES</span></span>

## <span data-ttu-id="b0d5b-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0d5b-125">RELATED LINKS</span></span>
