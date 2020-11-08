---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247488"
---
# <span data-ttu-id="34156-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="34156-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="34156-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34156-102">SYNOPSIS</span></span>
<span data-ttu-id="34156-103">Обновите приложение.</span><span class="sxs-lookup"><span data-stu-id="34156-103">Update an application.</span></span>

## <span data-ttu-id="34156-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34156-104">SYNTAX</span></span>

### <span data-ttu-id="34156-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34156-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="34156-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="34156-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34156-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34156-107">DESCRIPTION</span></span>
<span data-ttu-id="34156-108">Обновите приложение.</span><span class="sxs-lookup"><span data-stu-id="34156-108">Update an application.</span></span>

## <span data-ttu-id="34156-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34156-109">EXAMPLES</span></span>

### <span data-ttu-id="34156-110">Пример 1: обновление приложения виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="34156-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="34156-111">Эта команда обновляет приложение виртуальных рабочих столов Windows в группе applicaton.</span><span class="sxs-lookup"><span data-stu-id="34156-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="34156-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34156-112">PARAMETERS</span></span>

### <span data-ttu-id="34156-113">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="34156-113">-CommandLineArgument</span></span>
<span data-ttu-id="34156-114">Аргументы командной строки для приложения.</span><span class="sxs-lookup"><span data-stu-id="34156-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="34156-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="34156-115">-CommandLineSetting</span></span>
<span data-ttu-id="34156-116">Указывает, может ли опубликованное приложение запускаться с помощью аргументов командной строки, предоставленных клиентом, аргументов командной строки, заданных во время публикации, или вообще без аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="34156-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="34156-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34156-117">-DefaultProfile</span></span>
<span data-ttu-id="34156-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34156-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34156-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="34156-119">-Description</span></span>
<span data-ttu-id="34156-120">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="34156-120">Description of Application.</span></span>

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

### <span data-ttu-id="34156-121">-FilePath</span><span class="sxs-lookup"><span data-stu-id="34156-121">-FilePath</span></span>
<span data-ttu-id="34156-122">Задает путь к исполняемому файлу для приложения.</span><span class="sxs-lookup"><span data-stu-id="34156-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="34156-123">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="34156-123">-FriendlyName</span></span>
<span data-ttu-id="34156-124">Понятное имя приложения.</span><span class="sxs-lookup"><span data-stu-id="34156-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="34156-125">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="34156-125">-GroupName</span></span>
<span data-ttu-id="34156-126">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="34156-126">The name of the application group</span></span>

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

### <span data-ttu-id="34156-127">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="34156-127">-IconIndex</span></span>
<span data-ttu-id="34156-128">Указатель значка.</span><span class="sxs-lookup"><span data-stu-id="34156-128">Index of the icon.</span></span>

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

### <span data-ttu-id="34156-129">-IconPath</span><span class="sxs-lookup"><span data-stu-id="34156-129">-IconPath</span></span>
<span data-ttu-id="34156-130">Значок "путь".</span><span class="sxs-lookup"><span data-stu-id="34156-130">Path to icon.</span></span>

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

### <span data-ttu-id="34156-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34156-131">-InputObject</span></span>
<span data-ttu-id="34156-132">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="34156-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="34156-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34156-133">-Name</span></span>
<span data-ttu-id="34156-134">Имя приложения в заданной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="34156-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="34156-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34156-135">-ResourceGroupName</span></span>
<span data-ttu-id="34156-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34156-136">The name of the resource group.</span></span>
<span data-ttu-id="34156-137">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="34156-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="34156-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="34156-138">-ShowInPortal</span></span>
<span data-ttu-id="34156-139">Указывает, нужно ли отображать удаленное приложение RemoteApp на сервере веб-доступа к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="34156-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="34156-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34156-140">-SubscriptionId</span></span>
<span data-ttu-id="34156-141">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="34156-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="34156-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="34156-142">-Tag</span></span>
<span data-ttu-id="34156-143">Теги для обновления</span><span class="sxs-lookup"><span data-stu-id="34156-143">tags to be updated</span></span>

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

### <span data-ttu-id="34156-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34156-144">-Confirm</span></span>
<span data-ttu-id="34156-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34156-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34156-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34156-146">-WhatIf</span></span>
<span data-ttu-id="34156-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34156-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34156-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34156-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34156-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34156-149">CommonParameters</span></span>
<span data-ttu-id="34156-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34156-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34156-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34156-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34156-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34156-152">INPUTS</span></span>

### <span data-ttu-id="34156-153">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="34156-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="34156-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34156-154">OUTPUTS</span></span>

### <span data-ttu-id="34156-155">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="34156-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="34156-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="34156-156">NOTES</span></span>

<span data-ttu-id="34156-157">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="34156-157">ALIASES</span></span>

<span data-ttu-id="34156-158">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="34156-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34156-159">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="34156-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34156-160">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34156-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34156-161">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="34156-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34156-162">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="34156-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="34156-163">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="34156-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="34156-164">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="34156-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="34156-165">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34156-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="34156-166">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="34156-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34156-167">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34156-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="34156-168">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="34156-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="34156-169">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="34156-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="34156-170">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="34156-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="34156-171">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="34156-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="34156-172">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="34156-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="34156-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34156-173">RELATED LINKS</span></span>

