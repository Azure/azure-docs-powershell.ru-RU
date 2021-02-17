---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222412"
---
# <span data-ttu-id="7d563-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="7d563-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="7d563-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d563-102">SYNOPSIS</span></span>
<span data-ttu-id="7d563-103">Описание единицы настройки изображения</span><span class="sxs-lookup"><span data-stu-id="7d563-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="7d563-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d563-104">SYNTAX</span></span>

### <span data-ttu-id="7d563-105">ShellCustomizer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d563-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="7d563-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="7d563-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d563-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="7d563-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7d563-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d563-110">DESCRIPTION</span></span>
<span data-ttu-id="7d563-111">Описание единицы настройки изображения</span><span class="sxs-lookup"><span data-stu-id="7d563-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="7d563-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d563-112">EXAMPLES</span></span>

### <span data-ttu-id="7d563-113">Пример 1. Создание настраиваемой системы обновления Windows</span><span class="sxs-lookup"><span data-stu-id="7d563-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="7d563-114">Эта команда создает окно с обновлением windows.</span><span class="sxs-lookup"><span data-stu-id="7d563-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="7d563-115">Пример 2. Создание настраиваемой папки</span><span class="sxs-lookup"><span data-stu-id="7d563-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="7d563-116">Эта команда создает пользовательский файл.</span><span class="sxs-lookup"><span data-stu-id="7d563-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="7d563-117">Пример 3. Создание настроек Powershell</span><span class="sxs-lookup"><span data-stu-id="7d563-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="7d563-118">Эта команда создает настраиватель Powershell.</span><span class="sxs-lookup"><span data-stu-id="7d563-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="7d563-119">Пример 4. Создание настройки перезагрузки</span><span class="sxs-lookup"><span data-stu-id="7d563-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="7d563-120">Эта команда создает настраиваемый перезапуск.</span><span class="sxs-lookup"><span data-stu-id="7d563-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="7d563-121">Пример 5. Создание настраиваемой оболочки</span><span class="sxs-lookup"><span data-stu-id="7d563-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="7d563-122">Эта команда создает настраиваемый оболочки.</span><span class="sxs-lookup"><span data-stu-id="7d563-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="7d563-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d563-123">PARAMETERS</span></span>

### <span data-ttu-id="7d563-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="7d563-124">-CustomizerName</span></span>
<span data-ttu-id="7d563-125">Удобное имя, которое обеспечивает контекст для этого шага настройки.</span><span class="sxs-lookup"><span data-stu-id="7d563-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-126">-Destination</span><span class="sxs-lookup"><span data-stu-id="7d563-126">-Destination</span></span>
<span data-ttu-id="7d563-127">Абсолютный путь к файлу (с уже созданными вложенными структурами каталогов), в который файл (из sourceUri) будет загружен в VM-файл.</span><span class="sxs-lookup"><span data-stu-id="7d563-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-128">-FileCustomizer</span></span>
<span data-ttu-id="7d563-129">Отправка файлов на VMs (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="7d563-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="7d563-130">Соответствует пакету для подготовка файла.</span><span class="sxs-lookup"><span data-stu-id="7d563-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="7d563-131">-Filter</span></span>
<span data-ttu-id="7d563-132">Массив фильтров для выбора обновлений, которые нужно применить.</span><span class="sxs-lookup"><span data-stu-id="7d563-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="7d563-133">Опустить или указать пустой массив, который будет использовать по умолчанию (без фильтра).</span><span class="sxs-lookup"><span data-stu-id="7d563-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="7d563-134">Примеры и подробное описание этого поля можно найти по ссылке выше.</span><span class="sxs-lookup"><span data-stu-id="7d563-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-135">-Inline</span><span class="sxs-lookup"><span data-stu-id="7d563-135">-Inline</span></span>
<span data-ttu-id="7d563-136">Массив команд оболочки, которые нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="7d563-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="7d563-138">Запуск указанной powerShell в VM (Windows).</span><span class="sxs-lookup"><span data-stu-id="7d563-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="7d563-139">Соответствует предварительной информации Packer Powershell.</span><span class="sxs-lookup"><span data-stu-id="7d563-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="7d563-140">Можно укастить точно один из сценариевUri или inline.</span><span class="sxs-lookup"><span data-stu-id="7d563-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="7d563-141">-RestartCheckCommand</span></span>
<span data-ttu-id="7d563-142">Команда для проверки успешного перезапуска [По умолчанию: ''].</span><span class="sxs-lookup"><span data-stu-id="7d563-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="7d563-143">-RestartCommand</span></span>
<span data-ttu-id="7d563-144">Команда для выполнения перезапуска [По умолчанию: 'shutdown /r /f /t 0 /c packer restart']</span><span class="sxs-lookup"><span data-stu-id="7d563-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-145">-RestartCustomizer</span></span>
<span data-ttu-id="7d563-146">Перезагружает VM-компьютер и ждет его, пока он вернется в сеть (Windows).</span><span class="sxs-lookup"><span data-stu-id="7d563-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="7d563-147">Соответствует пакету для перезапуска windows.</span><span class="sxs-lookup"><span data-stu-id="7d563-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="7d563-148">-RestartTimeout</span></span>
<span data-ttu-id="7d563-149">Время перезапуска, указанное как строка значения и единицы, например "5 м" (5 минут) или "2 ч" (2 часа) [По умолчанию: '5m'].</span><span class="sxs-lookup"><span data-stu-id="7d563-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="7d563-150">-RunElevated</span></span>
<span data-ttu-id="7d563-151">При этом сценарий PowerShell будет запускаться с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="7d563-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="7d563-152">-ScriptUri</span></span>
<span data-ttu-id="7d563-153">URI сценария оболочки, который нужно запустить для настройки.</span><span class="sxs-lookup"><span data-stu-id="7d563-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="7d563-154">Это может быть ссылка в github, URI SAS для хранилища Azure и т. д.</span><span class="sxs-lookup"><span data-stu-id="7d563-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="7d563-155">-SearchCriterion</span></span>
<span data-ttu-id="7d563-156">Условия для поиска обновлений.</span><span class="sxs-lookup"><span data-stu-id="7d563-156">Criteria to search updates.</span></span>
<span data-ttu-id="7d563-157">Опустить или указать пустую строку для использования по умолчанию (поиск по всем строкам).</span><span class="sxs-lookup"><span data-stu-id="7d563-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="7d563-158">Примеры и подробное описание этого поля можно найти по ссылке выше.</span><span class="sxs-lookup"><span data-stu-id="7d563-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="7d563-159">-Sha256Checksum</span></span>
<span data-ttu-id="7d563-160">Контрольнаяum SHA256 сценария оболочки, представленная в поле scriptUri.</span><span class="sxs-lookup"><span data-stu-id="7d563-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-161">-ShellCustomizer</span></span>
<span data-ttu-id="7d563-162">Выполняет сценарий оболочки на этапе настройки (Linux).</span><span class="sxs-lookup"><span data-stu-id="7d563-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="7d563-163">Соответствует предварительной информации о пакетной оболочке.</span><span class="sxs-lookup"><span data-stu-id="7d563-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="7d563-164">Можно укастить точно один из сценариевUri или inline.</span><span class="sxs-lookup"><span data-stu-id="7d563-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="7d563-165">-SourceUri</span></span>
<span data-ttu-id="7d563-166">URI файла, который нужно отправить для настройки VM-файла.</span><span class="sxs-lookup"><span data-stu-id="7d563-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="7d563-167">Это может быть ссылка в github, URI SAS для хранилища Azure и т. д.</span><span class="sxs-lookup"><span data-stu-id="7d563-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="7d563-168">-UpdateLimit</span></span>
<span data-ttu-id="7d563-169">Максимальное количество обновлений, которые нужно применить одновременно.</span><span class="sxs-lookup"><span data-stu-id="7d563-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="7d563-170">Опустить или указать значение 0, используемого по умолчанию (1000).</span><span class="sxs-lookup"><span data-stu-id="7d563-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="7d563-171">-ValidExitCode</span></span>
<span data-ttu-id="7d563-172">Допустимые коды выхода для сценария PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7d563-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="7d563-173">[Значение по умолчанию: 0].</span><span class="sxs-lookup"><span data-stu-id="7d563-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="7d563-175">Устанавливает Обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="7d563-175">Installs Windows Updates.</span></span>
<span data-ttu-id="7d563-176">Соответствует пакете для предварительной версии Windows Update https://github.com/rgl/packer-provisioner-windows-update) (.</span><span class="sxs-lookup"><span data-stu-id="7d563-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d563-177">CommonParameters</span></span>
<span data-ttu-id="7d563-178">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d563-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d563-179">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d563-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d563-180">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d563-180">INPUTS</span></span>

## <span data-ttu-id="7d563-181">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d563-181">OUTPUTS</span></span>

### <span data-ttu-id="7d563-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="7d563-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="7d563-183">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d563-183">NOTES</span></span>

<span data-ttu-id="7d563-184">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7d563-184">ALIASES</span></span>

## <span data-ttu-id="7d563-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d563-185">RELATED LINKS</span></span>

