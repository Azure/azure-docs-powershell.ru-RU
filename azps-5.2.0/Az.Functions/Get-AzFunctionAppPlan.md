---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392599"
---
# <span data-ttu-id="b519f-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="b519f-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="b519f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b519f-102">SYNOPSIS</span></span>
<span data-ttu-id="b519f-103">Получите планы приложений функций в подписке.</span><span class="sxs-lookup"><span data-stu-id="b519f-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="b519f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b519f-104">SYNTAX</span></span>

### <span data-ttu-id="b519f-105">GetAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b519f-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b519f-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="b519f-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b519f-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b519f-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b519f-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b519f-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b519f-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b519f-109">DESCRIPTION</span></span>
<span data-ttu-id="b519f-110">Получите планы приложений функций в подписке.</span><span class="sxs-lookup"><span data-stu-id="b519f-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="b519f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b519f-111">EXAMPLES</span></span>

### <span data-ttu-id="b519f-112">Пример 1. Получить все планы приложений для функций.</span><span class="sxs-lookup"><span data-stu-id="b519f-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="b519f-113">Эта команда получает все планы приложений для функций.</span><span class="sxs-lookup"><span data-stu-id="b519f-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="b519f-114">Пример 2. Получать планы приложения функций по имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b519f-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="b519f-115">Эта команда получает планы приложения функций по имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b519f-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="b519f-116">Пример 3. Получить планы приложений функций для заданной подписки.</span><span class="sxs-lookup"><span data-stu-id="b519f-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="b519f-117">Эта команда получает планы приложения функций для заданной подписки.</span><span class="sxs-lookup"><span data-stu-id="b519f-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="b519f-118">Пример 4. Получить планы приложения функций по расположению.</span><span class="sxs-lookup"><span data-stu-id="b519f-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="b519f-119">Эта команда получает планы приложения функций по расположению.</span><span class="sxs-lookup"><span data-stu-id="b519f-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="b519f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b519f-120">PARAMETERS</span></span>

### <span data-ttu-id="b519f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b519f-121">-DefaultProfile</span></span>
<span data-ttu-id="b519f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b519f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b519f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="b519f-123">-Location</span></span>
<span data-ttu-id="b519f-124">Расположение плана приложения функции.</span><span class="sxs-lookup"><span data-stu-id="b519f-124">The location of the function app plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b519f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b519f-125">-Name</span></span>
<span data-ttu-id="b519f-126">Название плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b519f-126">The service plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b519f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b519f-127">-ResourceGroupName</span></span>
<span data-ttu-id="b519f-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b519f-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b519f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b519f-129">-SubscriptionId</span></span>
<span data-ttu-id="b519f-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="b519f-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b519f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b519f-131">CommonParameters</span></span>
<span data-ttu-id="b519f-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b519f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b519f-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b519f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b519f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b519f-134">INPUTS</span></span>

## <span data-ttu-id="b519f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b519f-135">OUTPUTS</span></span>

### <span data-ttu-id="b519f-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b519f-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="b519f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b519f-137">NOTES</span></span>

<span data-ttu-id="b519f-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b519f-138">ALIASES</span></span>

## <span data-ttu-id="b519f-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b519f-139">RELATED LINKS</span></span>

