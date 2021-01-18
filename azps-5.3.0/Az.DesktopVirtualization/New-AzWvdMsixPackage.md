---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: 162071e07e8081f80e4187f049aef8931dcffc78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507569"
---
# <span data-ttu-id="31b0e-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="31b0e-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="31b0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="31b0e-103">Создание или обновление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="31b0e-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="31b0e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31b0e-104">SYNTAX</span></span>

### <span data-ttu-id="31b0e-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31b0e-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="31b0e-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="31b0e-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="31b0e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31b0e-107">DESCRIPTION</span></span>
<span data-ttu-id="31b0e-108">Создание или обновление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="31b0e-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="31b0e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31b0e-109">EXAMPLES</span></span>

### <span data-ttu-id="31b0e-110">Пример 1. Создание нового пакета MSIX в HostPool с помощью псевдонима пакета</span><span class="sxs-lookup"><span data-stu-id="31b0e-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="31b0e-111">Эта команда добавляет пакет MSIX из указанного пути изображения в HostPool.</span><span class="sxs-lookup"><span data-stu-id="31b0e-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="31b0e-112">Пример 2. Создание нового пакета MSIX в HostPool</span><span class="sxs-lookup"><span data-stu-id="31b0e-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -FullName PackageFullName `
                            -HostPoolName HostPoolName `
                            -ResourceGroupName ResourceGroupName ` 
                            -SubscriptionId SubscriptionId ` 
                            -DisplayName displayname `
                            -ImagePath imageURI ` 
                            -IsActive:$false `
                            -IsRegularRegistration:$false `
                            -LastUpdated datelastupdated `
                            -PackageApplication $apps `
                            -PackageDependency $deps `
                            -PackageFamilyName packagefamilyname `
                            -PackageName packagename `
                            -PackageRelativePath packagerelativepath `
                            -Version packageversion `

Name                              Type
----                              ----
HotPoolName/PackageFullName      Microsoft.DesktopVirtualization/hostpools/msixpackages

```

<span data-ttu-id="31b0e-113">Эта команда добавляет пакет MSIX в указанный HostPool.</span><span class="sxs-lookup"><span data-stu-id="31b0e-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="31b0e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31b0e-114">PARAMETERS</span></span>

### <span data-ttu-id="31b0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b0e-115">-DefaultProfile</span></span>
<span data-ttu-id="31b0e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31b0e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b0e-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="31b0e-117">-DisplayName</span></span>
<span data-ttu-id="31b0e-118">Удобное имя, которое будет отображаться на портале.</span><span class="sxs-lookup"><span data-stu-id="31b0e-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="31b0e-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="31b0e-119">-FullName</span></span>
<span data-ttu-id="31b0e-120">Название пакета MSIX для конкретной версии в указанном hostpool</span><span class="sxs-lookup"><span data-stu-id="31b0e-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0e-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="31b0e-121">-HostPoolName</span></span>
<span data-ttu-id="31b0e-122">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="31b0e-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="31b0e-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="31b0e-123">-ImagePath</span></span>
<span data-ttu-id="31b0e-124">Путь изображения VHD/CIM в сетевой области.</span><span class="sxs-lookup"><span data-stu-id="31b0e-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="31b0e-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="31b0e-125">-IsActive</span></span>
<span data-ttu-id="31b0e-126">Сделайте эту версию пакета активной во всем hostpool.</span><span class="sxs-lookup"><span data-stu-id="31b0e-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="31b0e-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="31b0e-127">-IsRegularRegistration</span></span>
<span data-ttu-id="31b0e-128">Определяет, как зарегистрировать пакет в веб-канале.</span><span class="sxs-lookup"><span data-stu-id="31b0e-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="31b0e-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="31b0e-129">-LastUpdated</span></span>
<span data-ttu-id="31b0e-130">Дата последнего обновления пакета, найденная в appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="31b0e-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0e-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="31b0e-131">-PackageAlias</span></span>
<span data-ttu-id="31b0e-132">Псевдоним пакета из извлечения изображения MSIX</span><span class="sxs-lookup"><span data-stu-id="31b0e-132">Package Alias from extract MSIX Image</span></span>

```yaml
Type: System.String
Parameter Sets: PackageAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0e-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="31b0e-133">-PackageApplication</span></span>
<span data-ttu-id="31b0e-134">Список пакетных приложений.</span><span class="sxs-lookup"><span data-stu-id="31b0e-134">List of package applications.</span></span>

<span data-ttu-id="31b0e-135">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств PACKAGEAPPLICATION и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="31b0e-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0e-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="31b0e-136">-PackageDependency</span></span>
<span data-ttu-id="31b0e-137">Список зависимостей пакетов.</span><span class="sxs-lookup"><span data-stu-id="31b0e-137">List of package dependencies.</span></span>

<span data-ttu-id="31b0e-138">Чтобы построить новую таблицу, см. раздел "ПРИМЕЧАНИЯ" для свойств PACKAGEDEPENDENCY и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="31b0e-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0e-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="31b0e-139">-PackageFamilyName</span></span>
<span data-ttu-id="31b0e-140">Пакет "Семейная имя из appxmanifest.xml".</span><span class="sxs-lookup"><span data-stu-id="31b0e-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="31b0e-141">Содержит имя пакета и имя издателя.</span><span class="sxs-lookup"><span data-stu-id="31b0e-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="31b0e-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="31b0e-142">-PackageName</span></span>
<span data-ttu-id="31b0e-143">Имя пакета из appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="31b0e-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="31b0e-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="31b0e-144">-PackageRelativePath</span></span>
<span data-ttu-id="31b0e-145">Относительный путь к пакету внутри изображения.</span><span class="sxs-lookup"><span data-stu-id="31b0e-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="31b0e-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b0e-146">-ResourceGroupName</span></span>
<span data-ttu-id="31b0e-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31b0e-147">The name of the resource group.</span></span>
<span data-ttu-id="31b0e-148">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="31b0e-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="31b0e-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31b0e-149">-SubscriptionId</span></span>
<span data-ttu-id="31b0e-150">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="31b0e-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="31b0e-151">-Version</span><span class="sxs-lookup"><span data-stu-id="31b0e-151">-Version</span></span>
<span data-ttu-id="31b0e-152">Версия пакета, найденная в appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="31b0e-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="31b0e-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31b0e-153">-Confirm</span></span>
<span data-ttu-id="31b0e-154">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="31b0e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b0e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b0e-155">-WhatIf</span></span>
<span data-ttu-id="31b0e-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31b0e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b0e-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="31b0e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b0e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b0e-158">CommonParameters</span></span>
<span data-ttu-id="31b0e-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b0e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b0e-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31b0e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b0e-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31b0e-161">INPUTS</span></span>

## <span data-ttu-id="31b0e-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31b0e-162">OUTPUTS</span></span>

### <span data-ttu-id="31b0e-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="31b0e-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="31b0e-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31b0e-164">NOTES</span></span>

<span data-ttu-id="31b0e-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="31b0e-165">ALIASES</span></span>

<span data-ttu-id="31b0e-166">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="31b0e-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="31b0e-167">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="31b0e-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31b0e-168">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="31b0e-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="31b0e-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: список приложений пакета.</span><span class="sxs-lookup"><span data-stu-id="31b0e-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="31b0e-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="31b0e-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="31b0e-171">`[AppUserModelId <String>]`: Используется для активации пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="31b0e-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="31b0e-172">Содержит имя пакета и applicationID.</span><span class="sxs-lookup"><span data-stu-id="31b0e-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="31b0e-173">Найдено в appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="31b0e-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="31b0e-174">`[Description <String>]`: Описание пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="31b0e-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="31b0e-175">`[FriendlyName <String>]`: удобное имя.</span><span class="sxs-lookup"><span data-stu-id="31b0e-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="31b0e-176">`[IconImageName <String>]`: удобное имя.</span><span class="sxs-lookup"><span data-stu-id="31b0e-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="31b0e-177">`[RawIcon <Byte[]>]`: значок 64-битной строки в качестве массива byte.</span><span class="sxs-lookup"><span data-stu-id="31b0e-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="31b0e-178">`[RawPng <Byte[]>]`: значок 64-битной строки в качестве массива byte.</span><span class="sxs-lookup"><span data-stu-id="31b0e-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="31b0e-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: список зависимостей пакетов.</span><span class="sxs-lookup"><span data-stu-id="31b0e-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="31b0e-180">`[DependencyName <String>]`: Имя зависимости пакета.</span><span class="sxs-lookup"><span data-stu-id="31b0e-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="31b0e-181">`[MinVersion <String>]`: Требуется версия зависимостей.</span><span class="sxs-lookup"><span data-stu-id="31b0e-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="31b0e-182">`[Publisher <String>]`: Имя издателя зависимостей.</span><span class="sxs-lookup"><span data-stu-id="31b0e-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="31b0e-183">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31b0e-183">RELATED LINKS</span></span>

