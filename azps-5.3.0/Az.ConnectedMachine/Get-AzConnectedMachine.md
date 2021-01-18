---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519416"
---
# <span data-ttu-id="026de-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="026de-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="026de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="026de-102">SYNOPSIS</span></span>
<span data-ttu-id="026de-103">Извлекает сведения о представлении модели или экземпляре гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="026de-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="026de-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="026de-104">SYNTAX</span></span>

### <span data-ttu-id="026de-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="026de-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="026de-106">Получить</span><span class="sxs-lookup"><span data-stu-id="026de-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="026de-107">Список</span><span class="sxs-lookup"><span data-stu-id="026de-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="026de-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="026de-108">DESCRIPTION</span></span>
<span data-ttu-id="026de-109">Извлекает сведения о представлении модели или экземпляре гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="026de-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="026de-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="026de-110">EXAMPLES</span></span>

### <span data-ttu-id="026de-111">Пример 1. Список всех подключенных компьютеров в подписке</span><span class="sxs-lookup"><span data-stu-id="026de-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="026de-112">Список всех подключенных компьютеров в подписке.</span><span class="sxs-lookup"><span data-stu-id="026de-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="026de-113">Если подписка не указана, она будет использовать ее из контекста Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="026de-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="026de-114">Пример 2. Список всех подключенных компьютеров в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="026de-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="026de-115">Перечислить все подключенные компьютеры в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="026de-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="026de-116">Пример 3. Подключение компьютера к группе ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="026de-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="026de-117">Получить подключенный компьютер в группе ресурсов по имени.</span><span class="sxs-lookup"><span data-stu-id="026de-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="026de-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="026de-118">PARAMETERS</span></span>

### <span data-ttu-id="026de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="026de-119">-DefaultProfile</span></span>
<span data-ttu-id="026de-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="026de-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="026de-121">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="026de-121">-Expand</span></span>
<span data-ttu-id="026de-122">Выражение для расширения, применяемая к операции.</span><span class="sxs-lookup"><span data-stu-id="026de-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="026de-123">-Name</span><span class="sxs-lookup"><span data-stu-id="026de-123">-Name</span></span>
<span data-ttu-id="026de-124">Имя гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="026de-124">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="026de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="026de-125">-ResourceGroupName</span></span>
<span data-ttu-id="026de-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="026de-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="026de-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="026de-127">-SubscriptionId</span></span>
<span data-ttu-id="026de-128">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="026de-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="026de-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="026de-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="026de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="026de-130">CommonParameters</span></span>
<span data-ttu-id="026de-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="026de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="026de-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="026de-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="026de-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="026de-133">INPUTS</span></span>

## <span data-ttu-id="026de-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="026de-134">OUTPUTS</span></span>

### <span data-ttu-id="026de-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelse</span><span class="sxs-lookup"><span data-stu-id="026de-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="026de-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="026de-136">NOTES</span></span>

<span data-ttu-id="026de-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="026de-137">ALIASES</span></span>

## <span data-ttu-id="026de-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="026de-138">RELATED LINKS</span></span>

