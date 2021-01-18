---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504649"
---
# <span data-ttu-id="66af1-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="66af1-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="66af1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66af1-102">SYNOPSIS</span></span>
<span data-ttu-id="66af1-103">Отправка сценария DSC в хранилище BLOB-хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="66af1-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="66af1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="66af1-104">SYNTAX</span></span>

### <span data-ttu-id="66af1-105">UploadArchive (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66af1-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66af1-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="66af1-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66af1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66af1-107">DESCRIPTION</span></span>
<span data-ttu-id="66af1-108">С помощью cmdlet **Publish-AzVMDscConfiguration** можно загрузить сценарий настройки состояния (DSC) в хранилище BLOB-машин Azure, который позже можно будет применить к виртуальным машинам Azure с помощью Set-AzVMDscExtension.</span><span class="sxs-lookup"><span data-stu-id="66af1-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="66af1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="66af1-109">EXAMPLES</span></span>

### <span data-ttu-id="66af1-110">Пример 1. Создание ZIP-пакета для его отправки в хранилище Azure</span><span class="sxs-lookup"><span data-stu-id="66af1-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="66af1-111">Эта команда создает ZIP-пакет для заданного сценария и всех зависимых модулей ресурсов и передает его в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="66af1-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="66af1-112">Пример 2. Создание ZIP-пакета и его хранение в локальном файле</span><span class="sxs-lookup"><span data-stu-id="66af1-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="66af1-113">Эта команда создает ZIP-пакет для заданного сценария и всех зависимых модулей ресурсов и сохраняет его в локальном файле, который называется .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="66af1-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="66af1-114">Пример 3. Добавление конфигурации в архив и ее отправка в хранилище</span><span class="sxs-lookup"><span data-stu-id="66af1-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="66af1-115">Эта команда добавляет конфигурацию с Sample.ps1 в архив конфигурации для отправки в хранилище Azure и пропускает зависимые модули ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66af1-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="66af1-116">Пример 4. Добавление данных конфигурации и конфигурации в архив и их отправка в хранилище</span><span class="sxs-lookup"><span data-stu-id="66af1-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="66af1-117">Эта команда добавляет данные конфигурации Sample.ps1 и конфигурации SampleData.psd1 в архив конфигурации для отправки в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="66af1-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="66af1-118">Пример 5. Добавление данных конфигурации, конфигурации и дополнительного содержимого в архив и его отправка в хранилище</span><span class="sxs-lookup"><span data-stu-id="66af1-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="66af1-119">Эта команда добавляет конфигурацию Sample.ps1, данные конфигурации SampleData.psd1 и дополнительное содержимое в архив конфигурации для отправки в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="66af1-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="66af1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66af1-120">PARAMETERS</span></span>

### <span data-ttu-id="66af1-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="66af1-121">-AdditionalPath</span></span>
<span data-ttu-id="66af1-122">Путь к файлу или каталогу, которые нужно включить в архив конфигурации.</span><span class="sxs-lookup"><span data-stu-id="66af1-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="66af1-123">Оно загружается на виртуальную машину вместе с конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="66af1-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="66af1-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="66af1-125">Путь к PSD1-файлу, который определяет данные для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="66af1-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="66af1-126">Он добавляется в архив конфигурации, а затем передается в функцию конфигурации.</span><span class="sxs-lookup"><span data-stu-id="66af1-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="66af1-127">Она перезаписывается путем к данным конфигурации, заданным Set-AzVMDscExtension-м</span><span class="sxs-lookup"><span data-stu-id="66af1-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="66af1-128">-ConfigurationPath</span></span>
<span data-ttu-id="66af1-129">Путь к файлу, который содержит одну или несколько конфигураций.</span><span class="sxs-lookup"><span data-stu-id="66af1-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="66af1-130">Это может быть Windows PowerShell сценарий (PS1) или Windows PowerShell (PSM1).</span><span class="sxs-lookup"><span data-stu-id="66af1-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="66af1-131">-ContainerName</span></span>
<span data-ttu-id="66af1-132">Указывает имя контейнера хранилища Azure, в который загружается конфигурация.</span><span class="sxs-lookup"><span data-stu-id="66af1-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66af1-133">-DefaultProfile</span></span>
<span data-ttu-id="66af1-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66af1-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-135">-Force</span><span class="sxs-lookup"><span data-stu-id="66af1-135">-Force</span></span>
<span data-ttu-id="66af1-136">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="66af1-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66af1-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="66af1-137">-OutputArchivePath</span></span>
<span data-ttu-id="66af1-138">Путь к локальному ZIP-файлу для записи архива конфигурации.</span><span class="sxs-lookup"><span data-stu-id="66af1-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="66af1-139">Если используется этот параметр, сценарий конфигурации не передается в хранилище BLOB-параметров Azure.</span><span class="sxs-lookup"><span data-stu-id="66af1-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66af1-140">-ResourceGroupName</span></span>
<span data-ttu-id="66af1-141">Имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="66af1-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="66af1-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="66af1-143">Указывает на то, что этот cmdlet исключает зависимости ресурсов DSC из архива конфигурации.</span><span class="sxs-lookup"><span data-stu-id="66af1-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="66af1-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="66af1-144">-StorageAccountName</span></span>
<span data-ttu-id="66af1-145">Указывает имя учетной записи хранилища Azure, используемой для отправки сценария конфигурации в контейнер, заданный *параметром ContainerName.*</span><span class="sxs-lookup"><span data-stu-id="66af1-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="66af1-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="66af1-147">Указывает суффикс для точки хранения.</span><span class="sxs-lookup"><span data-stu-id="66af1-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66af1-148">-Confirm</span></span>
<span data-ttu-id="66af1-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="66af1-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66af1-150">-WhatIf</span></span>
<span data-ttu-id="66af1-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66af1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66af1-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="66af1-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66af1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66af1-153">CommonParameters</span></span>
<span data-ttu-id="66af1-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66af1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66af1-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66af1-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66af1-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66af1-156">INPUTS</span></span>

### <span data-ttu-id="66af1-157">System.String</span><span class="sxs-lookup"><span data-stu-id="66af1-157">System.String</span></span>

### <span data-ttu-id="66af1-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="66af1-158">System.String[]</span></span>

## <span data-ttu-id="66af1-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="66af1-159">OUTPUTS</span></span>

### <span data-ttu-id="66af1-160">System.String</span><span class="sxs-lookup"><span data-stu-id="66af1-160">System.String</span></span>

## <span data-ttu-id="66af1-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="66af1-161">NOTES</span></span>

## <span data-ttu-id="66af1-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66af1-162">RELATED LINKS</span></span>

[<span data-ttu-id="66af1-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="66af1-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="66af1-164">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="66af1-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="66af1-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="66af1-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


