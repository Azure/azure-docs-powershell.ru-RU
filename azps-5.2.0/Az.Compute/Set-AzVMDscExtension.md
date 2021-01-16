---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 7b4c416b8a083b1cf64e9e23ccdf08f153a76261
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393959"
---
# <span data-ttu-id="f3ed9-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f3ed9-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="f3ed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ed9-103">Настраивает расширение DSC на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="f3ed9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3ed9-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3ed9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3ed9-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ed9-106">Для настройки расширения Windows PowerShell DSC в группе ресурсов будет настроено расширение **Set-AzVMDscExtension.**</span><span class="sxs-lookup"><span data-stu-id="f3ed9-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="f3ed9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3ed9-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ed9-108">Пример 1. Настройка расширения DSC</span><span class="sxs-lookup"><span data-stu-id="f3ed9-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="f3ed9-109">Эта команда задает расширение DSC на виртуальной машине VM07, чтобы Sample.ps1.zip из учетной записи хранения Stg и контейнера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="f3ed9-110">Команда вызывает конфигурацию с именем ConfigName.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="f3ed9-111">Файл Sample.ps1.zip ранее был добавлен с помощью **Publish-AzVMDscConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="f3ed9-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="f3ed9-112">Пример 2. Настройка расширения DSC с данными конфигурации</span><span class="sxs-lookup"><span data-stu-id="f3ed9-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="f3ed9-113">Эта команда задает расширение на виртуальной машине с именем VM13 для скачивания Sample.ps1.zip из учетной записи хранения Stg и контейнера с именем WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="f3ed9-114">Команда конфигурации с именем ConfigName и указывает данные конфигурации и аргументы.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="f3ed9-115">Файл Sample.ps1.zip ранее был добавлен с помощью **Publish-AzVMDscConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="f3ed9-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="f3ed9-116">Пример 3. Настройка расширения DSC с данными конфигурации с автоматическим обновлением</span><span class="sxs-lookup"><span data-stu-id="f3ed9-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="f3ed9-117">Эта команда задает расширение на виртуальной машине (VM22) для скачивания Sample.ps1.zip из учетной записи хранения Stg и контейнера с именем WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="f3ed9-118">Команда вызывает конфигурацию с именем ConfigName и указывает данные конфигурации и аргументы.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="f3ed9-119">Эта команда также включает автоматическое обновление обработера расширений до последней версии.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="f3ed9-120">The Sample.ps1.zip was previously uploaded by **publish-AzVMDscConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="f3ed9-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="f3ed9-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3ed9-121">PARAMETERS</span></span>

### <span data-ttu-id="f3ed9-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="f3ed9-122">-ArchiveBlobName</span></span>
<span data-ttu-id="f3ed9-123">Указывает имя файла конфигурации, который ранее был добавлен Publish-AzVMDscConfiguration этим Publish-AzVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="f3ed9-124">-ArchiveContainerName</span></span>
<span data-ttu-id="f3ed9-125">Имя вида контейнера хранилища Azure, в котором расположен архив конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ed9-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="f3ed9-127">Имя группы ресурсов, которая содержит учетную запись хранения, которая содержит архив конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="f3ed9-128">Этот параметр необязателен, если учетная запись хранения и виртуальная машину находятся в одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="f3ed9-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f3ed9-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="f3ed9-130">Имя учетной записи хранилища Azure, используемой для скачивания ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f3ed9-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="f3ed9-132">Определяет суффикс конечной точки хранения.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="f3ed9-133">-AutoUpdate</span></span>
<span data-ttu-id="f3ed9-134">Определяет версию обработера расширения, заданную параметром *Version.*</span><span class="sxs-lookup"><span data-stu-id="f3ed9-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="f3ed9-135">По умолчанию обработтель расширений не обрабатывается автоматически.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="f3ed9-136">Используйте параметр *автоматического обновления,* чтобы включить автоматическое обновление обработвода расширений до последней версии, как и когда он доступен.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="f3ed9-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="f3ed9-137">-ConfigurationArgument</span></span>
<span data-ttu-id="f3ed9-138">Указывает таблицу с hash table, которая содержит аргументы функции конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="f3ed9-139">-ConfigurationData</span></span>
<span data-ttu-id="f3ed9-140">Путь к PSD1-файлу, который определяет данные для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="f3ed9-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f3ed9-141">-ConfigurationName</span></span>
<span data-ttu-id="f3ed9-142">Указывает имя конфигурации, вызываемой расширением DSC.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="f3ed9-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="f3ed9-143">-DataCollection</span></span>
<span data-ttu-id="f3ed9-144">Тип сбора данных.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-144">Specifies the data collection type.</span></span>
<span data-ttu-id="f3ed9-145">Допустимые значения этого параметра: Enable (Включить) и Disable (Отключить).</span><span class="sxs-lookup"><span data-stu-id="f3ed9-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ed9-146">-DefaultProfile</span></span>
<span data-ttu-id="f3ed9-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3ed9-148">-Force</span><span class="sxs-lookup"><span data-stu-id="f3ed9-148">-Force</span></span>
<span data-ttu-id="f3ed9-149">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3ed9-150">-Location</span><span class="sxs-lookup"><span data-stu-id="f3ed9-150">-Location</span></span>
<span data-ttu-id="f3ed9-151">Путь к расширению ресурса.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="f3ed9-152">-Name</span><span class="sxs-lookup"><span data-stu-id="f3ed9-152">-Name</span></span>
<span data-ttu-id="f3ed9-153">Имя ресурса Диспетчера ресурсов Azure, представляюца расширение.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="f3ed9-154">Значение по умолчанию — Microsoft.Powershell.DSC.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="f3ed9-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f3ed9-155">-NoWait</span></span>
<span data-ttu-id="f3ed9-156">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f3ed9-157">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f3ed9-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ed9-158">-ResourceGroupName</span></span>
<span data-ttu-id="f3ed9-159">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-159">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-160">-Версия</span><span class="sxs-lookup"><span data-stu-id="f3ed9-160">-Version</span></span>
<span data-ttu-id="f3ed9-161">Определяет версию расширения DSC, к Set-AzVMDscExtension применяются параметры.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="f3ed9-162">-VMName</span></span>
<span data-ttu-id="f3ed9-163">Указывает имя виртуальной машины, на которой установлен обработчик расширения DSC.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="f3ed9-164">-WmfVersion</span></span>
<span data-ttu-id="f3ed9-165">Указывает версию WMF.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-165">Specifies the WMF version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed9-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3ed9-166">-Confirm</span></span>
<span data-ttu-id="f3ed9-167">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ed9-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ed9-168">-WhatIf</span></span>
<span data-ttu-id="f3ed9-169">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ed9-170">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ed9-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ed9-171">CommonParameters</span></span>
<span data-ttu-id="f3ed9-172">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ed9-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ed9-173">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3ed9-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ed9-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3ed9-174">INPUTS</span></span>

### <span data-ttu-id="f3ed9-175">System.String</span><span class="sxs-lookup"><span data-stu-id="f3ed9-175">System.String</span></span>

### <span data-ttu-id="f3ed9-176">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f3ed9-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f3ed9-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3ed9-177">OUTPUTS</span></span>

### <span data-ttu-id="f3ed9-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f3ed9-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f3ed9-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3ed9-179">NOTES</span></span>

## <span data-ttu-id="f3ed9-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3ed9-180">RELATED LINKS</span></span>

[<span data-ttu-id="f3ed9-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f3ed9-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="f3ed9-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f3ed9-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="f3ed9-183">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3ed9-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)

