---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244554"
---
# <span data-ttu-id="dedea-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="dedea-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="dedea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dedea-102">SYNOPSIS</span></span>
<span data-ttu-id="dedea-103">Создание или обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="dedea-103">Create or update an application.</span></span>

## <span data-ttu-id="dedea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dedea-104">SYNTAX</span></span>

### <span data-ttu-id="dedea-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dedea-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dedea-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="dedea-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dedea-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dedea-107">DESCRIPTION</span></span>
<span data-ttu-id="dedea-108">Создание или обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="dedea-108">Create or update an application.</span></span>

## <span data-ttu-id="dedea-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dedea-109">EXAMPLES</span></span>

### <span data-ttu-id="dedea-110">Пример 1: создание приложения виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="dedea-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="dedea-111">Эта команда создает приложение виртуальных рабочих столов для Windows в группе applicaton.</span><span class="sxs-lookup"><span data-stu-id="dedea-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="dedea-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dedea-112">PARAMETERS</span></span>

### <span data-ttu-id="dedea-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="dedea-113">-AppAlias</span></span>
<span data-ttu-id="dedea-114">Псевдоним приложения из элемента меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="dedea-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="dedea-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="dedea-115">-CommandLineArgument</span></span>
<span data-ttu-id="dedea-116">Аргументы командной строки для приложения.</span><span class="sxs-lookup"><span data-stu-id="dedea-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="dedea-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="dedea-117">-CommandLineSetting</span></span>
<span data-ttu-id="dedea-118">Указывает, может ли опубликованное приложение запускаться с помощью аргументов командной строки, предоставленных клиентом, аргументов командной строки, заданных во время публикации, или вообще без аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="dedea-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="dedea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dedea-119">-DefaultProfile</span></span>
<span data-ttu-id="dedea-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dedea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dedea-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="dedea-121">-Description</span></span>
<span data-ttu-id="dedea-122">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="dedea-122">Description of Application.</span></span>

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

### <span data-ttu-id="dedea-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="dedea-123">-FilePath</span></span>
<span data-ttu-id="dedea-124">Задает путь к исполняемому файлу для приложения.</span><span class="sxs-lookup"><span data-stu-id="dedea-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="dedea-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dedea-125">-FriendlyName</span></span>
<span data-ttu-id="dedea-126">Понятное имя приложения.</span><span class="sxs-lookup"><span data-stu-id="dedea-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="dedea-127">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="dedea-127">-GroupName</span></span>
<span data-ttu-id="dedea-128">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="dedea-128">The name of the application group</span></span>

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

### <span data-ttu-id="dedea-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="dedea-129">-IconIndex</span></span>
<span data-ttu-id="dedea-130">Указатель значка.</span><span class="sxs-lookup"><span data-stu-id="dedea-130">Index of the icon.</span></span>

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

### <span data-ttu-id="dedea-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="dedea-131">-IconPath</span></span>
<span data-ttu-id="dedea-132">Значок "путь".</span><span class="sxs-lookup"><span data-stu-id="dedea-132">Path to icon.</span></span>

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

### <span data-ttu-id="dedea-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dedea-133">-Name</span></span>
<span data-ttu-id="dedea-134">Имя приложения в заданной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="dedea-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="dedea-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dedea-135">-ResourceGroupName</span></span>
<span data-ttu-id="dedea-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dedea-136">The name of the resource group.</span></span>
<span data-ttu-id="dedea-137">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="dedea-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dedea-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="dedea-138">-ShowInPortal</span></span>
<span data-ttu-id="dedea-139">Указывает, нужно ли отображать удаленное приложение RemoteApp на сервере веб-доступа к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="dedea-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="dedea-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dedea-140">-SubscriptionId</span></span>
<span data-ttu-id="dedea-141">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="dedea-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dedea-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dedea-142">-Confirm</span></span>
<span data-ttu-id="dedea-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dedea-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dedea-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dedea-144">-WhatIf</span></span>
<span data-ttu-id="dedea-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dedea-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dedea-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dedea-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dedea-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedea-147">CommonParameters</span></span>
<span data-ttu-id="dedea-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dedea-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedea-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dedea-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedea-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dedea-150">INPUTS</span></span>

## <span data-ttu-id="dedea-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dedea-151">OUTPUTS</span></span>

### <span data-ttu-id="dedea-152">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="dedea-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="dedea-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="dedea-153">NOTES</span></span>

<span data-ttu-id="dedea-154">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="dedea-154">ALIASES</span></span>

## <span data-ttu-id="dedea-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dedea-155">RELATED LINKS</span></span>

