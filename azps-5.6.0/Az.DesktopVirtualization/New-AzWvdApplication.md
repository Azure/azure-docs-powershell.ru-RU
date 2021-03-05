---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: af0073a94401ce8c260027fcf905fd763d89326e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980536"
---
# <span data-ttu-id="7af63-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="7af63-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="7af63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7af63-102">SYNOPSIS</span></span>
<span data-ttu-id="7af63-103">Создайте или обновйте приложение.</span><span class="sxs-lookup"><span data-stu-id="7af63-103">Create or update an application.</span></span>

## <span data-ttu-id="7af63-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7af63-104">SYNTAX</span></span>

### <span data-ttu-id="7af63-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7af63-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7af63-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="7af63-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7af63-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7af63-107">DESCRIPTION</span></span>
<span data-ttu-id="7af63-108">Создайте или обновйте приложение.</span><span class="sxs-lookup"><span data-stu-id="7af63-108">Create or update an application.</span></span>

## <span data-ttu-id="7af63-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7af63-109">EXAMPLES</span></span>

### <span data-ttu-id="7af63-110">Пример 1. Создание виртуального настольного приложения Windows</span><span class="sxs-lookup"><span data-stu-id="7af63-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
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

<span data-ttu-id="7af63-111">Эта команда создает виртуальное настольное приложение Windows в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="7af63-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="7af63-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7af63-112">PARAMETERS</span></span>

### <span data-ttu-id="7af63-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="7af63-113">-AppAlias</span></span>
<span data-ttu-id="7af63-114">Псевдоним приложения из элемента меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="7af63-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="7af63-115">-ApplicationType</span></span>
<span data-ttu-id="7af63-116">Тип ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="7af63-116">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="7af63-117">-CommandLineArgument</span></span>
<span data-ttu-id="7af63-118">Аргументы командной строки для приложения.</span><span class="sxs-lookup"><span data-stu-id="7af63-118">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="7af63-119">-CommandLineSetting</span></span>
<span data-ttu-id="7af63-120">Указывает, можно ли запускать опубликованную программу с аргументами командной строки, предоставленными клиентом, аргументами командной строки, указанными во время публикации, или вообще без аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="7af63-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af63-121">-DefaultProfile</span></span>
<span data-ttu-id="7af63-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7af63-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7af63-123">-Description</span><span class="sxs-lookup"><span data-stu-id="7af63-123">-Description</span></span>
<span data-ttu-id="7af63-124">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="7af63-124">Description of Application.</span></span>

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

### <span data-ttu-id="7af63-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7af63-125">-FilePath</span></span>
<span data-ttu-id="7af63-126">Путь к исполняемом файлу приложения.</span><span class="sxs-lookup"><span data-stu-id="7af63-126">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7af63-127">-FriendlyName</span></span>
<span data-ttu-id="7af63-128">Имя приложения.</span><span class="sxs-lookup"><span data-stu-id="7af63-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="7af63-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="7af63-129">-GroupName</span></span>
<span data-ttu-id="7af63-130">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="7af63-130">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="7af63-131">-IconIndex</span></span>
<span data-ttu-id="7af63-132">Указатель значка.</span><span class="sxs-lookup"><span data-stu-id="7af63-132">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="7af63-133">-IconPath</span></span>
<span data-ttu-id="7af63-134">Путь к значку.</span><span class="sxs-lookup"><span data-stu-id="7af63-134">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="7af63-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="7af63-136">Определяет ИД приложения пакета для приложений MSIX.</span><span class="sxs-lookup"><span data-stu-id="7af63-136">Specifies the package application Id for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="7af63-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="7af63-138">Определяет семейство пакетов для приложений MSIX.</span><span class="sxs-lookup"><span data-stu-id="7af63-138">Specifies the package family name for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-139">-Name</span><span class="sxs-lookup"><span data-stu-id="7af63-139">-Name</span></span>
<span data-ttu-id="7af63-140">Имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="7af63-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7af63-141">-ResourceGroupName</span></span>
<span data-ttu-id="7af63-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7af63-142">The name of the resource group.</span></span>
<span data-ttu-id="7af63-143">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="7af63-143">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="7af63-144">-ShowInPortal</span></span>
<span data-ttu-id="7af63-145">Указывает, нужно ли показывать программу RemoteApp на сервере RD Web Access.</span><span class="sxs-lookup"><span data-stu-id="7af63-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="7af63-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7af63-146">-SubscriptionId</span></span>
<span data-ttu-id="7af63-147">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="7af63-147">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af63-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7af63-148">-Confirm</span></span>
<span data-ttu-id="7af63-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7af63-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7af63-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7af63-150">-WhatIf</span></span>
<span data-ttu-id="7af63-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7af63-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7af63-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7af63-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7af63-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af63-153">CommonParameters</span></span>
<span data-ttu-id="7af63-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7af63-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af63-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7af63-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af63-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7af63-156">INPUTS</span></span>

## <span data-ttu-id="7af63-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7af63-157">OUTPUTS</span></span>

### <span data-ttu-id="7af63-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="7af63-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="7af63-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7af63-159">NOTES</span></span>

<span data-ttu-id="7af63-160">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7af63-160">ALIASES</span></span>

## <span data-ttu-id="7af63-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7af63-161">RELATED LINKS</span></span>

