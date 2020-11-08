---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: ab1f338be9d983efceac0045fec96b1a63fb66bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079659"
---
# <span data-ttu-id="7e566-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="7e566-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="7e566-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e566-102">SYNOPSIS</span></span>
<span data-ttu-id="7e566-103">Обновление applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="7e566-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="7e566-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e566-104">SYNTAX</span></span>

### <span data-ttu-id="7e566-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e566-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7e566-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7e566-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7e566-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e566-107">DESCRIPTION</span></span>
<span data-ttu-id="7e566-108">Обновление applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="7e566-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="7e566-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e566-109">EXAMPLES</span></span>

### <span data-ttu-id="7e566-110">Пример 1: создание виртуального рабочего стола Windows ApplicationGroup по имени</span><span class="sxs-lookup"><span data-stu-id="7e566-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="7e566-111">Эта команда создает ApplicationGroup виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e566-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="7e566-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e566-112">PARAMETERS</span></span>

### <span data-ttu-id="7e566-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e566-113">-DefaultProfile</span></span>
<span data-ttu-id="7e566-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e566-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e566-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="7e566-115">-Description</span></span>
<span data-ttu-id="7e566-116">Описание ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="7e566-116">Description of ApplicationGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e566-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7e566-117">-FriendlyName</span></span>
<span data-ttu-id="7e566-118">Понятное имя ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="7e566-118">Friendly name of ApplicationGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e566-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e566-119">-InputObject</span></span>
<span data-ttu-id="7e566-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7e566-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e566-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e566-121">-Name</span></span>
<span data-ttu-id="7e566-122">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="7e566-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e566-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e566-123">-ResourceGroupName</span></span>
<span data-ttu-id="7e566-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e566-124">The name of the resource group.</span></span>
<span data-ttu-id="7e566-125">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="7e566-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e566-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e566-126">-SubscriptionId</span></span>
<span data-ttu-id="7e566-127">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="7e566-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e566-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="7e566-128">-Tag</span></span>
<span data-ttu-id="7e566-129">Теги для обновления</span><span class="sxs-lookup"><span data-stu-id="7e566-129">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e566-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e566-130">-Confirm</span></span>
<span data-ttu-id="7e566-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e566-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e566-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e566-132">-WhatIf</span></span>
<span data-ttu-id="7e566-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e566-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e566-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e566-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e566-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e566-135">CommonParameters</span></span>
<span data-ttu-id="7e566-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e566-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e566-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e566-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e566-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e566-138">INPUTS</span></span>

### <span data-ttu-id="7e566-139">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="7e566-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="7e566-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e566-140">OUTPUTS</span></span>

### <span data-ttu-id="7e566-141">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="7e566-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="7e566-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e566-142">NOTES</span></span>

<span data-ttu-id="7e566-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="7e566-143">ALIASES</span></span>

<span data-ttu-id="7e566-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7e566-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7e566-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7e566-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7e566-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7e566-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7e566-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="7e566-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7e566-148">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="7e566-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="7e566-149">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="7e566-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="7e566-150">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="7e566-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="7e566-151">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e566-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="7e566-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="7e566-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7e566-153">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e566-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7e566-154">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="7e566-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="7e566-155">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="7e566-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="7e566-156">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="7e566-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7e566-157">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="7e566-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="7e566-158">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7e566-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="7e566-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e566-159">RELATED LINKS</span></span>

