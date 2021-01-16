---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508974"
---
# <span data-ttu-id="713ca-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="713ca-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="713ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="713ca-102">SYNOPSIS</span></span>
<span data-ttu-id="713ca-103">Операция получения расширения.</span><span class="sxs-lookup"><span data-stu-id="713ca-103">The operation to get the extension.</span></span>

## <span data-ttu-id="713ca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="713ca-104">SYNTAX</span></span>

### <span data-ttu-id="713ca-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="713ca-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="713ca-106">Получить</span><span class="sxs-lookup"><span data-stu-id="713ca-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="713ca-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="713ca-107">DESCRIPTION</span></span>
<span data-ttu-id="713ca-108">Операция получения расширения.</span><span class="sxs-lookup"><span data-stu-id="713ca-108">The operation to get the extension.</span></span>

## <span data-ttu-id="713ca-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="713ca-109">EXAMPLES</span></span>

### <span data-ttu-id="713ca-110">Пример 1. Список всех расширений для компьютера</span><span class="sxs-lookup"><span data-stu-id="713ca-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="713ca-111">Список всех расширений для определенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="713ca-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="713ca-112">Пример 2. Получить определенное расширение на компьютере</span><span class="sxs-lookup"><span data-stu-id="713ca-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="713ca-113">Получает определенное расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="713ca-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="713ca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="713ca-114">PARAMETERS</span></span>

### <span data-ttu-id="713ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="713ca-115">-DefaultProfile</span></span>
<span data-ttu-id="713ca-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="713ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="713ca-117">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="713ca-117">-Expand</span></span>
<span data-ttu-id="713ca-118">Выражение для расширения, применяемая к операции.</span><span class="sxs-lookup"><span data-stu-id="713ca-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="713ca-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="713ca-119">-MachineName</span></span>
<span data-ttu-id="713ca-120">Имя компьютера, содержащего расширение.</span><span class="sxs-lookup"><span data-stu-id="713ca-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="713ca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="713ca-121">-Name</span></span>
<span data-ttu-id="713ca-122">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="713ca-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="713ca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="713ca-123">-ResourceGroupName</span></span>
<span data-ttu-id="713ca-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="713ca-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="713ca-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="713ca-125">-SubscriptionId</span></span>
<span data-ttu-id="713ca-126">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="713ca-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="713ca-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="713ca-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="713ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="713ca-128">CommonParameters</span></span>
<span data-ttu-id="713ca-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="713ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="713ca-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="713ca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="713ca-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="713ca-131">INPUTS</span></span>

## <span data-ttu-id="713ca-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="713ca-132">OUTPUTS</span></span>

### <span data-ttu-id="713ca-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="713ca-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="713ca-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="713ca-134">NOTES</span></span>

<span data-ttu-id="713ca-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="713ca-135">ALIASES</span></span>

## <span data-ttu-id="713ca-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="713ca-136">RELATED LINKS</span></span>

