---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: a81bb1515e25f9000438fbd463117e4fd69b9690
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504857"
---
# <span data-ttu-id="a14c5-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="a14c5-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="a14c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a14c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a14c5-103">Получает приложения функций в подписке.</span><span class="sxs-lookup"><span data-stu-id="a14c5-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="a14c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a14c5-104">SYNTAX</span></span>

### <span data-ttu-id="a14c5-105">GetAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a14c5-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a14c5-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="a14c5-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a14c5-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a14c5-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a14c5-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a14c5-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a14c5-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a14c5-109">DESCRIPTION</span></span>
<span data-ttu-id="a14c5-110">Получает приложения функций в подписке.</span><span class="sxs-lookup"><span data-stu-id="a14c5-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="a14c5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a14c5-111">EXAMPLES</span></span>

### <span data-ttu-id="a14c5-112">Пример 1. Получить все приложения функций.</span><span class="sxs-lookup"><span data-stu-id="a14c5-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="a14c5-113">Пример 2. Получить приложения функции по имени.</span><span class="sxs-lookup"><span data-stu-id="a14c5-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="a14c5-114">Пример 3. Получить приложения функций по имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a14c5-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="a14c5-115">Пример 4. Получить приложения функций для заданной подписки.</span><span class="sxs-lookup"><span data-stu-id="a14c5-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="a14c5-116">Пример 5. Получить приложения функций по расположению.</span><span class="sxs-lookup"><span data-stu-id="a14c5-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="a14c5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a14c5-117">PARAMETERS</span></span>

### <span data-ttu-id="a14c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14c5-118">-DefaultProfile</span></span>
<span data-ttu-id="a14c5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a14c5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a14c5-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="a14c5-120">-IncludeSlot</span></span>
<span data-ttu-id="a14c5-121">Используется для указания того, следует ли включать слоты развертывания в результаты.</span><span class="sxs-lookup"><span data-stu-id="a14c5-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a14c5-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a14c5-122">-Location</span></span>
<span data-ttu-id="a14c5-123">Расположение приложения функции.</span><span class="sxs-lookup"><span data-stu-id="a14c5-123">The location of the function app.</span></span>

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

### <span data-ttu-id="a14c5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a14c5-124">-Name</span></span>
<span data-ttu-id="a14c5-125">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="a14c5-125">The name of the function app.</span></span>

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

### <span data-ttu-id="a14c5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a14c5-126">-ResourceGroupName</span></span>
<span data-ttu-id="a14c5-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a14c5-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a14c5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a14c5-128">-SubscriptionId</span></span>
<span data-ttu-id="a14c5-129">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a14c5-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="a14c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14c5-130">CommonParameters</span></span>
<span data-ttu-id="a14c5-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14c5-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a14c5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14c5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a14c5-133">INPUTS</span></span>

## <span data-ttu-id="a14c5-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a14c5-134">OUTPUTS</span></span>

### <span data-ttu-id="a14c5-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="a14c5-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="a14c5-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a14c5-136">NOTES</span></span>

<span data-ttu-id="a14c5-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a14c5-137">ALIASES</span></span>

## <span data-ttu-id="a14c5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a14c5-138">RELATED LINKS</span></span>

