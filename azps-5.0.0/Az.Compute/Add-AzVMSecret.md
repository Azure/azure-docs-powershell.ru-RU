---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395447"
---
# <span data-ttu-id="18d35-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="18d35-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="18d35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18d35-102">SYNOPSIS</span></span>
<span data-ttu-id="18d35-103">Добавляет секрет для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="18d35-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="18d35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18d35-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18d35-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18d35-105">DESCRIPTION</span></span>
<span data-ttu-id="18d35-106">Командлет **Add-AzVMSecret** добавляет секрет на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="18d35-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="18d35-107">Это значение позволяет добавить сертификат на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="18d35-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="18d35-108">Секрет должен храниться в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="18d35-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="18d35-109">Дополнительные сведения о хранилище ключей можно найти в разделе [что такое Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="18d35-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="18d35-110">Дополнительные сведения о командлетах можно найти в статьях [командлетов Azure Key Vault](/powershell/module/az.keyvault) или командлет [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="18d35-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="18d35-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18d35-111">EXAMPLES</span></span>

### <span data-ttu-id="18d35-112">Пример 1: Добавление секрета на виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="18d35-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="18d35-113">В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="18d35-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="18d35-114">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="18d35-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="18d35-115">Вторая команда создает объект учетных данных с помощью командлета Get-Credential и сохраняет результат в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="18d35-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="18d35-116">В командной строке будет предложено ввести имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="18d35-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="18d35-117">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="18d35-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="18d35-118">Третья команда использует командлет **Set-AzVMOperatingSystem** для настройки виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="18d35-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="18d35-119">Четвертая команда назначает идентификатор исходного хранилища переменной $SourceVaultId для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="18d35-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="18d35-120">Предполагается, что переменной $SubscriptionId присвоено нужное значение.</span><span class="sxs-lookup"><span data-stu-id="18d35-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="18d35-121">Пятая команда присваивает значение переменной $CertificateStore 01 для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="18d35-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="18d35-122">Шестая команда назначает URL-адрес для хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="18d35-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="18d35-123">Седьмая команда добавляет секрет на виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="18d35-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="18d35-124">Параметр SourceVaultId указывает хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="18d35-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="18d35-125">Команда задает имя хранилища сертификатов и URL-адрес сертификата.</span><span class="sxs-lookup"><span data-stu-id="18d35-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="18d35-126">Вы можете повторно запустить **надстройку "AzVMSecret** ", чтобы добавить секреты для других сертификатов.</span><span class="sxs-lookup"><span data-stu-id="18d35-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="18d35-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18d35-127">PARAMETERS</span></span>

### <span data-ttu-id="18d35-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="18d35-128">-CertificateStore</span></span>
<span data-ttu-id="18d35-129">Указывает имя хранилища сертификатов на виртуальной машине, работающей под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="18d35-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="18d35-130">Этот командлет добавляет сертификат в хранилище, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="18d35-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="18d35-131">Этот параметр можно задать только для виртуальных машин, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="18d35-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d35-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="18d35-132">-CertificateUrl</span></span>
<span data-ttu-id="18d35-133">Указывает URL-адрес, указывающий на секретный ключ хранилища, который содержит сертификат.</span><span class="sxs-lookup"><span data-stu-id="18d35-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="18d35-134">Сертификат — это кодировка Base64 следующего объекта JSON, который кодируется в кодировке UTF-8: {"Data": "", "Password": "" \<Base64-encoded-file\> \<file-format\> , \<pfx-file-password\> в настоящее время DataType принимает только PFX-файлы.</span><span class="sxs-lookup"><span data-stu-id="18d35-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="18d35-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18d35-135">-DefaultProfile</span></span>
<span data-ttu-id="18d35-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18d35-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18d35-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="18d35-137">-SourceVaultId</span></span>
<span data-ttu-id="18d35-138">Указывает идентификатор ресурса для хранилища ключей, содержащего сертификаты, которые можно добавить на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="18d35-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="18d35-139">Это значение также действует в качестве ключа для добавления нескольких сертификатов.</span><span class="sxs-lookup"><span data-stu-id="18d35-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="18d35-140">Это означает, что вы можете использовать одно и то же значение для *SourceVaultId* при добавлении нескольких сертификатов из одного и того же хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="18d35-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d35-141">-VM</span><span class="sxs-lookup"><span data-stu-id="18d35-141">-VM</span></span>
<span data-ttu-id="18d35-142">Указывает объект виртуальной машины, измененный этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="18d35-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="18d35-143">Чтобы получить объект виртуальной машины, используйте командлет [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="18d35-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="18d35-144">Вы можете использовать командлет [New-AzVMConfig](./New-AzVMConfig.md) для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="18d35-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18d35-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d35-145">CommonParameters</span></span>
<span data-ttu-id="18d35-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18d35-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d35-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18d35-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d35-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18d35-148">INPUTS</span></span>

### <span data-ttu-id="18d35-149">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="18d35-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="18d35-150">System. String</span><span class="sxs-lookup"><span data-stu-id="18d35-150">System.String</span></span>

## <span data-ttu-id="18d35-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18d35-151">OUTPUTS</span></span>

### <span data-ttu-id="18d35-152">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="18d35-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="18d35-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="18d35-153">NOTES</span></span>

## <span data-ttu-id="18d35-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18d35-154">RELATED LINKS</span></span>

[<span data-ttu-id="18d35-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="18d35-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="18d35-156">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="18d35-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="18d35-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="18d35-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
