---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5705d899f06d4a834b8864ec2a66c268e1c99c84
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413831"
---
# <span data-ttu-id="e9b91-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e9b91-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="e9b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9b91-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b91-103">Настраивает расширение диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e9b91-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="e9b91-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9b91-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9b91-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9b91-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b91-106">С **помощью cmdlet Set-AzVMDiagnosticsExtension** можно настроить расширение диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e9b91-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="e9b91-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9b91-107">EXAMPLES</span></span>

### <span data-ttu-id="e9b91-108">Пример 1. Включить диагностику с использованием учетной записи хранения, указанной в файле конфигурации диагностики</span><span class="sxs-lookup"><span data-stu-id="e9b91-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="e9b91-109">Эта команда использует файл конфигурации диагностики для обеспечения диагностики.</span><span class="sxs-lookup"><span data-stu-id="e9b91-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="e9b91-110">Файл diagnostics_publicconfig.xml содержит общедоступный XML-файл для расширения диагностики, включая имя учетной записи хранения, в которую будут отправлены диагностические данные.</span><span class="sxs-lookup"><span data-stu-id="e9b91-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="e9b91-111">Учетная запись хранения диагностики должна быть в той же подписке, что и виртуальная машинка.</span><span class="sxs-lookup"><span data-stu-id="e9b91-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="e9b91-112">Пример 2. Включить диагностику с использованием имени учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e9b91-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="e9b91-113">Эта команда использует имя учетной записи хранения, чтобы включить диагностику.</span><span class="sxs-lookup"><span data-stu-id="e9b91-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="e9b91-114">Если в конфигурации диагностики не указано имя учетной записи хранения или вы хотите переопрединить имя учетной записи хранилища диагностики, указанное в файле конфигурации, используйте параметр *StorageAccountName.*</span><span class="sxs-lookup"><span data-stu-id="e9b91-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="e9b91-115">Учетная запись хранения диагностики должна быть в той же подписке, что и виртуальная машинка.</span><span class="sxs-lookup"><span data-stu-id="e9b91-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="e9b91-116">Пример 3. Включить диагностику с использованием имени учетной записи хранения и ключа</span><span class="sxs-lookup"><span data-stu-id="e9b91-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="e9b91-117">Эта команда использует имя учетной записи хранения и ключ для диагностики.</span><span class="sxs-lookup"><span data-stu-id="e9b91-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="e9b91-118">Если учетная запись хранения диагностики находится в другой подписке, а не на виртуальной машине, в этой учетной записи можно отправлять диагностические данные, явно указав ее имя и ключ.</span><span class="sxs-lookup"><span data-stu-id="e9b91-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="e9b91-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9b91-119">PARAMETERS</span></span>

### <span data-ttu-id="e9b91-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e9b91-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e9b91-121">Указывает, разрешает ли этот cmdlet агенту гостей Azure автоматически обновлять расширение до более новой версии.</span><span class="sxs-lookup"><span data-stu-id="e9b91-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="e9b91-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b91-122">-DefaultProfile</span></span>
<span data-ttu-id="e9b91-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b91-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9b91-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="e9b91-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="e9b91-125">Путь к файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e9b91-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="e9b91-126">-Location</span><span class="sxs-lookup"><span data-stu-id="e9b91-126">-Location</span></span>
<span data-ttu-id="e9b91-127">Определяет расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e9b91-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="e9b91-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e9b91-128">-Name</span></span>
<span data-ttu-id="e9b91-129">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="e9b91-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="e9b91-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e9b91-130">-NoWait</span></span>
<span data-ttu-id="e9b91-131">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="e9b91-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e9b91-132">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="e9b91-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e9b91-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b91-133">-ResourceGroupName</span></span>
<span data-ttu-id="e9b91-134">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e9b91-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e9b91-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9b91-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="e9b91-136">Указывает конечную точку учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e9b91-136">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="e9b91-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e9b91-137">-StorageAccountKey</span></span>
<span data-ttu-id="e9b91-138">Указывает ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e9b91-138">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="e9b91-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e9b91-139">-StorageAccountName</span></span>
<span data-ttu-id="e9b91-140">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e9b91-140">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="e9b91-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e9b91-141">-StorageContext</span></span>
<span data-ttu-id="e9b91-142">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b91-142">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="e9b91-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e9b91-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="e9b91-144">Определяет версию расширения, используемого для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e9b91-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="e9b91-145">Чтобы получить версию, запустите Get-AzVMExtensionImage Microsoft.Compute для параметра *PublisherName* и VMAccessAgent для параметра *Type.*</span><span class="sxs-lookup"><span data-stu-id="e9b91-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="e9b91-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="e9b91-146">-VMName</span></span>
<span data-ttu-id="e9b91-147">Указывает имя виртуальной машины, на которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9b91-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e9b91-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b91-148">CommonParameters</span></span>
<span data-ttu-id="e9b91-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b91-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b91-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9b91-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b91-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9b91-151">INPUTS</span></span>

### <span data-ttu-id="e9b91-152">System.String</span><span class="sxs-lookup"><span data-stu-id="e9b91-152">System.String</span></span>

### <span data-ttu-id="e9b91-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9b91-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="e9b91-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e9b91-154">System.Boolean</span></span>

## <span data-ttu-id="e9b91-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9b91-155">OUTPUTS</span></span>

### <span data-ttu-id="e9b91-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e9b91-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e9b91-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9b91-157">NOTES</span></span>

## <span data-ttu-id="e9b91-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9b91-158">RELATED LINKS</span></span>

[<span data-ttu-id="e9b91-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e9b91-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="e9b91-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="e9b91-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="e9b91-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e9b91-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


