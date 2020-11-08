---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080005"
---
# <span data-ttu-id="99f8f-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="99f8f-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="99f8f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="99f8f-103">Получение сведений о представлении модели или представлении экземпляра гибридного компьютера.</span><span class="sxs-lookup"><span data-stu-id="99f8f-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="99f8f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99f8f-104">SYNTAX</span></span>

### <span data-ttu-id="99f8f-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99f8f-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="99f8f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="99f8f-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="99f8f-107">Список</span><span class="sxs-lookup"><span data-stu-id="99f8f-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="99f8f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99f8f-108">DESCRIPTION</span></span>
<span data-ttu-id="99f8f-109">Получение сведений о представлении модели или представлении экземпляра гибридного компьютера.</span><span class="sxs-lookup"><span data-stu-id="99f8f-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="99f8f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99f8f-110">EXAMPLES</span></span>

### <span data-ttu-id="99f8f-111">Пример 1: список всех подключенных машин в подписке</span><span class="sxs-lookup"><span data-stu-id="99f8f-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="99f8f-112">Список всех подключенных компьютеров в подписке.</span><span class="sxs-lookup"><span data-stu-id="99f8f-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="99f8f-113">Если подписка не указана, она будет использовать подписку из текущего контекста Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99f8f-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="99f8f-114">Пример 2: список всех подключенных машин в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="99f8f-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="99f8f-115">Перечислите все подключенные машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99f8f-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="99f8f-116">Пример 3: получение имени подключенного компьютера в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="99f8f-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="99f8f-117">Получение имени подключенного компьютера в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99f8f-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="99f8f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99f8f-118">PARAMETERS</span></span>

### <span data-ttu-id="99f8f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f8f-119">-DefaultProfile</span></span>
<span data-ttu-id="99f8f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99f8f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f8f-121">-Expand</span><span class="sxs-lookup"><span data-stu-id="99f8f-121">-Expand</span></span>
<span data-ttu-id="99f8f-122">Выражение развертывания, применяемое к операции.</span><span class="sxs-lookup"><span data-stu-id="99f8f-122">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="99f8f-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99f8f-123">-Name</span></span>
<span data-ttu-id="99f8f-124">Имя гибридного компьютера.</span><span class="sxs-lookup"><span data-stu-id="99f8f-124">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="99f8f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f8f-125">-ResourceGroupName</span></span>
<span data-ttu-id="99f8f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99f8f-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="99f8f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99f8f-127">-SubscriptionId</span></span>
<span data-ttu-id="99f8f-128">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99f8f-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="99f8f-129">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="99f8f-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="99f8f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f8f-130">CommonParameters</span></span>
<span data-ttu-id="99f8f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99f8f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f8f-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99f8f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f8f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99f8f-133">INPUTS</span></span>

## <span data-ttu-id="99f8f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99f8f-134">OUTPUTS</span></span>

### <span data-ttu-id="99f8f-135">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. Api20200802. IMachine</span><span class="sxs-lookup"><span data-stu-id="99f8f-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="99f8f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="99f8f-136">NOTES</span></span>

<span data-ttu-id="99f8f-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="99f8f-137">ALIASES</span></span>

## <span data-ttu-id="99f8f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99f8f-138">RELATED LINKS</span></span>
