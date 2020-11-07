---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: ed3215d6ae5b4e6386dc1ee9fce951f8b036d39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721684"
---
# <span data-ttu-id="294d0-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="294d0-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="294d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="294d0-102">SYNOPSIS</span></span>
<span data-ttu-id="294d0-103">Настраивает расширение диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="294d0-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="294d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="294d0-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="294d0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="294d0-105">DESCRIPTION</span></span>
<span data-ttu-id="294d0-106">Командлет **Set-AzVMDiagnosticsExtension** настраивает расширение диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="294d0-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="294d0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="294d0-107">EXAMPLES</span></span>

### <span data-ttu-id="294d0-108">Пример 1: включение диагностики с помощью учетной записи хранения, указанной в файле конфигурации диагностики</span><span class="sxs-lookup"><span data-stu-id="294d0-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="294d0-109">Эта команда использует файл конфигурации диагностики, чтобы включить диагностику.</span><span class="sxs-lookup"><span data-stu-id="294d0-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="294d0-110">Файл diagnostics_publicconfig.xml содержит конфигурацию общедоступного XML для расширения диагностики, включая имя учетной записи хранения, в которую будут отправлены диагностические данные.</span><span class="sxs-lookup"><span data-stu-id="294d0-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="294d0-111">Учетная запись хранения диагностики должна находиться в той же подписке, что и виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="294d0-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="294d0-112">Пример 2: включение диагностики с помощью имени учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="294d0-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="294d0-113">Эта команда использует имя учетной записи хранения, чтобы включить диагностику.</span><span class="sxs-lookup"><span data-stu-id="294d0-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="294d0-114">Если в конфигурации диагностики не указано имя учетной записи хранения или вы хотите переопределить имя учетной записи хранения диагностики, указанное в файле конфигурации, используйте параметр *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="294d0-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="294d0-115">Учетная запись хранения диагностики должна находиться в той же подписке, что и виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="294d0-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="294d0-116">Пример 3: включение диагностики с помощью имени и ключа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="294d0-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="294d0-117">Эта команда использует имя учетной записи хранения и ключ для включения диагностики.</span><span class="sxs-lookup"><span data-stu-id="294d0-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="294d0-118">Если учетная запись хранения диагностических данных находится в другой подписке, чем виртуальная машина, включите отправку диагностических данных в эту учетную запись хранения, явно указав ее имя и ключ.</span><span class="sxs-lookup"><span data-stu-id="294d0-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="294d0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="294d0-119">PARAMETERS</span></span>

### <span data-ttu-id="294d0-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="294d0-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="294d0-121">Указывает, допускает ли этот командлет Гостевой агент Azure автоматическое обновление расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="294d0-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294d0-122">-DefaultProfile</span></span>
<span data-ttu-id="294d0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="294d0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="294d0-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="294d0-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="294d0-125">Задает путь к файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="294d0-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-126">-Location</span><span class="sxs-lookup"><span data-stu-id="294d0-126">-Location</span></span>
<span data-ttu-id="294d0-127">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="294d0-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="294d0-128">-Name</span></span>
<span data-ttu-id="294d0-129">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="294d0-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="294d0-130">-NoWait</span></span>
<span data-ttu-id="294d0-131">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="294d0-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="294d0-132">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="294d0-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="294d0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="294d0-133">-ResourceGroupName</span></span>
<span data-ttu-id="294d0-134">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="294d0-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="294d0-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="294d0-136">Указывает конечную точку учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="294d0-136">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="294d0-137">-StorageAccountKey</span></span>
<span data-ttu-id="294d0-138">Указывает ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="294d0-138">Specifies the storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="294d0-139">-StorageAccountName</span></span>
<span data-ttu-id="294d0-140">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="294d0-140">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="294d0-141">-StorageContext</span></span>
<span data-ttu-id="294d0-142">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="294d0-142">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="294d0-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="294d0-144">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="294d0-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="294d0-145">Чтобы получить версию, выполните командлет Get-AzVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .</span><span class="sxs-lookup"><span data-stu-id="294d0-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="294d0-146">-VMName</span></span>
<span data-ttu-id="294d0-147">Указывает имя виртуальной машины, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="294d0-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294d0-148">CommonParameters</span></span>
<span data-ttu-id="294d0-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="294d0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294d0-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="294d0-150">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294d0-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="294d0-151">INPUTS</span></span>

### <span data-ttu-id="294d0-152">System. String</span><span class="sxs-lookup"><span data-stu-id="294d0-152">System.String</span></span>

### <span data-ttu-id="294d0-153">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="294d0-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="294d0-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="294d0-154">System.Boolean</span></span>

## <span data-ttu-id="294d0-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="294d0-155">OUTPUTS</span></span>

### <span data-ttu-id="294d0-156">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="294d0-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="294d0-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="294d0-157">NOTES</span></span>

## <span data-ttu-id="294d0-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="294d0-158">RELATED LINKS</span></span>

[<span data-ttu-id="294d0-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="294d0-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="294d0-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="294d0-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="294d0-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="294d0-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


