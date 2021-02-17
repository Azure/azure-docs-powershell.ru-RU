---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: 67a49250607e1c7d70f1799aa26bd866924b5edc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234580"
---
# <span data-ttu-id="5f8d2-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="5f8d2-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="5f8d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8d2-103">Получите приложение.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-103">Get an application.</span></span>

## <span data-ttu-id="5f8d2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5f8d2-104">SYNTAX</span></span>

### <span data-ttu-id="5f8d2-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f8d2-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f8d2-106">Получить</span><span class="sxs-lookup"><span data-stu-id="5f8d2-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f8d2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5f8d2-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f8d2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f8d2-108">DESCRIPTION</span></span>
<span data-ttu-id="5f8d2-109">Получите приложение.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-109">Get an application.</span></span>

## <span data-ttu-id="5f8d2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5f8d2-110">EXAMPLES</span></span>

### <span data-ttu-id="5f8d2-111">Пример 1. Получение имени виртуального настольного приложения Windows</span><span class="sxs-lookup"><span data-stu-id="5f8d2-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="5f8d2-112">Эта команда получает виртуальное настольное приложение Windows в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="5f8d2-113">Пример 2. Список виртуальных классических приложений Windows</span><span class="sxs-lookup"><span data-stu-id="5f8d2-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="5f8d2-114">Эта команда содержит список виртуальных классических приложений Windows в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="5f8d2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f8d2-115">PARAMETERS</span></span>

### <span data-ttu-id="5f8d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8d2-116">-DefaultProfile</span></span>
<span data-ttu-id="5f8d2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f8d2-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="5f8d2-118">-GroupName</span></span>
<span data-ttu-id="5f8d2-119">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="5f8d2-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8d2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f8d2-120">-InputObject</span></span>
<span data-ttu-id="5f8d2-121">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f8d2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5f8d2-122">-Name</span></span>
<span data-ttu-id="5f8d2-123">Имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="5f8d2-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f8d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f8d2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-125">The name of the resource group.</span></span>
<span data-ttu-id="5f8d2-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5f8d2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f8d2-127">-SubscriptionId</span></span>
<span data-ttu-id="5f8d2-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5f8d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8d2-129">CommonParameters</span></span>
<span data-ttu-id="5f8d2-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8d2-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f8d2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8d2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f8d2-132">INPUTS</span></span>

### <span data-ttu-id="5f8d2-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5f8d2-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5f8d2-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f8d2-134">OUTPUTS</span></span>

### <span data-ttu-id="5f8d2-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="5f8d2-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="5f8d2-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5f8d2-136">NOTES</span></span>

<span data-ttu-id="5f8d2-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5f8d2-137">ALIASES</span></span>

<span data-ttu-id="5f8d2-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5f8d2-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f8d2-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f8d2-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f8d2-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="5f8d2-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f8d2-142">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="5f8d2-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5f8d2-143">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="5f8d2-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5f8d2-144">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="5f8d2-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5f8d2-145">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5f8d2-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5f8d2-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="5f8d2-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f8d2-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="5f8d2-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5f8d2-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5f8d2-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="5f8d2-150">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="5f8d2-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5f8d2-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5f8d2-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5f8d2-152">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="5f8d2-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5f8d2-153">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="5f8d2-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5f8d2-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f8d2-154">RELATED LINKS</span></span>

