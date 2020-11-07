---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 70342620aeab42ba7236091e8aacc32ea44354ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914637"
---
# <span data-ttu-id="0c4c3-101">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="0c4c3-101">Add-AzureRmVMSecret</span></span>

## <span data-ttu-id="0c4c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c4c3-102">SYNOPSIS</span></span>
<span data-ttu-id="0c4c3-103">Добавляет секрет для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-103">Adds a secret to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c4c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c4c3-104">SYNTAX</span></span>

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c4c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c4c3-105">DESCRIPTION</span></span>
<span data-ttu-id="0c4c3-106">Командлет **Add-AzureRmVMSecret** добавляет секрет на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-106">The **Add-AzureRmVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="0c4c3-107">Это значение позволяет добавить сертификат на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="0c4c3-108">Секрет должен храниться в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="0c4c3-109">Дополнительные сведения о хранилище ключей можно найти в разделе [что такое Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="0c4c3-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="0c4c3-110">Дополнительные сведения о командлетах можно найти в статьях [командлетов Azure Key Vault](https://msdn.microsoft.com/library/azure/dn868052.aspx) в сетевой библиотеке разработчиков Microsoft или командлете [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="0c4c3-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="0c4c3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c4c3-111">EXAMPLES</span></span>

### <span data-ttu-id="0c4c3-112">Пример 1: Добавление секрета на виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="0c4c3-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="0c4c3-113">В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0c4c3-114">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="0c4c3-115">Вторая команда создает объект учетных данных с помощью командлета Get-Credential и сохраняет результат в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="0c4c3-116">В командной строке будет предложено ввести имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="0c4c3-117">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="0c4c3-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="0c4c3-118">Третья команда использует командлет **Set-AzureRmVMOperatingSystem** для настройки виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-118">The third command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="0c4c3-119">Четвертая команда назначает идентификатор исходного хранилища переменной $SourceVaultId для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="0c4c3-120">Предполагается, что переменной $SubscriptionId присвоено нужное значение.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="0c4c3-121">Пятая команда присваивает значение переменной $CertificateStore 01 для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="0c4c3-122">Шестая команда назначает URL-адрес для хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="0c4c3-123">Седьмая команда добавляет секрет на виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="0c4c3-124">Параметр SourceVaultId указывает хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="0c4c3-125">Команда задает имя хранилища сертификатов и URL-адрес сертификата.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="0c4c3-126">Вы можете повторно запустить **надстройку "AzureRmVMSecret** ", чтобы добавить секреты для других сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-126">You can run the **Add-AzureRmVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="0c4c3-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c4c3-127">PARAMETERS</span></span>

### <span data-ttu-id="0c4c3-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="0c4c3-128">-CertificateStore</span></span>
<span data-ttu-id="0c4c3-129">Указывает имя хранилища сертификатов на виртуальной машине, работающей под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="0c4c3-130">Этот командлет добавляет сертификат в хранилище, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="0c4c3-131">Этот параметр можно задать только для виртуальных машин, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4c3-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="0c4c3-132">-CertificateUrl</span></span>
<span data-ttu-id="0c4c3-133">Указывает URL-адрес, указывающий на секретный ключ хранилища, который содержит сертификат.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="0c4c3-134">Сертификат — это кодировка Base64 следующего объекта JSON, который кодируется в кодировке UTF-8.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="0c4c3-135">{"Data": " \<Base64-encoded-file\> ", "тип данных": "" \<file-format\> , "пароль": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="0c4c3-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="0c4c3-136">В настоящее время тип данных принимает только PFX-файлы.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-136">Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4c3-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c4c3-137">-DefaultProfile</span></span>
<span data-ttu-id="0c4c3-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4c3-139">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0c4c3-139">-SourceVaultId</span></span>
<span data-ttu-id="0c4c3-140">Указывает идентификатор ресурса для хранилища ключей, содержащего сертификаты, которые можно добавить на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-140">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="0c4c3-141">Это значение также действует в качестве ключа для добавления нескольких сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-141">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="0c4c3-142">Это означает, что вы можете использовать одно и то же значение для *SourceVaultId* при добавлении нескольких сертификатов из одного и того же хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-142">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4c3-143">-VM</span><span class="sxs-lookup"><span data-stu-id="0c4c3-143">-VM</span></span>
<span data-ttu-id="0c4c3-144">Указывает объект виртуальной машины, измененный этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-144">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="0c4c3-145">Чтобы получить объект виртуальной машины, используйте командлет [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="0c4c3-145">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="0c4c3-146">Вы можете использовать командлет [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-146">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4c3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c4c3-147">CommonParameters</span></span>
<span data-ttu-id="0c4c3-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c4c3-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c4c3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c4c3-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c4c3-150">INPUTS</span></span>

### <span data-ttu-id="0c4c3-151">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0c4c3-151">PSVirtualMachine</span></span>
<span data-ttu-id="0c4c3-152">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0c4c3-152">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="0c4c3-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c4c3-153">OUTPUTS</span></span>

### <span data-ttu-id="0c4c3-154">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0c4c3-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0c4c3-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c4c3-155">NOTES</span></span>

## <span data-ttu-id="0c4c3-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c4c3-156">RELATED LINKS</span></span>

[<span data-ttu-id="0c4c3-157">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c4c3-157">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0c4c3-158">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="0c4c3-158">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="0c4c3-159">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="0c4c3-159">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)
