---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236747"
---
# <span data-ttu-id="6caa5-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="6caa5-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="6caa5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6caa5-102">SYNOPSIS</span></span>
<span data-ttu-id="6caa5-103">Получает рабочую область.</span><span class="sxs-lookup"><span data-stu-id="6caa5-103">Gets the workspace.</span></span>

## <span data-ttu-id="6caa5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6caa5-104">SYNTAX</span></span>

### <span data-ttu-id="6caa5-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6caa5-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6caa5-106">Получить</span><span class="sxs-lookup"><span data-stu-id="6caa5-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6caa5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6caa5-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6caa5-108">Список</span><span class="sxs-lookup"><span data-stu-id="6caa5-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6caa5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6caa5-109">DESCRIPTION</span></span>
<span data-ttu-id="6caa5-110">Получает рабочую область.</span><span class="sxs-lookup"><span data-stu-id="6caa5-110">Gets the workspace.</span></span>

## <span data-ttu-id="6caa5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6caa5-111">EXAMPLES</span></span>

### <span data-ttu-id="6caa5-112">Пример 1: получение модуля данными рабочей области с именем</span><span class="sxs-lookup"><span data-stu-id="6caa5-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="6caa5-113">Эта команда получает рабочую область модуля данные в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6caa5-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="6caa5-114">Пример 2: список всех рабочих областей "кирпичные" в подписке</span><span class="sxs-lookup"><span data-stu-id="6caa5-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="6caa5-115">Эта команда выводит список всех рабочих областей кирпичей в подписке.</span><span class="sxs-lookup"><span data-stu-id="6caa5-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="6caa5-116">Пример 3: список всех рабочих областей «кирпичные ресурсы» в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="6caa5-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="6caa5-117">Эта команда выводит список всех рабочих областей кирпичей в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6caa5-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="6caa5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6caa5-118">PARAMETERS</span></span>

### <span data-ttu-id="6caa5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6caa5-119">-DefaultProfile</span></span>
<span data-ttu-id="6caa5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6caa5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6caa5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6caa5-121">-InputObject</span></span>
<span data-ttu-id="6caa5-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="6caa5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6caa5-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6caa5-123">-Name</span></span>
<span data-ttu-id="6caa5-124">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6caa5-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="6caa5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6caa5-125">-ResourceGroupName</span></span>
<span data-ttu-id="6caa5-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6caa5-126">The name of the resource group.</span></span>
<span data-ttu-id="6caa5-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6caa5-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6caa5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6caa5-128">-SubscriptionId</span></span>
<span data-ttu-id="6caa5-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6caa5-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6caa5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6caa5-130">CommonParameters</span></span>
<span data-ttu-id="6caa5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6caa5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6caa5-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6caa5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6caa5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6caa5-133">INPUTS</span></span>

### <span data-ttu-id="6caa5-134">Microsoft. Azure. PowerShell. командлеты. кирпичи. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="6caa5-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="6caa5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6caa5-135">OUTPUTS</span></span>

### <span data-ttu-id="6caa5-136">Microsoft. Azure. PowerShell. командлеты. кирпичи. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="6caa5-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="6caa5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6caa5-137">NOTES</span></span>

<span data-ttu-id="6caa5-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="6caa5-138">ALIASES</span></span>

<span data-ttu-id="6caa5-139">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6caa5-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6caa5-140">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6caa5-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6caa5-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6caa5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6caa5-142">INPUTOBJECT <IDatabricksIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="6caa5-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6caa5-143">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="6caa5-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6caa5-144">`[PeeringName <String>]`: Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="6caa5-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="6caa5-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6caa5-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6caa5-146">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6caa5-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="6caa5-147">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6caa5-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6caa5-148">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6caa5-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="6caa5-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6caa5-149">RELATED LINKS</span></span>

