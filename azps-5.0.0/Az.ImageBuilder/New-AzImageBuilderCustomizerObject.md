---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311780"
---
# <span data-ttu-id="5895a-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="5895a-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="5895a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5895a-102">SYNOPSIS</span></span>
<span data-ttu-id="5895a-103">Описание единицы настройки изображения</span><span class="sxs-lookup"><span data-stu-id="5895a-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="5895a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5895a-104">SYNTAX</span></span>

### <span data-ttu-id="5895a-105">ShellCustomizer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5895a-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="5895a-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="5895a-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="5895a-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="5895a-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5895a-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5895a-110">DESCRIPTION</span></span>
<span data-ttu-id="5895a-111">Описание единицы настройки изображения</span><span class="sxs-lookup"><span data-stu-id="5895a-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="5895a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5895a-112">EXAMPLES</span></span>

### <span data-ttu-id="5895a-113">Пример 1: создание средства настройки центра обновления Windows</span><span class="sxs-lookup"><span data-stu-id="5895a-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="5895a-114">Эта команда создает средство настройки центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="5895a-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="5895a-115">Пример 2: создание средства настройки файлов</span><span class="sxs-lookup"><span data-stu-id="5895a-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="5895a-116">Эта команда создает средство настройки файлов.</span><span class="sxs-lookup"><span data-stu-id="5895a-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="5895a-117">Пример 3: создание средства настройки PowerShell</span><span class="sxs-lookup"><span data-stu-id="5895a-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="5895a-118">Эта команда создает средство настройки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5895a-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="5895a-119">Пример 4: создание средства настройки перезапуска</span><span class="sxs-lookup"><span data-stu-id="5895a-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="5895a-120">Эта команда создает средство настройки перезапуска.</span><span class="sxs-lookup"><span data-stu-id="5895a-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="5895a-121">Пример 5: создание средства настройки оболочки</span><span class="sxs-lookup"><span data-stu-id="5895a-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="5895a-122">Эта команда создает средство настройки оболочки.</span><span class="sxs-lookup"><span data-stu-id="5895a-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="5895a-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5895a-123">PARAMETERS</span></span>

### <span data-ttu-id="5895a-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="5895a-124">-CustomizerName</span></span>
<span data-ttu-id="5895a-125">Понятное имя, которое предоставляет контекст на этапе настройки.</span><span class="sxs-lookup"><span data-stu-id="5895a-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="5895a-126">-Destination</span><span class="sxs-lookup"><span data-stu-id="5895a-126">-Destination</span></span>
<span data-ttu-id="5895a-127">Абсолютный путь к файлу (вместе с уже созданными вложенными структурами каталогов), в который будет отправляться файл (из sourceUri) в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5895a-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="5895a-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-128">-FileCustomizer</span></span>
<span data-ttu-id="5895a-129">Отправка файлов в виртуальные машины (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="5895a-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="5895a-130">Соответствует профилировщику файлов пакета.</span><span class="sxs-lookup"><span data-stu-id="5895a-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="5895a-131">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="5895a-131">-Filter</span></span>
<span data-ttu-id="5895a-132">Массив фильтров для выбора применяемых обновлений.</span><span class="sxs-lookup"><span data-stu-id="5895a-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="5895a-133">Пропустите или укажите пустой массив, чтобы использовать значение по умолчанию (фильтр отсутствует).</span><span class="sxs-lookup"><span data-stu-id="5895a-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="5895a-134">Ниже приведены ссылки на примеры и подробное описание этого поля.</span><span class="sxs-lookup"><span data-stu-id="5895a-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="5895a-135">-Inline</span><span class="sxs-lookup"><span data-stu-id="5895a-135">-Inline</span></span>
<span data-ttu-id="5895a-136">Массив команд оболочки для выполнения.</span><span class="sxs-lookup"><span data-stu-id="5895a-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="5895a-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="5895a-138">Запускает указанную оболочку PowerShell на виртуальной машине (Windows).</span><span class="sxs-lookup"><span data-stu-id="5895a-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="5895a-139">Соответствует координатору PowerShell для пакетной подготовки.</span><span class="sxs-lookup"><span data-stu-id="5895a-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="5895a-140">Можно указать только один из параметров "scriptUri" или "inline".</span><span class="sxs-lookup"><span data-stu-id="5895a-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="5895a-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="5895a-141">-RestartCheckCommand</span></span>
<span data-ttu-id="5895a-142">Команда для проверки успешности запуска [по умолчанию: ' '].</span><span class="sxs-lookup"><span data-stu-id="5895a-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="5895a-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="5895a-143">-RestartCommand</span></span>
<span data-ttu-id="5895a-144">Команда для выполнения перезапуска [по умолчанию: "shutdown/r/f/t 0/c перезагрузка"]</span><span class="sxs-lookup"><span data-stu-id="5895a-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="5895a-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-145">-RestartCustomizer</span></span>
<span data-ttu-id="5895a-146">Перезагружает виртуальную машину и ждет, пока она не будет снова подключена к сети (Windows).</span><span class="sxs-lookup"><span data-stu-id="5895a-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="5895a-147">Соответствует выпадающему пакету Windows в качестве перезапуска подготовки.</span><span class="sxs-lookup"><span data-stu-id="5895a-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="5895a-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="5895a-148">-RestartTimeout</span></span>
<span data-ttu-id="5895a-149">Время ожидания перезапуска задается как строка величины и единица, например "5 млн." (5 минут) или "2H" (2 часа) [по умолчанию: "5 млн."].</span><span class="sxs-lookup"><span data-stu-id="5895a-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="5895a-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="5895a-150">-RunElevated</span></span>
<span data-ttu-id="5895a-151">Если указан, сценарий PowerShell будет выполняться с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="5895a-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="5895a-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="5895a-152">-ScriptUri</span></span>
<span data-ttu-id="5895a-153">URI сценария оболочки, который необходимо выполнить для настройки.</span><span class="sxs-lookup"><span data-stu-id="5895a-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="5895a-154">Это может быть ссылка GitHub, URI SAS для хранилища Azure и т. д.</span><span class="sxs-lookup"><span data-stu-id="5895a-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="5895a-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="5895a-155">-SearchCriterion</span></span>
<span data-ttu-id="5895a-156">Условия для поиска обновлений.</span><span class="sxs-lookup"><span data-stu-id="5895a-156">Criteria to search updates.</span></span>
<span data-ttu-id="5895a-157">Чтобы использовать значение по умолчанию (Поиск всех), пропустите или укажите пустую строку.</span><span class="sxs-lookup"><span data-stu-id="5895a-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="5895a-158">Ниже приведены ссылки на примеры и подробное описание этого поля.</span><span class="sxs-lookup"><span data-stu-id="5895a-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="5895a-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="5895a-159">-Sha256Checksum</span></span>
<span data-ttu-id="5895a-160">Контрольная сумма SHA256 сценария Shell, указанного в поле scriptUri.</span><span class="sxs-lookup"><span data-stu-id="5895a-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="5895a-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-161">-ShellCustomizer</span></span>
<span data-ttu-id="5895a-162">Запускает сценарий оболочки на этапе настройки (Linux).</span><span class="sxs-lookup"><span data-stu-id="5895a-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="5895a-163">Соответствует подготовке оболочки упаковки.</span><span class="sxs-lookup"><span data-stu-id="5895a-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="5895a-164">Можно указать только один из параметров "scriptUri" или "inline".</span><span class="sxs-lookup"><span data-stu-id="5895a-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="5895a-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="5895a-165">-SourceUri</span></span>
<span data-ttu-id="5895a-166">Универсальный код ресурса (URI) файла, который нужно отправить для настройки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5895a-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="5895a-167">Это может быть ссылка GitHub, URI SAS для хранилища Azure и т. д.</span><span class="sxs-lookup"><span data-stu-id="5895a-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="5895a-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="5895a-168">-UpdateLimit</span></span>
<span data-ttu-id="5895a-169">Максимальное количество обновлений, которые необходимо применить за один раз.</span><span class="sxs-lookup"><span data-stu-id="5895a-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="5895a-170">Чтобы использовать значение по умолчанию (1000), пропустите или укажите 0.</span><span class="sxs-lookup"><span data-stu-id="5895a-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="5895a-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="5895a-171">-ValidExitCode</span></span>
<span data-ttu-id="5895a-172">Допустимые коды выхода для сценария PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5895a-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="5895a-173">[По умолчанию: 0].</span><span class="sxs-lookup"><span data-stu-id="5895a-173">[Default: 0].</span></span>

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

### <span data-ttu-id="5895a-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="5895a-175">Установка обновлений для Windows.</span><span class="sxs-lookup"><span data-stu-id="5895a-175">Installs Windows Updates.</span></span>
<span data-ttu-id="5895a-176">Соответствует предварительной версии центра обновления Windows (версии) https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="5895a-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="5895a-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5895a-177">CommonParameters</span></span>
<span data-ttu-id="5895a-178">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5895a-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5895a-179">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5895a-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5895a-180">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5895a-180">INPUTS</span></span>

## <span data-ttu-id="5895a-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5895a-181">OUTPUTS</span></span>

### <span data-ttu-id="5895a-182">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. Api20200214. IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="5895a-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="5895a-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="5895a-183">NOTES</span></span>

<span data-ttu-id="5895a-184">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5895a-184">ALIASES</span></span>

## <span data-ttu-id="5895a-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5895a-185">RELATED LINKS</span></span>

