---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406348"
---
# <span data-ttu-id="cecae-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="cecae-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="cecae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cecae-102">SYNOPSIS</span></span>
<span data-ttu-id="cecae-103">Расположение, в котором доступно приложение функции для данного ос и типа плана.</span><span class="sxs-lookup"><span data-stu-id="cecae-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="cecae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cecae-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cecae-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cecae-105">DESCRIPTION</span></span>
<span data-ttu-id="cecae-106">Расположение, в котором доступно приложение функции для данного ос и типа плана.</span><span class="sxs-lookup"><span data-stu-id="cecae-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="cecae-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cecae-107">EXAMPLES</span></span>

### <span data-ttu-id="cecae-108">Пример 1. Получите расположения, в которых premium доступна для Windows.</span><span class="sxs-lookup"><span data-stu-id="cecae-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="cecae-109">Если параметры не указаны, Для PlanType задан тип "Премиум", а для OSType — "Windows".</span><span class="sxs-lookup"><span data-stu-id="cecae-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="cecae-110">Эта команда возвращает расположения, в которых premium доступна для Windows.</span><span class="sxs-lookup"><span data-stu-id="cecae-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="cecae-111">Пример 2. Получите расположения, в которых premium доступна для Linux.</span><span class="sxs-lookup"><span data-stu-id="cecae-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="cecae-112">Эта команда возвращает расположения, в которых premium доступна для Linux.</span><span class="sxs-lookup"><span data-stu-id="cecae-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="cecae-113">Пример 3. Получите расположения, в которых доступно потребление для Windows.</span><span class="sxs-lookup"><span data-stu-id="cecae-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="cecae-114">Эта команда возвращает расположения, в которых доступно потребление для Windows.</span><span class="sxs-lookup"><span data-stu-id="cecae-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="cecae-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cecae-115">PARAMETERS</span></span>

### <span data-ttu-id="cecae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cecae-116">-DefaultProfile</span></span>
<span data-ttu-id="cecae-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cecae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cecae-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="cecae-118">-OSType</span></span>
<span data-ttu-id="cecae-119">Тип ОС для плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cecae-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cecae-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="cecae-120">-PlanType</span></span>
<span data-ttu-id="cecae-121">Тип плана.</span><span class="sxs-lookup"><span data-stu-id="cecae-121">The plan type.</span></span>
<span data-ttu-id="cecae-122">Допустимые входные данные: потребление или премиум</span><span class="sxs-lookup"><span data-stu-id="cecae-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cecae-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cecae-123">-SubscriptionId</span></span>
<span data-ttu-id="cecae-124">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="cecae-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cecae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cecae-125">CommonParameters</span></span>
<span data-ttu-id="cecae-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cecae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cecae-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cecae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cecae-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cecae-128">INPUTS</span></span>

## <span data-ttu-id="cecae-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cecae-129">OUTPUTS</span></span>

### <span data-ttu-id="cecae-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="cecae-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="cecae-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cecae-131">NOTES</span></span>

<span data-ttu-id="cecae-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cecae-132">ALIASES</span></span>

## <span data-ttu-id="cecae-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cecae-133">RELATED LINKS</span></span>

