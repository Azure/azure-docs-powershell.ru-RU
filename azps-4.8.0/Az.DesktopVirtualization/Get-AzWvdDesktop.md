---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079671"
---
# <span data-ttu-id="0f16e-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="0f16e-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="0f16e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f16e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f16e-103">Получение рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0f16e-103">Get a desktop.</span></span>

## <span data-ttu-id="0f16e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f16e-104">SYNTAX</span></span>

### <span data-ttu-id="0f16e-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f16e-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f16e-106">Получить</span><span class="sxs-lookup"><span data-stu-id="0f16e-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f16e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0f16e-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f16e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f16e-108">DESCRIPTION</span></span>
<span data-ttu-id="0f16e-109">Получение рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0f16e-109">Get a desktop.</span></span>

## <span data-ttu-id="0f16e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f16e-110">EXAMPLES</span></span>

### <span data-ttu-id="0f16e-111">Пример 1: получение имени рабочего стола Windows для виртуальных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="0f16e-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="0f16e-112">Эта команда возвращает Рабочий стол виртуальных рабочих столов Windows в группе applicaton.</span><span class="sxs-lookup"><span data-stu-id="0f16e-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="0f16e-113">Пример 2: список рабочих столов виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="0f16e-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="0f16e-114">Эта команда listsWindows виртуальные рабочие столы в группе applicaton.</span><span class="sxs-lookup"><span data-stu-id="0f16e-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="0f16e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f16e-115">PARAMETERS</span></span>

### <span data-ttu-id="0f16e-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="0f16e-116">-ApplicationGroupName</span></span>
<span data-ttu-id="0f16e-117">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="0f16e-117">The name of the application group</span></span>

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

### <span data-ttu-id="0f16e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f16e-118">-DefaultProfile</span></span>
<span data-ttu-id="0f16e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f16e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f16e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f16e-120">-InputObject</span></span>
<span data-ttu-id="0f16e-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="0f16e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0f16e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f16e-122">-Name</span></span>
<span data-ttu-id="0f16e-123">Имя рабочего стола в пределах указанной группы рабочего стола</span><span class="sxs-lookup"><span data-stu-id="0f16e-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f16e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f16e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f16e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f16e-125">The name of the resource group.</span></span>
<span data-ttu-id="0f16e-126">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="0f16e-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0f16e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f16e-127">-SubscriptionId</span></span>
<span data-ttu-id="0f16e-128">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0f16e-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0f16e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f16e-129">CommonParameters</span></span>
<span data-ttu-id="0f16e-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f16e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f16e-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f16e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f16e-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f16e-132">INPUTS</span></span>

### <span data-ttu-id="0f16e-133">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0f16e-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0f16e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f16e-134">OUTPUTS</span></span>

### <span data-ttu-id="0f16e-135">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="0f16e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="0f16e-136">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IDesktopList</span><span class="sxs-lookup"><span data-stu-id="0f16e-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="0f16e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f16e-137">NOTES</span></span>

<span data-ttu-id="0f16e-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0f16e-138">ALIASES</span></span>

<span data-ttu-id="0f16e-139">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0f16e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f16e-140">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0f16e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f16e-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f16e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f16e-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="0f16e-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0f16e-143">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="0f16e-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0f16e-144">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="0f16e-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0f16e-145">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0f16e-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0f16e-146">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f16e-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0f16e-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="0f16e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0f16e-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f16e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0f16e-149">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="0f16e-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="0f16e-150">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="0f16e-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0f16e-151">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0f16e-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0f16e-152">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="0f16e-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0f16e-153">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0f16e-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0f16e-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f16e-154">RELATED LINKS</span></span>

