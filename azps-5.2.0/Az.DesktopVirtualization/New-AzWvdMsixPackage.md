---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: fd5dd920863d4bd53257cfe2170e83f53c620096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409415"
---
# <span data-ttu-id="5cbf2-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="5cbf2-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="5cbf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cbf2-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbf2-103">Создание или обновление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="5cbf2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cbf2-104">SYNTAX</span></span>

### <span data-ttu-id="5cbf2-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5cbf2-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5cbf2-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="5cbf2-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5cbf2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cbf2-107">DESCRIPTION</span></span>
<span data-ttu-id="5cbf2-108">Создание или обновление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="5cbf2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cbf2-109">EXAMPLES</span></span>

### <span data-ttu-id="5cbf2-110">Пример 1. Создание нового пакета MSIX в HostPool с помощью псевдонима пакета</span><span class="sxs-lookup"><span data-stu-id="5cbf2-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="5cbf2-111">Эта команда добавляет пакет MSIX из указанного пути изображения в HostPool.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="5cbf2-112">Пример 2. Создание нового пакета MSIX в HostPool</span><span class="sxs-lookup"><span data-stu-id="5cbf2-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
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

<span data-ttu-id="5cbf2-113">Эта команда добавляет пакет MSIX в указанный HostPool.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="5cbf2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cbf2-114">PARAMETERS</span></span>

### <span data-ttu-id="5cbf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbf2-115">-DefaultProfile</span></span>
<span data-ttu-id="5cbf2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cbf2-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5cbf2-117">-DisplayName</span></span>
<span data-ttu-id="5cbf2-118">Удобное имя, которое будет отображаться на портале.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="5cbf2-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="5cbf2-119">-FullName</span></span>
<span data-ttu-id="5cbf2-120">Название пакета MSIX для конкретной версии в указанном hostpool</span><span class="sxs-lookup"><span data-stu-id="5cbf2-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="5cbf2-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5cbf2-121">-HostPoolName</span></span>
<span data-ttu-id="5cbf2-122">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5cbf2-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="5cbf2-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="5cbf2-123">-ImagePath</span></span>
<span data-ttu-id="5cbf2-124">Путь изображения VHD/CIM в сетевой области.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="5cbf2-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="5cbf2-125">-IsActive</span></span>
<span data-ttu-id="5cbf2-126">Сделайте эту версию пакета активной во всем hostpool.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="5cbf2-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="5cbf2-127">-IsRegularRegistration</span></span>
<span data-ttu-id="5cbf2-128">Определяет, как зарегистрировать пакет в веб-канале.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="5cbf2-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="5cbf2-129">-LastUpdated</span></span>
<span data-ttu-id="5cbf2-130">Дата последнего обновления пакета, найденная в appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="5cbf2-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="5cbf2-131">-PackageAlias</span></span>
<span data-ttu-id="5cbf2-132">Package Alias from extract MSIX Image</span><span class="sxs-lookup"><span data-stu-id="5cbf2-132">Package Alias from extract MSIX Image</span></span>

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

### <span data-ttu-id="5cbf2-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="5cbf2-133">-PackageApplication</span></span>
<span data-ttu-id="5cbf2-134">Список пакетных приложений.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-134">List of package applications.</span></span>

<span data-ttu-id="5cbf2-135">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств PACKAGEAPPLICATION и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbf2-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="5cbf2-136">-PackageDependency</span></span>
<span data-ttu-id="5cbf2-137">Список зависимостей пакетов.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-137">List of package dependencies.</span></span>

<span data-ttu-id="5cbf2-138">Чтобы построить новую таблицу, см. раздел "ПРИМЕЧАНИЯ" для свойств PACKAGEDEPENDENCY и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbf2-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="5cbf2-139">-PackageFamilyName</span></span>
<span data-ttu-id="5cbf2-140">Пакет "Семейная имя из appxmanifest.xml".</span><span class="sxs-lookup"><span data-stu-id="5cbf2-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="5cbf2-141">Содержит имя пакета и имя издателя.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="5cbf2-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="5cbf2-142">-PackageName</span></span>
<span data-ttu-id="5cbf2-143">Имя пакета из appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="5cbf2-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="5cbf2-144">-PackageRelativePath</span></span>
<span data-ttu-id="5cbf2-145">Относительный путь к пакету внутри изображения.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="5cbf2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cbf2-146">-ResourceGroupName</span></span>
<span data-ttu-id="5cbf2-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-147">The name of the resource group.</span></span>
<span data-ttu-id="5cbf2-148">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5cbf2-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cbf2-149">-SubscriptionId</span></span>
<span data-ttu-id="5cbf2-150">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5cbf2-151">-Версия</span><span class="sxs-lookup"><span data-stu-id="5cbf2-151">-Version</span></span>
<span data-ttu-id="5cbf2-152">Версия пакета, найденная в appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="5cbf2-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cbf2-153">-Confirm</span></span>
<span data-ttu-id="5cbf2-154">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbf2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cbf2-155">-WhatIf</span></span>
<span data-ttu-id="5cbf2-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cbf2-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbf2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbf2-158">CommonParameters</span></span>
<span data-ttu-id="5cbf2-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbf2-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cbf2-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbf2-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cbf2-161">INPUTS</span></span>

## <span data-ttu-id="5cbf2-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cbf2-162">OUTPUTS</span></span>

### <span data-ttu-id="5cbf2-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="5cbf2-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="5cbf2-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cbf2-164">NOTES</span></span>

<span data-ttu-id="5cbf2-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5cbf2-165">ALIASES</span></span>

<span data-ttu-id="5cbf2-166">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5cbf2-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cbf2-167">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cbf2-168">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cbf2-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: список приложений пакета.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="5cbf2-170">`[AppId <String>]`: Пакетный ИД приложения, найденный в appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="5cbf2-171">`[AppUserModelId <String>]`: Используется для активации пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="5cbf2-172">Содержит имя пакета и applicationID.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="5cbf2-173">Найдено в appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="5cbf2-174">`[Description <String>]`: Описание пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="5cbf2-175">`[FriendlyName <String>]`: удобное имя.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="5cbf2-176">`[IconImageName <String>]`: удобное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="5cbf2-177">`[RawIcon <Byte[]>]`: значок 64-битной строки в качестве массива byte.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="5cbf2-178">`[RawPng <Byte[]>]`: значок 64-битной строки в качестве массива byte.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="5cbf2-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: список зависимостей пакетов.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="5cbf2-180">`[DependencyName <String>]`: Имя зависимости пакета.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="5cbf2-181">`[MinVersion <String>]`: Требуется версия зависимостей.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="5cbf2-182">`[Publisher <String>]`: Имя издателя зависимостей.</span><span class="sxs-lookup"><span data-stu-id="5cbf2-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="5cbf2-183">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cbf2-183">RELATED LINKS</span></span>

