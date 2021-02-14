---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243989"
---
# <span data-ttu-id="91fa4-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="91fa4-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="91fa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="91fa4-103">Операция получения расширения.</span><span class="sxs-lookup"><span data-stu-id="91fa4-103">The operation to get the extension.</span></span>

## <span data-ttu-id="91fa4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91fa4-104">SYNTAX</span></span>

### <span data-ttu-id="91fa4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91fa4-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91fa4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="91fa4-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="91fa4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91fa4-107">DESCRIPTION</span></span>
<span data-ttu-id="91fa4-108">Операция получения расширения.</span><span class="sxs-lookup"><span data-stu-id="91fa4-108">The operation to get the extension.</span></span>

## <span data-ttu-id="91fa4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91fa4-109">EXAMPLES</span></span>

### <span data-ttu-id="91fa4-110">Пример 1. Список всех расширений для компьютера</span><span class="sxs-lookup"><span data-stu-id="91fa4-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="91fa4-111">Список всех расширений для определенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="91fa4-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="91fa4-112">Пример 2. Получить определенное расширение на компьютере</span><span class="sxs-lookup"><span data-stu-id="91fa4-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="91fa4-113">Получает определенное расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="91fa4-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="91fa4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91fa4-114">PARAMETERS</span></span>

### <span data-ttu-id="91fa4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91fa4-115">-DefaultProfile</span></span>
<span data-ttu-id="91fa4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91fa4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91fa4-117">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="91fa4-117">-Expand</span></span>
<span data-ttu-id="91fa4-118">Выражение для расширения, применяемая к операции.</span><span class="sxs-lookup"><span data-stu-id="91fa4-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="91fa4-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="91fa4-119">-MachineName</span></span>
<span data-ttu-id="91fa4-120">Имя компьютера, содержащего расширение.</span><span class="sxs-lookup"><span data-stu-id="91fa4-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="91fa4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="91fa4-121">-Name</span></span>
<span data-ttu-id="91fa4-122">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="91fa4-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="91fa4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91fa4-123">-ResourceGroupName</span></span>
<span data-ttu-id="91fa4-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91fa4-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="91fa4-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91fa4-125">-SubscriptionId</span></span>
<span data-ttu-id="91fa4-126">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="91fa4-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="91fa4-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="91fa4-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="91fa4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91fa4-128">CommonParameters</span></span>
<span data-ttu-id="91fa4-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91fa4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91fa4-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91fa4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91fa4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91fa4-131">INPUTS</span></span>

## <span data-ttu-id="91fa4-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91fa4-132">OUTPUTS</span></span>

### <span data-ttu-id="91fa4-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="91fa4-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="91fa4-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91fa4-134">NOTES</span></span>

<span data-ttu-id="91fa4-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="91fa4-135">ALIASES</span></span>

## <span data-ttu-id="91fa4-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91fa4-136">RELATED LINKS</span></span>

