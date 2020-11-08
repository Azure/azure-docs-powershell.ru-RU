---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 7b4c416b8a083b1cf64e9e23ccdf08f153a76261
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079097"
---
# <span data-ttu-id="c5aeb-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c5aeb-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="c5aeb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="c5aeb-103">Настраивает расширение DSC на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="c5aeb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5aeb-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5aeb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5aeb-105">DESCRIPTION</span></span>
<span data-ttu-id="c5aeb-106">Командлет **Set-AzVMDscExtension** настраивает расширение конфигурации Windows POWERSHELL (DSC) на виртуальной машине в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="c5aeb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5aeb-107">EXAMPLES</span></span>

### <span data-ttu-id="c5aeb-108">Пример 1: Настройка расширения DSC</span><span class="sxs-lookup"><span data-stu-id="c5aeb-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="c5aeb-109">Эта команда задает расширение DSC на виртуальной машине с именем VM07, чтобы скачать Sample.ps1.zip из учетной записи хранения с именем STG и контейнером по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="c5aeb-110">Команда вызывает конфигурацию с именем ConfigName.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="c5aeb-111">Файл Sample.ps1.zip был ранее загружен с помощью команды **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="c5aeb-112">Пример 2: Настройка расширения DSC с данными конфигурации</span><span class="sxs-lookup"><span data-stu-id="c5aeb-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="c5aeb-113">Эта команда задает расширение на виртуальной машине с именем VM13, чтобы скачать Sample.ps1.zip из учетной записи хранения с именем STG и контейнером с именем WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="c5aeb-114">Команда конфигурации с именем ConfigName и определяет данные конфигурации и аргументы.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="c5aeb-115">Файл Sample.ps1.zip был ранее загружен с помощью команды **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="c5aeb-116">Пример 3: Настройка расширения DSC с данными конфигурации с автоматическим обновлением</span><span class="sxs-lookup"><span data-stu-id="c5aeb-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="c5aeb-117">Эта команда задает расширение на виртуальной машине с именем VM22, чтобы скачать Sample.ps1.zip из учетной записи хранения с именем STG и контейнером с именем WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="c5aeb-118">Эта команда вызывает конфигурацию с именем ConfigName и определяет данные конфигурации и аргументы.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="c5aeb-119">Эта команда также позволяет автоматически обновлять обработчик расширений до последней версии.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="c5aeb-120">Sample.ps1.zip был ранее загружен с помощью команды **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="c5aeb-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5aeb-121">PARAMETERS</span></span>

### <span data-ttu-id="c5aeb-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="c5aeb-122">-ArchiveBlobName</span></span>
<span data-ttu-id="c5aeb-123">Указывает имя файла конфигурации, который ранее был загружен с помощью командлета Publish-AzVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="c5aeb-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="c5aeb-124">-ArchiveContainerName</span></span>
<span data-ttu-id="c5aeb-125">Форель имя контейнера хранилища Azure, в котором находится архив конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="c5aeb-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5aeb-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="c5aeb-127">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которая содержит архив конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="c5aeb-128">Этот параметр необязателен, если учетная запись хранения и виртуальная машина находятся в одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="c5aeb-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c5aeb-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="c5aeb-130">Указывает имя учетной записи хранения Azure, используемой для загрузки ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="c5aeb-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c5aeb-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="c5aeb-132">Указывает суффикс конечной точки хранилища.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="c5aeb-133">-Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="c5aeb-133">-AutoUpdate</span></span>
<span data-ttu-id="c5aeb-134">Указывает версию обработчика расширения, заданную параметром *Version* .</span><span class="sxs-lookup"><span data-stu-id="c5aeb-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="c5aeb-135">По умолчанию обработчик расширений не обновляется.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="c5aeb-136">С помощью параметра "автоматическое *Обновление* " Включите для автоматического обновления обработчика расширений самую последнюю версию и когда она доступна.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="c5aeb-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="c5aeb-137">-ConfigurationArgument</span></span>
<span data-ttu-id="c5aeb-138">Указывает хэш-таблицу, которая содержит аргументы для функции конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="c5aeb-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="c5aeb-139">-ConfigurationData</span></span>
<span data-ttu-id="c5aeb-140">Задает путь к файлу PSD1, который задает данные для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="c5aeb-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c5aeb-141">-ConfigurationName</span></span>
<span data-ttu-id="c5aeb-142">Указывает имя конфигурации, которую вызывает расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="c5aeb-143">-Коллекция</span><span class="sxs-lookup"><span data-stu-id="c5aeb-143">-DataCollection</span></span>
<span data-ttu-id="c5aeb-144">Указывает тип сбора данных.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-144">Specifies the data collection type.</span></span>
<span data-ttu-id="c5aeb-145">Допустимые значения этого параметра: Включение и отключение.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="c5aeb-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5aeb-146">-DefaultProfile</span></span>
<span data-ttu-id="c5aeb-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5aeb-148">-Force</span><span class="sxs-lookup"><span data-stu-id="c5aeb-148">-Force</span></span>
<span data-ttu-id="c5aeb-149">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5aeb-150">-Location</span><span class="sxs-lookup"><span data-stu-id="c5aeb-150">-Location</span></span>
<span data-ttu-id="c5aeb-151">Указывает путь к расширению ресурса.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="c5aeb-152">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5aeb-152">-Name</span></span>
<span data-ttu-id="c5aeb-153">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="c5aeb-154">Значением по умолчанию является Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="c5aeb-155">-Wait</span><span class="sxs-lookup"><span data-stu-id="c5aeb-155">-NoWait</span></span>
<span data-ttu-id="c5aeb-156">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c5aeb-157">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c5aeb-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5aeb-158">-ResourceGroupName</span></span>
<span data-ttu-id="c5aeb-159">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c5aeb-160">-Version</span><span class="sxs-lookup"><span data-stu-id="c5aeb-160">-Version</span></span>
<span data-ttu-id="c5aeb-161">Определяет версию расширения DSC, к которой Set-AzVMDscExtension применяются параметры.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="c5aeb-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="c5aeb-162">-VMName</span></span>
<span data-ttu-id="c5aeb-163">Указывает имя виртуальной машины, на которой установлен обработчик расширений DSC.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="c5aeb-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="c5aeb-164">-WmfVersion</span></span>
<span data-ttu-id="c5aeb-165">Указывает версию WMF.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-165">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="c5aeb-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5aeb-166">-Confirm</span></span>
<span data-ttu-id="c5aeb-167">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5aeb-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5aeb-168">-WhatIf</span></span>
<span data-ttu-id="c5aeb-169">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5aeb-170">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5aeb-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5aeb-171">CommonParameters</span></span>
<span data-ttu-id="c5aeb-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5aeb-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5aeb-173">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5aeb-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5aeb-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5aeb-174">INPUTS</span></span>

### <span data-ttu-id="c5aeb-175">System. String</span><span class="sxs-lookup"><span data-stu-id="c5aeb-175">System.String</span></span>

### <span data-ttu-id="c5aeb-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c5aeb-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c5aeb-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5aeb-177">OUTPUTS</span></span>

### <span data-ttu-id="c5aeb-178">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c5aeb-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c5aeb-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5aeb-179">NOTES</span></span>

## <span data-ttu-id="c5aeb-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5aeb-180">RELATED LINKS</span></span>

[<span data-ttu-id="c5aeb-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c5aeb-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="c5aeb-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c5aeb-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="c5aeb-183">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5aeb-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)

