---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415807"
---
# <span data-ttu-id="0a8c5-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a8c5-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="0a8c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a8c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8c5-103">Возвращает рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-103">Gets the workspace.</span></span>

## <span data-ttu-id="0a8c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a8c5-104">SYNTAX</span></span>

### <span data-ttu-id="0a8c5-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a8c5-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a8c5-106">Получить</span><span class="sxs-lookup"><span data-stu-id="0a8c5-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a8c5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0a8c5-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a8c5-108">Список</span><span class="sxs-lookup"><span data-stu-id="0a8c5-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0a8c5-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a8c5-109">DESCRIPTION</span></span>
<span data-ttu-id="0a8c5-110">Возвращает рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-110">Gets the workspace.</span></span>

## <span data-ttu-id="0a8c5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a8c5-111">EXAMPLES</span></span>

### <span data-ttu-id="0a8c5-112">Пример 1. Получить рабочее пространство datab в имени</span><span class="sxs-lookup"><span data-stu-id="0a8c5-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="0a8c5-113">Эта команда получает рабочее пространство Datab в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="0a8c5-114">Пример 2. Список всех бизнес-области в подписке</span><span class="sxs-lookup"><span data-stu-id="0a8c5-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="0a8c5-115">Эта команда содержит список всех рабочей области Datab действой в подписке.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="0a8c5-116">Пример 3. Список всех ветвей данных в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="0a8c5-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="0a8c5-117">Эта команда содержит список всех ветвей данных в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="0a8c5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a8c5-118">PARAMETERS</span></span>

### <span data-ttu-id="0a8c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8c5-119">-DefaultProfile</span></span>
<span data-ttu-id="0a8c5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a8c5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a8c5-121">-InputObject</span></span>
<span data-ttu-id="0a8c5-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0a8c5-123">-Name</span></span>
<span data-ttu-id="0a8c5-124">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a8c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a8c5-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-126">The name of the resource group.</span></span>
<span data-ttu-id="0a8c5-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0a8c5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a8c5-128">-SubscriptionId</span></span>
<span data-ttu-id="0a8c5-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8c5-130">CommonParameters</span></span>
<span data-ttu-id="0a8c5-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8c5-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a8c5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8c5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a8c5-133">INPUTS</span></span>

### <span data-ttu-id="0a8c5-134">Microsoft.Azure.PowerShell.Cmdlets.Datab ветвей.Models.IDatabоsIdentity</span><span class="sxs-lookup"><span data-stu-id="0a8c5-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="0a8c5-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a8c5-135">OUTPUTS</span></span>

### <span data-ttu-id="0a8c5-136">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a8c5-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="0a8c5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a8c5-137">NOTES</span></span>

<span data-ttu-id="0a8c5-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0a8c5-138">ALIASES</span></span>

<span data-ttu-id="0a8c5-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0a8c5-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a8c5-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a8c5-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a8c5-142">INPUTOBJECT <IDatabricksIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="0a8c5-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a8c5-143">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="0a8c5-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a8c5-144">`[PeeringName <String>]`: имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="0a8c5-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0a8c5-146">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="0a8c5-147">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0a8c5-148">`[WorkspaceName <String>]`: название рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="0a8c5-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a8c5-149">RELATED LINKS</span></span>

