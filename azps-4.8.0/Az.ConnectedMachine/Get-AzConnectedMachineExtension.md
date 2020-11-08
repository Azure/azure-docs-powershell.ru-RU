---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243391"
---
# <span data-ttu-id="06e4b-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="06e4b-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="06e4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="06e4b-103">Операция, позволяющая получить расширение.</span><span class="sxs-lookup"><span data-stu-id="06e4b-103">The operation to get the extension.</span></span>

## <span data-ttu-id="06e4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06e4b-104">SYNTAX</span></span>

### <span data-ttu-id="06e4b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06e4b-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="06e4b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="06e4b-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="06e4b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06e4b-107">DESCRIPTION</span></span>
<span data-ttu-id="06e4b-108">Операция, позволяющая получить расширение.</span><span class="sxs-lookup"><span data-stu-id="06e4b-108">The operation to get the extension.</span></span>

## <span data-ttu-id="06e4b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06e4b-109">EXAMPLES</span></span>

### <span data-ttu-id="06e4b-110">Пример 1: список всех расширений для компьютера</span><span class="sxs-lookup"><span data-stu-id="06e4b-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="06e4b-111">Список всех расширений для определенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="06e4b-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="06e4b-112">Пример 2: получение определенного расширения на компьютере</span><span class="sxs-lookup"><span data-stu-id="06e4b-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="06e4b-113">Возвращает определенное расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="06e4b-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="06e4b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06e4b-114">PARAMETERS</span></span>

### <span data-ttu-id="06e4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e4b-115">-DefaultProfile</span></span>
<span data-ttu-id="06e4b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06e4b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e4b-117">-Expand</span><span class="sxs-lookup"><span data-stu-id="06e4b-117">-Expand</span></span>
<span data-ttu-id="06e4b-118">Выражение развертывания, применяемое к операции.</span><span class="sxs-lookup"><span data-stu-id="06e4b-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e4b-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="06e4b-119">-MachineName</span></span>
<span data-ttu-id="06e4b-120">Имя компьютера, содержащего расширение.</span><span class="sxs-lookup"><span data-stu-id="06e4b-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="06e4b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06e4b-121">-Name</span></span>
<span data-ttu-id="06e4b-122">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="06e4b-122">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="06e4b-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06e4b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="06e4b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06e4b-125">-SubscriptionId</span></span>
<span data-ttu-id="06e4b-126">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="06e4b-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06e4b-127">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="06e4b-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="06e4b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e4b-128">CommonParameters</span></span>
<span data-ttu-id="06e4b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06e4b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e4b-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06e4b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e4b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06e4b-131">INPUTS</span></span>

## <span data-ttu-id="06e4b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06e4b-132">OUTPUTS</span></span>

### <span data-ttu-id="06e4b-133">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="06e4b-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="06e4b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="06e4b-134">NOTES</span></span>

<span data-ttu-id="06e4b-135">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="06e4b-135">ALIASES</span></span>

## <span data-ttu-id="06e4b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06e4b-136">RELATED LINKS</span></span>

