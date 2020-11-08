---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 047ede26246c31b17fbeb49fca4353b2cb17594c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078315"
---
# <span data-ttu-id="1c1d6-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="1c1d6-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="1c1d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1d6-103">Отправить пользователю сообщение.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-103">Send a message to a user.</span></span>

## <span data-ttu-id="1c1d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c1d6-104">SYNTAX</span></span>

### <span data-ttu-id="1c1d6-105">SendExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c1d6-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c1d6-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1c1d6-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c1d6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c1d6-107">DESCRIPTION</span></span>
<span data-ttu-id="1c1d6-108">Отправить пользователю сообщение.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-108">Send a message to a user.</span></span>

## <span data-ttu-id="1c1d6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c1d6-109">EXAMPLES</span></span>

### <span data-ttu-id="1c1d6-110">Пример 1: Отправка сообщения в UserSession</span><span class="sxs-lookup"><span data-stu-id="1c1d6-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="1c1d6-111">Эта команда отправляет сообщение в UserSession.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="1c1d6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c1d6-112">PARAMETERS</span></span>

### <span data-ttu-id="1c1d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c1d6-113">-DefaultProfile</span></span>
<span data-ttu-id="1c1d6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c1d6-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="1c1d6-115">-HostPoolName</span></span>
<span data-ttu-id="1c1d6-116">Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1d6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c1d6-117">-InputObject</span></span>
<span data-ttu-id="1c1d6-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1d6-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="1c1d6-119">-MessageBody</span></span>
<span data-ttu-id="1c1d6-120">Текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-120">Body of message.</span></span>

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

### <span data-ttu-id="1c1d6-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="1c1d6-121">-MessageTitle</span></span>
<span data-ttu-id="1c1d6-122">Заголовок сообщения.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-122">Title of message.</span></span>

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

### <span data-ttu-id="1c1d6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c1d6-123">-PassThru</span></span>
<span data-ttu-id="1c1d6-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1c1d6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c1d6-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c1d6-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-126">The name of the resource group.</span></span>
<span data-ttu-id="1c1d6-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1d6-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="1c1d6-128">-SessionHostName</span></span>
<span data-ttu-id="1c1d6-129">Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1d6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c1d6-130">-SubscriptionId</span></span>
<span data-ttu-id="1c1d6-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1d6-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="1c1d6-132">-UserSessionId</span></span>
<span data-ttu-id="1c1d6-133">Имя сеанса пользователя на указанном узле сеанса</span><span class="sxs-lookup"><span data-stu-id="1c1d6-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1d6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c1d6-134">-Confirm</span></span>
<span data-ttu-id="1c1d6-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c1d6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c1d6-136">-WhatIf</span></span>
<span data-ttu-id="1c1d6-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c1d6-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c1d6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1d6-139">CommonParameters</span></span>
<span data-ttu-id="1c1d6-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1d6-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c1d6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1d6-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c1d6-142">INPUTS</span></span>

### <span data-ttu-id="1c1d6-143">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="1c1d6-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1c1d6-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c1d6-144">OUTPUTS</span></span>

### <span data-ttu-id="1c1d6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c1d6-145">System.Boolean</span></span>

## <span data-ttu-id="1c1d6-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c1d6-146">NOTES</span></span>

<span data-ttu-id="1c1d6-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="1c1d6-147">ALIASES</span></span>

<span data-ttu-id="1c1d6-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1c1d6-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c1d6-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c1d6-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c1d6-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="1c1d6-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c1d6-152">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1c1d6-153">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1c1d6-154">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1c1d6-155">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1c1d6-156">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="1c1d6-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c1d6-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1c1d6-158">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="1c1d6-159">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1c1d6-160">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1c1d6-161">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="1c1d6-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1c1d6-162">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1c1d6-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1c1d6-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c1d6-163">RELATED LINKS</span></span>

