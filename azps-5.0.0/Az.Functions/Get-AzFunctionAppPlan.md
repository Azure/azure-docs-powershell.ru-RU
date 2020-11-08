---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245429"
---
# <span data-ttu-id="a0792-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="a0792-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="a0792-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0792-102">SYNOPSIS</span></span>
<span data-ttu-id="a0792-103">Приложения Function. планы в подписке.</span><span class="sxs-lookup"><span data-stu-id="a0792-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="a0792-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0792-104">SYNTAX</span></span>

### <span data-ttu-id="a0792-105">GetAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0792-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a0792-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="a0792-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0792-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a0792-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a0792-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0792-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0792-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0792-109">DESCRIPTION</span></span>
<span data-ttu-id="a0792-110">Приложения Function. планы в подписке.</span><span class="sxs-lookup"><span data-stu-id="a0792-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="a0792-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0792-111">EXAMPLES</span></span>

### <span data-ttu-id="a0792-112">Пример 1: получение планов приложений для всех функций.</span><span class="sxs-lookup"><span data-stu-id="a0792-112">Example 1: Get all function app plans.</span></span>
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

<span data-ttu-id="a0792-113">Эта команда получает планы приложения для всех функций.</span><span class="sxs-lookup"><span data-stu-id="a0792-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="a0792-114">Пример 2: получение планов приложений функций по названию группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0792-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="a0792-115">Эта команда получает планы приложения для функций по имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0792-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="a0792-116">Пример 3: получение планов приложений функций для заданных подписок.</span><span class="sxs-lookup"><span data-stu-id="a0792-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="a0792-117">Эта команда получает планы приложения для заданных подписок.</span><span class="sxs-lookup"><span data-stu-id="a0792-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="a0792-118">Пример 4: получение планов приложений функций по местоположению.</span><span class="sxs-lookup"><span data-stu-id="a0792-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="a0792-119">Эта команда получает планы приложения по расположению.</span><span class="sxs-lookup"><span data-stu-id="a0792-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="a0792-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0792-120">PARAMETERS</span></span>

### <span data-ttu-id="a0792-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0792-121">-DefaultProfile</span></span>
<span data-ttu-id="a0792-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0792-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0792-123">-Location</span><span class="sxs-lookup"><span data-stu-id="a0792-123">-Location</span></span>
<span data-ttu-id="a0792-124">Расположение плана приложения функции.</span><span class="sxs-lookup"><span data-stu-id="a0792-124">The location of the function app plan.</span></span>

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

### <span data-ttu-id="a0792-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a0792-125">-Name</span></span>
<span data-ttu-id="a0792-126">Имя плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a0792-126">The service plan name.</span></span>

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

### <span data-ttu-id="a0792-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0792-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0792-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0792-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0792-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0792-129">-SubscriptionId</span></span>
<span data-ttu-id="a0792-130">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a0792-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="a0792-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0792-131">CommonParameters</span></span>
<span data-ttu-id="a0792-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0792-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0792-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0792-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0792-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0792-134">INPUTS</span></span>

## <span data-ttu-id="a0792-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0792-135">OUTPUTS</span></span>

### <span data-ttu-id="a0792-136">Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a0792-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a0792-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0792-137">NOTES</span></span>

<span data-ttu-id="a0792-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a0792-138">ALIASES</span></span>

## <span data-ttu-id="a0792-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0792-139">RELATED LINKS</span></span>

