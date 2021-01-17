---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 6907967acfd86f151b038e26aa9c33f62db50a5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396727"
---
# <span data-ttu-id="ee4a7-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="ee4a7-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="ee4a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4a7-103">Обновив приложение.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-103">Update an application.</span></span>

## <span data-ttu-id="ee4a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee4a7-104">SYNTAX</span></span>

### <span data-ttu-id="ee4a7-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee4a7-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ee4a7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ee4a7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee4a7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee4a7-107">DESCRIPTION</span></span>
<span data-ttu-id="ee4a7-108">Обновив приложение.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-108">Update an application.</span></span>

## <span data-ttu-id="ee4a7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee4a7-109">EXAMPLES</span></span>

### <span data-ttu-id="ee4a7-110">Пример 1. Обновление виртуального настольного приложения Windows</span><span class="sxs-lookup"><span data-stu-id="ee4a7-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="ee4a7-111">Эта команда обновляет приложение Виртуального рабочего стола Windows в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="ee4a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee4a7-112">PARAMETERS</span></span>

### <span data-ttu-id="ee4a7-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="ee4a7-113">-ApplicationType</span></span>
<span data-ttu-id="ee4a7-114">Тип ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-114">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4a7-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="ee4a7-115">-CommandLineArgument</span></span>
<span data-ttu-id="ee4a7-116">Аргументы командной строки для приложения.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="ee4a7-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="ee4a7-117">-CommandLineSetting</span></span>
<span data-ttu-id="ee4a7-118">Указывает, можно ли запускать опубликованную программу с аргументами командной строки, предоставленными клиентом, аргументами командной строки, указанными во время публикации, или вообще без аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4a7-119">-DefaultProfile</span></span>
<span data-ttu-id="ee4a7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee4a7-121">-Description</span><span class="sxs-lookup"><span data-stu-id="ee4a7-121">-Description</span></span>
<span data-ttu-id="ee4a7-122">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-122">Description of Application.</span></span>

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

### <span data-ttu-id="ee4a7-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="ee4a7-123">-FilePath</span></span>
<span data-ttu-id="ee4a7-124">Путь к исполняемом файлу приложения.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="ee4a7-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ee4a7-125">-FriendlyName</span></span>
<span data-ttu-id="ee4a7-126">Имя приложения.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="ee4a7-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="ee4a7-127">-GroupName</span></span>
<span data-ttu-id="ee4a7-128">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="ee4a7-128">The name of the application group</span></span>

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

### <span data-ttu-id="ee4a7-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="ee4a7-129">-IconIndex</span></span>
<span data-ttu-id="ee4a7-130">Указатель значка.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-130">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4a7-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="ee4a7-131">-IconPath</span></span>
<span data-ttu-id="ee4a7-132">Путь к значку.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-132">Path to icon.</span></span>

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

### <span data-ttu-id="ee4a7-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee4a7-133">-InputObject</span></span>
<span data-ttu-id="ee4a7-134">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee4a7-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="ee4a7-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="ee4a7-136">Определяет ИД приложения пакета для приложений MSIX.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="ee4a7-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="ee4a7-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="ee4a7-138">Определяет семейство пакетов для приложений MSIX.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="ee4a7-139">-Name</span><span class="sxs-lookup"><span data-stu-id="ee4a7-139">-Name</span></span>
<span data-ttu-id="ee4a7-140">Имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="ee4a7-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4a7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4a7-141">-ResourceGroupName</span></span>
<span data-ttu-id="ee4a7-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-142">The name of the resource group.</span></span>
<span data-ttu-id="ee4a7-143">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ee4a7-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="ee4a7-144">-ShowInPortal</span></span>
<span data-ttu-id="ee4a7-145">Указывает, нужно ли показывать программу RemoteApp на сервере RD Web Access.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="ee4a7-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee4a7-146">-SubscriptionId</span></span>
<span data-ttu-id="ee4a7-147">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ee4a7-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee4a7-148">-Tag</span></span>
<span data-ttu-id="ee4a7-149">теги для обновления</span><span class="sxs-lookup"><span data-stu-id="ee4a7-149">tags to be updated</span></span>

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

### <span data-ttu-id="ee4a7-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee4a7-150">-Confirm</span></span>
<span data-ttu-id="ee4a7-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee4a7-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee4a7-152">-WhatIf</span></span>
<span data-ttu-id="ee4a7-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee4a7-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee4a7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4a7-155">CommonParameters</span></span>
<span data-ttu-id="ee4a7-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4a7-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee4a7-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4a7-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee4a7-158">INPUTS</span></span>

### <span data-ttu-id="ee4a7-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ee4a7-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ee4a7-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee4a7-160">OUTPUTS</span></span>

### <span data-ttu-id="ee4a7-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="ee4a7-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span></span>

## <span data-ttu-id="ee4a7-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee4a7-162">NOTES</span></span>

<span data-ttu-id="ee4a7-163">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ee4a7-163">ALIASES</span></span>

<span data-ttu-id="ee4a7-164">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ee4a7-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee4a7-165">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee4a7-166">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee4a7-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ee4a7-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee4a7-168">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="ee4a7-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ee4a7-169">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="ee4a7-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ee4a7-170">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="ee4a7-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ee4a7-171">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ee4a7-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ee4a7-172">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ee4a7-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee4a7-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="ee4a7-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ee4a7-174">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ee4a7-175">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="ee4a7-176">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="ee4a7-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ee4a7-177">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ee4a7-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ee4a7-178">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="ee4a7-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ee4a7-179">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="ee4a7-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ee4a7-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee4a7-180">RELATED LINKS</span></span>

