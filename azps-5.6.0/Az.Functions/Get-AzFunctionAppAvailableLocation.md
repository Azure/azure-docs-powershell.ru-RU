---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 987c4e351e024452231b5a5367ea7c2905d57863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969091"
---
# <span data-ttu-id="7d281-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="7d281-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="7d281-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d281-102">SYNOPSIS</span></span>
<span data-ttu-id="7d281-103">Расположение, в котором доступно приложение функции для данного ос и типа плана.</span><span class="sxs-lookup"><span data-stu-id="7d281-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="7d281-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d281-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7d281-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d281-105">DESCRIPTION</span></span>
<span data-ttu-id="7d281-106">Расположение, в котором доступно приложение функции для данного ос и типа плана.</span><span class="sxs-lookup"><span data-stu-id="7d281-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="7d281-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d281-107">EXAMPLES</span></span>

### <span data-ttu-id="7d281-108">Пример 1. Получите расположения, в которых premium доступна для Windows.</span><span class="sxs-lookup"><span data-stu-id="7d281-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="7d281-109">Если параметры не указаны, Для PlanType задан тип "Премиум", а для OSType — "Windows".</span><span class="sxs-lookup"><span data-stu-id="7d281-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
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

<span data-ttu-id="7d281-110">Эта команда возвращает расположения, в которых premium доступна для Windows.</span><span class="sxs-lookup"><span data-stu-id="7d281-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="7d281-111">Пример 2. Получите расположения, в которых premium доступна для Linux.</span><span class="sxs-lookup"><span data-stu-id="7d281-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
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

<span data-ttu-id="7d281-112">Эта команда возвращает расположения, в которых premium доступна для Linux.</span><span class="sxs-lookup"><span data-stu-id="7d281-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="7d281-113">Пример 3. Получите расположения, в которых доступно потребление для Windows.</span><span class="sxs-lookup"><span data-stu-id="7d281-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
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

<span data-ttu-id="7d281-114">Эта команда возвращает расположения, в которых доступно потребление для Windows.</span><span class="sxs-lookup"><span data-stu-id="7d281-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="7d281-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d281-115">PARAMETERS</span></span>

### <span data-ttu-id="7d281-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d281-116">-DefaultProfile</span></span>
<span data-ttu-id="7d281-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d281-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d281-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="7d281-118">-OSType</span></span>
<span data-ttu-id="7d281-119">Тип ОС для плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7d281-119">The OS type for the service plan.</span></span>

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

### <span data-ttu-id="7d281-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="7d281-120">-PlanType</span></span>
<span data-ttu-id="7d281-121">Тип плана.</span><span class="sxs-lookup"><span data-stu-id="7d281-121">The plan type.</span></span>
<span data-ttu-id="7d281-122">Допустимые входные данные: потребление или премиум</span><span class="sxs-lookup"><span data-stu-id="7d281-122">Valid inputs: Consumption or Premium</span></span>

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

### <span data-ttu-id="7d281-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d281-123">-SubscriptionId</span></span>
<span data-ttu-id="7d281-124">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="7d281-124">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="7d281-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d281-125">CommonParameters</span></span>
<span data-ttu-id="7d281-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d281-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d281-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d281-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d281-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d281-128">INPUTS</span></span>

## <span data-ttu-id="7d281-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d281-129">OUTPUTS</span></span>

### <span data-ttu-id="7d281-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="7d281-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="7d281-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d281-131">NOTES</span></span>

<span data-ttu-id="7d281-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7d281-132">ALIASES</span></span>

## <span data-ttu-id="7d281-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d281-133">RELATED LINKS</span></span>

