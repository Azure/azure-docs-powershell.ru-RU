---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079809"
---
# <span data-ttu-id="ac5f0-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac5f0-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="ac5f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5f0-103">Передает сценарий DSC в хранилище BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="ac5f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac5f0-104">SYNTAX</span></span>

### <span data-ttu-id="ac5f0-105">UploadArchive (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac5f0-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac5f0-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="ac5f0-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac5f0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac5f0-107">DESCRIPTION</span></span>
<span data-ttu-id="ac5f0-108">Командлет **Publish-AzVMDscConfiguration** передает в хранилище больших двоичных объектов Azure сценарий Desired State Configuration (DSC), который позже можно применить к виртуальным машинам Azure с помощью командлета Set-AzVMDscExtension.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="ac5f0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac5f0-109">EXAMPLES</span></span>

### <span data-ttu-id="ac5f0-110">Пример 1: создание ZIP-пакета для отправки в хранилище Azure</span><span class="sxs-lookup"><span data-stu-id="ac5f0-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="ac5f0-111">Эта команда создает ZIP-пакет для указанного сценария и зависимых модулей ресурсов и отправляет его в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="ac5f0-112">Пример 2: создание ZIP-пакета и сохранение его в локальном файле</span><span class="sxs-lookup"><span data-stu-id="ac5f0-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="ac5f0-113">Эта команда создает ZIP-пакет для указанного сценария и зависимых от него модулей ресурсов и сохраняет его в локальном файле с именем .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="ac5f0-114">Пример 3: Добавление конфигурации в архив, а затем его отправка в хранилище</span><span class="sxs-lookup"><span data-stu-id="ac5f0-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="ac5f0-115">Эта команда добавляет конфигурацию с именем Sample.ps1 в архив конфигурации для отправки в хранилище Azure и пропускает зависимые модули ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="ac5f0-116">Пример 4: Добавление данных конфигурации и конфигурации в архив, а затем их отправка в хранилище</span><span class="sxs-lookup"><span data-stu-id="ac5f0-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="ac5f0-117">Эта команда добавляет конфигурацию с именем Sample.ps1 и данными конфигурации с именем SampleData.psd1 в архив конфигурации для отправки в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="ac5f0-118">Пример 5: Добавление конфигурации, данных конфигурации и дополнительного содержимого в архив, а затем его отправка в хранилище</span><span class="sxs-lookup"><span data-stu-id="ac5f0-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="ac5f0-119">Эта команда добавляет конфигурацию с именем Sample.ps1, данными конфигурации SampleData.psd1 и дополнительным содержимым в архив конфигурации для отправки в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="ac5f0-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac5f0-120">PARAMETERS</span></span>

### <span data-ttu-id="ac5f0-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="ac5f0-121">-AdditionalPath</span></span>
<span data-ttu-id="ac5f0-122">Задает путь к файлу или папке, которые нужно включить в архив конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="ac5f0-123">Оно будет загружено на виртуальную машину вместе с конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

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

### <span data-ttu-id="ac5f0-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="ac5f0-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="ac5f0-125">Задает путь к файлу PSD1, который задает данные для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="ac5f0-126">Она будет добавлена в архив конфигурации, а затем передана в функцию конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="ac5f0-127">Он перезаписывается путем данных конфигурации, предоставленным с помощью командлета Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ac5f0-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="ac5f0-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="ac5f0-128">-ConfigurationPath</span></span>
<span data-ttu-id="ac5f0-129">Задает путь к файлу, содержащему одну или несколько конфигураций.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="ac5f0-130">Файл может быть файлом сценария Windows PowerShell (PS1) или файлом модуля Windows PowerShell (. PSM1).</span><span class="sxs-lookup"><span data-stu-id="ac5f0-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

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

### <span data-ttu-id="ac5f0-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ac5f0-131">-ContainerName</span></span>
<span data-ttu-id="ac5f0-132">Указывает имя контейнера хранилища Azure, в который загружается конфигурация.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

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

### <span data-ttu-id="ac5f0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5f0-133">-DefaultProfile</span></span>
<span data-ttu-id="ac5f0-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac5f0-135">-Force</span><span class="sxs-lookup"><span data-stu-id="ac5f0-135">-Force</span></span>
<span data-ttu-id="ac5f0-136">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac5f0-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="ac5f0-137">-OutputArchivePath</span></span>
<span data-ttu-id="ac5f0-138">Задает путь к локальному ZIP-файлу для записи архива конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="ac5f0-139">При использовании этого параметра сценарий конфигурации не загружается в хранилище BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

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

### <span data-ttu-id="ac5f0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac5f0-140">-ResourceGroupName</span></span>
<span data-ttu-id="ac5f0-141">Указывает имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-141">Specifies the name of the resource group that contains the storage account.</span></span>

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

### <span data-ttu-id="ac5f0-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="ac5f0-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="ac5f0-143">Указывает на то, что этот командлет исключает зависимости ресурса DSC из архива конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="ac5f0-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ac5f0-144">-StorageAccountName</span></span>
<span data-ttu-id="ac5f0-145">Указывает имя учетной записи хранения Azure, используемой для передачи сценария конфигурации в контейнер, указанный в параметре *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="ac5f0-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

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

### <span data-ttu-id="ac5f0-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ac5f0-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="ac5f0-147">Указывает суффикс для конечной точки хранилища.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-147">Specifies the suffix for the storage end point.</span></span>

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

### <span data-ttu-id="ac5f0-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac5f0-148">-Confirm</span></span>
<span data-ttu-id="ac5f0-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac5f0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac5f0-150">-WhatIf</span></span>
<span data-ttu-id="ac5f0-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac5f0-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac5f0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5f0-153">CommonParameters</span></span>
<span data-ttu-id="ac5f0-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac5f0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5f0-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac5f0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5f0-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac5f0-156">INPUTS</span></span>

### <span data-ttu-id="ac5f0-157">System. String</span><span class="sxs-lookup"><span data-stu-id="ac5f0-157">System.String</span></span>

### <span data-ttu-id="ac5f0-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="ac5f0-158">System.String[]</span></span>

## <span data-ttu-id="ac5f0-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac5f0-159">OUTPUTS</span></span>

### <span data-ttu-id="ac5f0-160">System. String</span><span class="sxs-lookup"><span data-stu-id="ac5f0-160">System.String</span></span>

## <span data-ttu-id="ac5f0-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac5f0-161">NOTES</span></span>

## <span data-ttu-id="ac5f0-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac5f0-162">RELATED LINKS</span></span>

[<span data-ttu-id="ac5f0-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ac5f0-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="ac5f0-164">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ac5f0-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="ac5f0-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ac5f0-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


