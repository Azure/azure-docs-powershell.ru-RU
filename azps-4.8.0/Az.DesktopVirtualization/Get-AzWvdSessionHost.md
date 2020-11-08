---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079670"
---
# <span data-ttu-id="cf078-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="cf078-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="cf078-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf078-102">SYNOPSIS</span></span>
<span data-ttu-id="cf078-103">Получение узла сеансов.</span><span class="sxs-lookup"><span data-stu-id="cf078-103">Get a session host.</span></span>

## <span data-ttu-id="cf078-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf078-104">SYNTAX</span></span>

### <span data-ttu-id="cf078-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf078-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cf078-106">Получить</span><span class="sxs-lookup"><span data-stu-id="cf078-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cf078-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf078-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf078-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf078-108">DESCRIPTION</span></span>
<span data-ttu-id="cf078-109">Получение узла сеансов.</span><span class="sxs-lookup"><span data-stu-id="cf078-109">Get a session host.</span></span>

## <span data-ttu-id="cf078-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf078-110">EXAMPLES</span></span>

### <span data-ttu-id="cf078-111">Пример 1: получение виртуального рабочего стола Windows SessionHost по имени</span><span class="sxs-lookup"><span data-stu-id="cf078-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="cf078-112">Эта команда получает SessionHost виртуальных рабочих столов Windows в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="cf078-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="cf078-113">Пример 2: список виртуальных рабочих столов Windows SessionHosts</span><span class="sxs-lookup"><span data-stu-id="cf078-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="cf078-114">Эта команда перечисляет SessionHosts виртуальных рабочих столов Windows в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="cf078-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="cf078-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf078-115">PARAMETERS</span></span>

### <span data-ttu-id="cf078-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf078-116">-DefaultProfile</span></span>
<span data-ttu-id="cf078-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf078-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf078-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="cf078-118">-HostPoolName</span></span>
<span data-ttu-id="cf078-119">Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf078-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="cf078-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf078-120">-InputObject</span></span>
<span data-ttu-id="cf078-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="cf078-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf078-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf078-122">-Name</span></span>
<span data-ttu-id="cf078-123">Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="cf078-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf078-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf078-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf078-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf078-125">The name of the resource group.</span></span>
<span data-ttu-id="cf078-126">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="cf078-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cf078-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf078-127">-SubscriptionId</span></span>
<span data-ttu-id="cf078-128">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="cf078-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf078-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf078-129">CommonParameters</span></span>
<span data-ttu-id="cf078-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf078-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf078-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf078-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf078-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf078-132">INPUTS</span></span>

### <span data-ttu-id="cf078-133">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cf078-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cf078-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf078-134">OUTPUTS</span></span>

### <span data-ttu-id="cf078-135">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="cf078-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="cf078-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf078-136">NOTES</span></span>

<span data-ttu-id="cf078-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="cf078-137">ALIASES</span></span>

<span data-ttu-id="cf078-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cf078-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf078-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf078-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf078-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf078-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf078-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="cf078-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf078-142">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="cf078-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cf078-143">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="cf078-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cf078-144">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="cf078-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cf078-145">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf078-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cf078-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="cf078-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf078-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf078-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cf078-148">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="cf078-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="cf078-149">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="cf078-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cf078-150">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="cf078-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cf078-151">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="cf078-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cf078-152">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cf078-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cf078-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf078-153">RELATED LINKS</span></span>

