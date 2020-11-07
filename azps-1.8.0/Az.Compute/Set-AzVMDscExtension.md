---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 75cd5e76fe4ebce1479525aba2c36e6741b6094b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731227"
---
# <span data-ttu-id="d2cf3-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d2cf3-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="d2cf3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="d2cf3-103">Настраивает расширение DSC на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="d2cf3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2cf3-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2cf3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="d2cf3-106">Командлет **Set-AzVMDscExtension** настраивает расширение конфигурации Windows POWERSHELL (DSC) на виртуальной машине в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="d2cf3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2cf3-107">EXAMPLES</span></span>

### <span data-ttu-id="d2cf3-108">Пример 1: Настройка расширения DSC</span><span class="sxs-lookup"><span data-stu-id="d2cf3-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="d2cf3-109">Эта команда задает расширение DSC на виртуальной машине с именем VM07, чтобы скачать Sample.ps1.zip из учетной записи хранения с именем STG и контейнером по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="d2cf3-110">Команда вызывает конфигурацию с именем ConfigName.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="d2cf3-111">Файл Sample.ps1.zip был ранее загружен с помощью команды **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="d2cf3-112">Пример 2: Настройка расширения DSC с данными конфигурации</span><span class="sxs-lookup"><span data-stu-id="d2cf3-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="d2cf3-113">Эта команда задает расширение на виртуальной машине с именем VM13, чтобы скачать Sample.ps1.zip из учетной записи хранения с именем STG и контейнером с именем WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="d2cf3-114">Команда конфигурации с именем ConfigName и определяет данные конфигурации и аргументы.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="d2cf3-115">Файл Sample.ps1.zip был ранее загружен с помощью команды **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="d2cf3-116">Пример 3: Настройка расширения DSC с данными конфигурации с автоматическим обновлением</span><span class="sxs-lookup"><span data-stu-id="d2cf3-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="d2cf3-117">Эта команда задает расширение на виртуальной машине с именем VM22, чтобы скачать Sample.ps1.zip из учетной записи хранения с именем STG и контейнером с именем WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="d2cf3-118">Эта команда вызывает конфигурацию с именем ConfigName и определяет данные конфигурации и аргументы.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="d2cf3-119">Эта команда также позволяет автоматически обновлять обработчик расширений до последней версии.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="d2cf3-120">Sample.ps1.zip был ранее загружен с помощью команды **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="d2cf3-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2cf3-121">PARAMETERS</span></span>

### <span data-ttu-id="d2cf3-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="d2cf3-122">-ArchiveBlobName</span></span>
<span data-ttu-id="d2cf3-123">Указывает имя файла конфигурации, который ранее был загружен с помощью командлета Publish-AzVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="d2cf3-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="d2cf3-124">-ArchiveContainerName</span></span>
<span data-ttu-id="d2cf3-125">Форель имя контейнера хранилища Azure, в котором находится архив конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="d2cf3-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2cf3-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="d2cf3-127">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которая содержит архив конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="d2cf3-128">Этот параметр необязателен, если учетная запись хранения и виртуальная машина находятся в одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="d2cf3-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2cf3-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="d2cf3-130">Указывает имя учетной записи хранения Azure, используемой для загрузки ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="d2cf3-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d2cf3-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="d2cf3-132">Указывает суффикс конечной точки хранилища.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="d2cf3-133">-Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="d2cf3-133">-AutoUpdate</span></span>
<span data-ttu-id="d2cf3-134">Указывает версию обработчика расширения, заданную параметром *Version* .</span><span class="sxs-lookup"><span data-stu-id="d2cf3-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="d2cf3-135">По умолчанию обработчик расширений не обновляется.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="d2cf3-136">С помощью параметра "автоматическое *Обновление* " Включите для автоматического обновления обработчика расширений самую последнюю версию и когда она доступна.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="d2cf3-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="d2cf3-137">-ConfigurationArgument</span></span>
<span data-ttu-id="d2cf3-138">Указывает хэш-таблицу, которая содержит аргументы для функции конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="d2cf3-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="d2cf3-139">-ConfigurationData</span></span>
<span data-ttu-id="d2cf3-140">Задает путь к файлу PSD1, который задает данные для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="d2cf3-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d2cf3-141">-ConfigurationName</span></span>
<span data-ttu-id="d2cf3-142">Указывает имя конфигурации, которую вызывает расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="d2cf3-143">-Коллекция</span><span class="sxs-lookup"><span data-stu-id="d2cf3-143">-DataCollection</span></span>
<span data-ttu-id="d2cf3-144">Указывает тип сбора данных.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-144">Specifies the data collection type.</span></span>
<span data-ttu-id="d2cf3-145">Допустимые значения этого параметра: Включение и отключение.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="d2cf3-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2cf3-146">-DefaultProfile</span></span>
<span data-ttu-id="d2cf3-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2cf3-148">-Force</span><span class="sxs-lookup"><span data-stu-id="d2cf3-148">-Force</span></span>
<span data-ttu-id="d2cf3-149">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2cf3-150">-Location</span><span class="sxs-lookup"><span data-stu-id="d2cf3-150">-Location</span></span>
<span data-ttu-id="d2cf3-151">Указывает путь к расширению ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="d2cf3-152">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2cf3-152">-Name</span></span>
<span data-ttu-id="d2cf3-153">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="d2cf3-154">Значением по умолчанию является Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="d2cf3-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2cf3-155">-ResourceGroupName</span></span>
<span data-ttu-id="d2cf3-156">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-156">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d2cf3-157">-Version</span><span class="sxs-lookup"><span data-stu-id="d2cf3-157">-Version</span></span>
<span data-ttu-id="d2cf3-158">Определяет версию расширения DSC, к которой Set-AzVMDscExtension применяются параметры.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-158">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="d2cf3-159">-VMName</span><span class="sxs-lookup"><span data-stu-id="d2cf3-159">-VMName</span></span>
<span data-ttu-id="d2cf3-160">Указывает имя виртуальной машины, на которой установлен обработчик расширений DSC.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-160">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="d2cf3-161">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="d2cf3-161">-WmfVersion</span></span>
<span data-ttu-id="d2cf3-162">Указывает версию WMF.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-162">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="d2cf3-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2cf3-163">-Confirm</span></span>
<span data-ttu-id="d2cf3-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2cf3-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2cf3-165">-WhatIf</span></span>
<span data-ttu-id="d2cf3-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2cf3-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2cf3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2cf3-168">CommonParameters</span></span>
<span data-ttu-id="d2cf3-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2cf3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2cf3-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2cf3-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2cf3-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2cf3-171">INPUTS</span></span>

### <span data-ttu-id="d2cf3-172">System. String</span><span class="sxs-lookup"><span data-stu-id="d2cf3-172">System.String</span></span>

### <span data-ttu-id="d2cf3-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d2cf3-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d2cf3-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2cf3-174">OUTPUTS</span></span>

### <span data-ttu-id="d2cf3-175">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d2cf3-175">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d2cf3-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2cf3-176">NOTES</span></span>

## <span data-ttu-id="d2cf3-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2cf3-177">RELATED LINKS</span></span>

[<span data-ttu-id="d2cf3-178">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d2cf3-178">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="d2cf3-179">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d2cf3-179">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="d2cf3-180">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2cf3-180">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


