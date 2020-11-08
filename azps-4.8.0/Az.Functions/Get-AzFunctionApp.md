---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: 6a3a421f1da374db1cc08635891bdeec4375855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242772"
---
# <span data-ttu-id="75d00-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="75d00-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="75d00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75d00-102">SYNOPSIS</span></span>
<span data-ttu-id="75d00-103">Возвращает приложения-функции в подписке.</span><span class="sxs-lookup"><span data-stu-id="75d00-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="75d00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75d00-104">SYNTAX</span></span>

### <span data-ttu-id="75d00-105">GetAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75d00-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="75d00-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="75d00-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="75d00-107">ByName</span><span class="sxs-lookup"><span data-stu-id="75d00-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="75d00-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d00-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="75d00-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75d00-109">DESCRIPTION</span></span>
<span data-ttu-id="75d00-110">Возвращает приложения-функции в подписке.</span><span class="sxs-lookup"><span data-stu-id="75d00-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="75d00-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75d00-111">EXAMPLES</span></span>

### <span data-ttu-id="75d00-112">Пример 1: получение всех приложений для всех функций.</span><span class="sxs-lookup"><span data-stu-id="75d00-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="75d00-113">Пример 2: получение приложений функций по имени.</span><span class="sxs-lookup"><span data-stu-id="75d00-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="75d00-114">Пример 3: получение приложений функций по названию группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75d00-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="75d00-115">Пример 4: получение приложений функций для заданных подписок.</span><span class="sxs-lookup"><span data-stu-id="75d00-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="75d00-116">Пример 5: получение приложений функций по местоположению.</span><span class="sxs-lookup"><span data-stu-id="75d00-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="75d00-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75d00-117">PARAMETERS</span></span>

### <span data-ttu-id="75d00-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d00-118">-DefaultProfile</span></span>
<span data-ttu-id="75d00-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75d00-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d00-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="75d00-120">-IncludeSlot</span></span>
<span data-ttu-id="75d00-121">Укажите, следует ли включать слоты развертывания в результаты.</span><span class="sxs-lookup"><span data-stu-id="75d00-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d00-122">-Location</span><span class="sxs-lookup"><span data-stu-id="75d00-122">-Location</span></span>
<span data-ttu-id="75d00-123">Расположение приложения "функция".</span><span class="sxs-lookup"><span data-stu-id="75d00-123">The location of the function app.</span></span>

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

### <span data-ttu-id="75d00-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75d00-124">-Name</span></span>
<span data-ttu-id="75d00-125">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="75d00-125">The name of the function app.</span></span>

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

### <span data-ttu-id="75d00-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d00-126">-ResourceGroupName</span></span>
<span data-ttu-id="75d00-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75d00-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="75d00-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75d00-128">-SubscriptionId</span></span>
<span data-ttu-id="75d00-129">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="75d00-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="75d00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d00-130">CommonParameters</span></span>
<span data-ttu-id="75d00-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75d00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d00-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75d00-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d00-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75d00-133">INPUTS</span></span>

## <span data-ttu-id="75d00-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75d00-134">OUTPUTS</span></span>

### <span data-ttu-id="75d00-135">Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="75d00-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="75d00-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="75d00-136">NOTES</span></span>

<span data-ttu-id="75d00-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="75d00-137">ALIASES</span></span>

## <span data-ttu-id="75d00-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75d00-138">RELATED LINKS</span></span>

