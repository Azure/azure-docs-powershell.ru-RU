---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: a81bb1515e25f9000438fbd463117e4fd69b9690
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245432"
---
# <span data-ttu-id="333a8-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="333a8-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="333a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="333a8-102">SYNOPSIS</span></span>
<span data-ttu-id="333a8-103">Возвращает приложения-функции в подписке.</span><span class="sxs-lookup"><span data-stu-id="333a8-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="333a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="333a8-104">SYNTAX</span></span>

### <span data-ttu-id="333a8-105">GetAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="333a8-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="333a8-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="333a8-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="333a8-107">ByName</span><span class="sxs-lookup"><span data-stu-id="333a8-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="333a8-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333a8-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="333a8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="333a8-109">DESCRIPTION</span></span>
<span data-ttu-id="333a8-110">Возвращает приложения-функции в подписке.</span><span class="sxs-lookup"><span data-stu-id="333a8-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="333a8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="333a8-111">EXAMPLES</span></span>

### <span data-ttu-id="333a8-112">Пример 1: получение всех приложений для всех функций.</span><span class="sxs-lookup"><span data-stu-id="333a8-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="333a8-113">Пример 2: получение приложений функций по имени.</span><span class="sxs-lookup"><span data-stu-id="333a8-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="333a8-114">Пример 3: получение приложений функций по названию группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="333a8-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="333a8-115">Пример 4: получение приложений функций для заданных подписок.</span><span class="sxs-lookup"><span data-stu-id="333a8-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="333a8-116">Пример 5: получение приложений функций по местоположению.</span><span class="sxs-lookup"><span data-stu-id="333a8-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="333a8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="333a8-117">PARAMETERS</span></span>

### <span data-ttu-id="333a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333a8-118">-DefaultProfile</span></span>
<span data-ttu-id="333a8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="333a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="333a8-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="333a8-120">-IncludeSlot</span></span>
<span data-ttu-id="333a8-121">Укажите, следует ли включать слоты развертывания в результаты.</span><span class="sxs-lookup"><span data-stu-id="333a8-121">Use to specify whether to include deployment slots in results.</span></span>

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

### <span data-ttu-id="333a8-122">-Location</span><span class="sxs-lookup"><span data-stu-id="333a8-122">-Location</span></span>
<span data-ttu-id="333a8-123">Расположение приложения "функция".</span><span class="sxs-lookup"><span data-stu-id="333a8-123">The location of the function app.</span></span>

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

### <span data-ttu-id="333a8-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="333a8-124">-Name</span></span>
<span data-ttu-id="333a8-125">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="333a8-125">The name of the function app.</span></span>

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

### <span data-ttu-id="333a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="333a8-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="333a8-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="333a8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="333a8-128">-SubscriptionId</span></span>
<span data-ttu-id="333a8-129">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="333a8-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="333a8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333a8-130">CommonParameters</span></span>
<span data-ttu-id="333a8-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="333a8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333a8-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="333a8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333a8-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="333a8-133">INPUTS</span></span>

## <span data-ttu-id="333a8-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="333a8-134">OUTPUTS</span></span>

### <span data-ttu-id="333a8-135">Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="333a8-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="333a8-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="333a8-136">NOTES</span></span>

<span data-ttu-id="333a8-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="333a8-137">ALIASES</span></span>

## <span data-ttu-id="333a8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="333a8-138">RELATED LINKS</span></span>

