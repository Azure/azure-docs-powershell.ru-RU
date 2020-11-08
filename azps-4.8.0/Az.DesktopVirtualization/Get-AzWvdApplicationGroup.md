---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078321"
---
# <span data-ttu-id="80957-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="80957-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="80957-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80957-102">SYNOPSIS</span></span>
<span data-ttu-id="80957-103">Получить группу приложений.</span><span class="sxs-lookup"><span data-stu-id="80957-103">Get an application group.</span></span>

## <span data-ttu-id="80957-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80957-104">SYNTAX</span></span>

### <span data-ttu-id="80957-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80957-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="80957-106">Получить</span><span class="sxs-lookup"><span data-stu-id="80957-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="80957-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80957-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="80957-108">Список</span><span class="sxs-lookup"><span data-stu-id="80957-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="80957-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80957-109">DESCRIPTION</span></span>
<span data-ttu-id="80957-110">Получить группу приложений.</span><span class="sxs-lookup"><span data-stu-id="80957-110">Get an application group.</span></span>

## <span data-ttu-id="80957-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80957-111">EXAMPLES</span></span>

### <span data-ttu-id="80957-112">Пример 1: получение виртуального рабочего стола Windows ApplicationGroup по имени</span><span class="sxs-lookup"><span data-stu-id="80957-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="80957-113">Эта команда получает ApplicationGroup виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80957-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="80957-114">Пример 2: список виртуальных рабочих столов Windows ApplicationGroups</span><span class="sxs-lookup"><span data-stu-id="80957-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="80957-115">Эта команда перечисляет ApplicationGroups виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80957-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="80957-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80957-116">PARAMETERS</span></span>

### <span data-ttu-id="80957-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80957-117">-DefaultProfile</span></span>
<span data-ttu-id="80957-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80957-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80957-119">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="80957-119">-Filter</span></span>
<span data-ttu-id="80957-120">Выражение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="80957-120">OData filter expression.</span></span>
<span data-ttu-id="80957-121">Допустимые свойства для фильтрации — applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="80957-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80957-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80957-122">-InputObject</span></span>
<span data-ttu-id="80957-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="80957-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80957-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80957-124">-Name</span></span>
<span data-ttu-id="80957-125">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="80957-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80957-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80957-126">-ResourceGroupName</span></span>
<span data-ttu-id="80957-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80957-127">The name of the resource group.</span></span>
<span data-ttu-id="80957-128">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="80957-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="80957-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80957-129">-SubscriptionId</span></span>
<span data-ttu-id="80957-130">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="80957-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="80957-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80957-131">CommonParameters</span></span>
<span data-ttu-id="80957-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80957-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80957-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80957-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80957-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80957-134">INPUTS</span></span>

### <span data-ttu-id="80957-135">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="80957-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="80957-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80957-136">OUTPUTS</span></span>

### <span data-ttu-id="80957-137">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="80957-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="80957-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="80957-138">NOTES</span></span>

<span data-ttu-id="80957-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="80957-139">ALIASES</span></span>

<span data-ttu-id="80957-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="80957-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80957-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="80957-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80957-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80957-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80957-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="80957-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80957-144">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="80957-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="80957-145">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="80957-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="80957-146">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="80957-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="80957-147">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80957-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="80957-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="80957-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80957-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80957-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="80957-150">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="80957-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="80957-151">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="80957-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="80957-152">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="80957-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="80957-153">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="80957-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="80957-154">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="80957-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="80957-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80957-155">RELATED LINKS</span></span>

