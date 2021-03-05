---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: ee678b905eba891543399c9130a8ef034daf2a16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969096"
---
# <span data-ttu-id="acf57-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="acf57-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="acf57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acf57-102">SYNOPSIS</span></span>
<span data-ttu-id="acf57-103">Получает приложения функций в подписке.</span><span class="sxs-lookup"><span data-stu-id="acf57-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="acf57-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="acf57-104">SYNTAX</span></span>

### <span data-ttu-id="acf57-105">GetAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acf57-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="acf57-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="acf57-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="acf57-107">ByName</span><span class="sxs-lookup"><span data-stu-id="acf57-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="acf57-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf57-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="acf57-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acf57-109">DESCRIPTION</span></span>
<span data-ttu-id="acf57-110">Получает приложения функций в подписке.</span><span class="sxs-lookup"><span data-stu-id="acf57-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="acf57-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="acf57-111">EXAMPLES</span></span>

### <span data-ttu-id="acf57-112">Пример 1. Получить все приложения функций.</span><span class="sxs-lookup"><span data-stu-id="acf57-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="acf57-113">Пример 2. Получить приложения функции по имени.</span><span class="sxs-lookup"><span data-stu-id="acf57-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="acf57-114">Пример 3. Получить приложения функций по имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acf57-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="acf57-115">Пример 4. Получить приложения функций для заданной подписки.</span><span class="sxs-lookup"><span data-stu-id="acf57-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="acf57-116">Пример 5. Получить приложения функций по расположению.</span><span class="sxs-lookup"><span data-stu-id="acf57-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="acf57-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acf57-117">PARAMETERS</span></span>

### <span data-ttu-id="acf57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf57-118">-DefaultProfile</span></span>
<span data-ttu-id="acf57-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acf57-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf57-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="acf57-120">-IncludeSlot</span></span>
<span data-ttu-id="acf57-121">Используется для указания того, следует ли включать слоты развертывания в результаты.</span><span class="sxs-lookup"><span data-stu-id="acf57-121">Use to specify whether to include deployment slots in results.</span></span>

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

### <span data-ttu-id="acf57-122">-Location</span><span class="sxs-lookup"><span data-stu-id="acf57-122">-Location</span></span>
<span data-ttu-id="acf57-123">Расположение приложения функции.</span><span class="sxs-lookup"><span data-stu-id="acf57-123">The location of the function app.</span></span>

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

### <span data-ttu-id="acf57-124">-Name</span><span class="sxs-lookup"><span data-stu-id="acf57-124">-Name</span></span>
<span data-ttu-id="acf57-125">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="acf57-125">The name of the function app.</span></span>

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

### <span data-ttu-id="acf57-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf57-126">-ResourceGroupName</span></span>
<span data-ttu-id="acf57-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acf57-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="acf57-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acf57-128">-SubscriptionId</span></span>
<span data-ttu-id="acf57-129">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="acf57-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="acf57-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf57-130">CommonParameters</span></span>
<span data-ttu-id="acf57-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf57-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf57-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acf57-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf57-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acf57-133">INPUTS</span></span>

## <span data-ttu-id="acf57-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acf57-134">OUTPUTS</span></span>

### <span data-ttu-id="acf57-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="acf57-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="acf57-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="acf57-136">NOTES</span></span>

<span data-ttu-id="acf57-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="acf57-137">ALIASES</span></span>

## <span data-ttu-id="acf57-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acf57-138">RELATED LINKS</span></span>

