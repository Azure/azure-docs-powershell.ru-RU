---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/remove-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
ms.openlocfilehash: d35de003bd4822758fd75c7dbbcf616ebecbbccb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012552"
---
# <span data-ttu-id="483ad-101">Remove-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="483ad-101">Remove-AzConfluentOrganization</span></span>

## <span data-ttu-id="483ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483ad-102">SYNOPSIS</span></span>
<span data-ttu-id="483ad-103">Удаление ресурса организации</span><span class="sxs-lookup"><span data-stu-id="483ad-103">Delete Organization resource</span></span>

## <span data-ttu-id="483ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="483ad-104">SYNTAX</span></span>

### <span data-ttu-id="483ad-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="483ad-105">Delete (Default)</span></span>
```
Remove-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="483ad-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="483ad-106">DeleteViaIdentity</span></span>
```
Remove-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="483ad-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="483ad-107">DESCRIPTION</span></span>
<span data-ttu-id="483ad-108">Удаление ресурса организации</span><span class="sxs-lookup"><span data-stu-id="483ad-108">Delete Organization resource</span></span>

## <span data-ttu-id="483ad-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="483ad-109">EXAMPLES</span></span>

### <span data-ttu-id="483ad-110">Пример 1. Удаление организации по имени</span><span class="sxs-lookup"><span data-stu-id="483ad-110">Example 1: Remove a confluent organization by name</span></span>
```powershell
PS C:\> Remove-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

```

<span data-ttu-id="483ad-111">Эта команда удаляет организацию по имени</span><span class="sxs-lookup"><span data-stu-id="483ad-111">This command removes a confluent organization by name</span></span>

### <span data-ttu-id="483ad-112">Пример 2. Удаление организации через канал</span><span class="sxs-lookup"><span data-stu-id="483ad-112">Example 2: Remove a confluent organization by pipeline</span></span>
```powershell
PS C:\>  Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Remove-AzConfluentOrganization

```

<span data-ttu-id="483ad-113">Эта команда удаляет организацию через канал.</span><span class="sxs-lookup"><span data-stu-id="483ad-113">This command removes a confluent organization by pipeline.</span></span>

## <span data-ttu-id="483ad-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="483ad-114">PARAMETERS</span></span>

### <span data-ttu-id="483ad-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="483ad-115">-AsJob</span></span>
<span data-ttu-id="483ad-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="483ad-116">Run the command as a job</span></span>

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

### <span data-ttu-id="483ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483ad-117">-DefaultProfile</span></span>
<span data-ttu-id="483ad-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="483ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="483ad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="483ad-119">-InputObject</span></span>
<span data-ttu-id="483ad-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="483ad-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="483ad-121">-Name</span><span class="sxs-lookup"><span data-stu-id="483ad-121">-Name</span></span>
<span data-ttu-id="483ad-122">Название ресурса организации</span><span class="sxs-lookup"><span data-stu-id="483ad-122">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="483ad-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="483ad-123">-NoWait</span></span>
<span data-ttu-id="483ad-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="483ad-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="483ad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="483ad-125">-PassThru</span></span>
<span data-ttu-id="483ad-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="483ad-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="483ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="483ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="483ad-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="483ad-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="483ad-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="483ad-129">-SubscriptionId</span></span>
<span data-ttu-id="483ad-130">ИД подписки Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="483ad-130">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="483ad-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="483ad-131">-Confirm</span></span>
<span data-ttu-id="483ad-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="483ad-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="483ad-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483ad-133">-WhatIf</span></span>
<span data-ttu-id="483ad-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="483ad-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="483ad-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="483ad-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="483ad-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483ad-136">CommonParameters</span></span>
<span data-ttu-id="483ad-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483ad-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483ad-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="483ad-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483ad-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="483ad-139">INPUTS</span></span>

### <span data-ttu-id="483ad-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="483ad-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="483ad-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="483ad-141">OUTPUTS</span></span>

### <span data-ttu-id="483ad-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="483ad-142">System.Boolean</span></span>

## <span data-ttu-id="483ad-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="483ad-143">NOTES</span></span>

<span data-ttu-id="483ad-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="483ad-144">ALIASES</span></span>

<span data-ttu-id="483ad-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="483ad-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="483ad-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="483ad-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="483ad-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="483ad-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="483ad-148">INPUTOBJECT <IConfluentIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="483ad-148">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="483ad-149">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="483ad-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="483ad-150">`[OrganizationName <String>]`: название ресурса организации</span><span class="sxs-lookup"><span data-stu-id="483ad-150">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="483ad-151">`[ResourceGroupName <String>]`: название группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="483ad-151">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="483ad-152">`[SubscriptionId <String>]`: ИД подписки Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="483ad-152">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="483ad-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="483ad-153">RELATED LINKS</span></span>

