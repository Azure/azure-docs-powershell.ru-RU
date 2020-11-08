---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 6c885f4962734bf1034256843258f4755a9b3b44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245007"
---
# <span data-ttu-id="aa353-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="aa353-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="aa353-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa353-102">SYNOPSIS</span></span>
<span data-ttu-id="aa353-103">Удаление applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="aa353-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="aa353-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa353-104">SYNTAX</span></span>

### <span data-ttu-id="aa353-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa353-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aa353-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa353-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa353-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa353-107">DESCRIPTION</span></span>
<span data-ttu-id="aa353-108">Удаление applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="aa353-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="aa353-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa353-109">EXAMPLES</span></span>

### <span data-ttu-id="aa353-110">Пример 1: Удаление виртуального рабочего стола Windows ApplicationGroup по имени</span><span class="sxs-lookup"><span data-stu-id="aa353-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="aa353-111">Эта команда удаляет ApplicationGroup виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa353-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="aa353-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa353-112">PARAMETERS</span></span>

### <span data-ttu-id="aa353-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa353-113">-DefaultProfile</span></span>
<span data-ttu-id="aa353-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa353-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa353-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa353-115">-InputObject</span></span>
<span data-ttu-id="aa353-116">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="aa353-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa353-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa353-117">-Name</span></span>
<span data-ttu-id="aa353-118">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="aa353-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa353-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa353-119">-PassThru</span></span>
<span data-ttu-id="aa353-120">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aa353-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aa353-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa353-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa353-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa353-122">The name of the resource group.</span></span>
<span data-ttu-id="aa353-123">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="aa353-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="aa353-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa353-124">-SubscriptionId</span></span>
<span data-ttu-id="aa353-125">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="aa353-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="aa353-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa353-126">-Confirm</span></span>
<span data-ttu-id="aa353-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa353-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa353-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa353-128">-WhatIf</span></span>
<span data-ttu-id="aa353-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa353-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa353-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa353-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa353-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa353-131">CommonParameters</span></span>
<span data-ttu-id="aa353-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa353-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa353-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa353-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa353-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa353-134">INPUTS</span></span>

### <span data-ttu-id="aa353-135">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="aa353-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="aa353-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa353-136">OUTPUTS</span></span>

### <span data-ttu-id="aa353-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa353-137">System.Boolean</span></span>

## <span data-ttu-id="aa353-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa353-138">NOTES</span></span>

<span data-ttu-id="aa353-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="aa353-139">ALIASES</span></span>

<span data-ttu-id="aa353-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="aa353-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa353-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="aa353-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa353-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aa353-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa353-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="aa353-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa353-144">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="aa353-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="aa353-145">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="aa353-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="aa353-146">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="aa353-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="aa353-147">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa353-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="aa353-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="aa353-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa353-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa353-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aa353-150">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="aa353-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="aa353-151">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="aa353-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="aa353-152">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="aa353-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="aa353-153">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="aa353-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="aa353-154">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="aa353-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="aa353-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa353-155">RELATED LINKS</span></span>

