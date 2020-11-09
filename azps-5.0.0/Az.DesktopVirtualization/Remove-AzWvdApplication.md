---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c2604531014283b3599adb94c4a12d70761e1533
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312509"
---
# <span data-ttu-id="306da-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="306da-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="306da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="306da-102">SYNOPSIS</span></span>
<span data-ttu-id="306da-103">Удаление приложения.</span><span class="sxs-lookup"><span data-stu-id="306da-103">Remove an application.</span></span>

## <span data-ttu-id="306da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="306da-104">SYNTAX</span></span>

### <span data-ttu-id="306da-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="306da-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="306da-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="306da-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="306da-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="306da-107">DESCRIPTION</span></span>
<span data-ttu-id="306da-108">Удаление приложения.</span><span class="sxs-lookup"><span data-stu-id="306da-108">Remove an application.</span></span>

## <span data-ttu-id="306da-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="306da-109">EXAMPLES</span></span>

### <span data-ttu-id="306da-110">Пример 1: Удаление приложения виртуальных рабочих столов Windows по имени</span><span class="sxs-lookup"><span data-stu-id="306da-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="306da-111">Эта команда удаляет приложение виртуальных рабочих столов Windows в группе applicaton.</span><span class="sxs-lookup"><span data-stu-id="306da-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="306da-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="306da-112">PARAMETERS</span></span>

### <span data-ttu-id="306da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="306da-113">-DefaultProfile</span></span>
<span data-ttu-id="306da-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="306da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="306da-115">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="306da-115">-GroupName</span></span>
<span data-ttu-id="306da-116">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="306da-116">The name of the application group</span></span>

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

### <span data-ttu-id="306da-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="306da-117">-InputObject</span></span>
<span data-ttu-id="306da-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="306da-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="306da-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="306da-119">-Name</span></span>
<span data-ttu-id="306da-120">Имя приложения в заданной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="306da-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="306da-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="306da-121">-PassThru</span></span>
<span data-ttu-id="306da-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="306da-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="306da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="306da-123">-ResourceGroupName</span></span>
<span data-ttu-id="306da-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="306da-124">The name of the resource group.</span></span>
<span data-ttu-id="306da-125">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="306da-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="306da-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="306da-126">-SubscriptionId</span></span>
<span data-ttu-id="306da-127">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="306da-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="306da-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="306da-128">-Confirm</span></span>
<span data-ttu-id="306da-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="306da-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="306da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="306da-130">-WhatIf</span></span>
<span data-ttu-id="306da-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="306da-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="306da-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="306da-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="306da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="306da-133">CommonParameters</span></span>
<span data-ttu-id="306da-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="306da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="306da-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="306da-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="306da-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="306da-136">INPUTS</span></span>

### <span data-ttu-id="306da-137">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="306da-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="306da-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="306da-138">OUTPUTS</span></span>

### <span data-ttu-id="306da-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="306da-139">System.Boolean</span></span>

## <span data-ttu-id="306da-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="306da-140">NOTES</span></span>

<span data-ttu-id="306da-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="306da-141">ALIASES</span></span>

<span data-ttu-id="306da-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="306da-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="306da-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="306da-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="306da-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="306da-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="306da-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="306da-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="306da-146">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="306da-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="306da-147">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="306da-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="306da-148">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="306da-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="306da-149">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="306da-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="306da-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="306da-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="306da-151">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="306da-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="306da-152">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="306da-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="306da-153">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="306da-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="306da-154">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="306da-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="306da-155">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="306da-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="306da-156">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="306da-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="306da-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="306da-157">RELATED LINKS</span></span>

