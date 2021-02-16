---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233428"
---
# <span data-ttu-id="70bb7-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="70bb7-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="70bb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="70bb7-103">Добавляет секрет в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="70bb7-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="70bb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="70bb7-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70bb7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70bb7-105">DESCRIPTION</span></span>
<span data-ttu-id="70bb7-106">**Cmdlet Add-AzVMSecret** добавляет секрет в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="70bb7-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="70bb7-107">Это значение позволяет добавить сертификат на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="70bb7-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="70bb7-108">Секрет должен храниться в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="70bb7-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="70bb7-109">Дополнительные сведения о хранилище ключей см. в [подмносях "Хранилище ключей Azure".](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="70bb7-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="70bb7-110">Дополнительные сведения о cmdlets см. в [cmdlets key Vault Azure](/powershell/module/az.keyvault) или [set-AzKeyVaultSecret cmdlet.](/powershell/module/az.keyvault/set-azkeyvaultsecret)</span><span class="sxs-lookup"><span data-stu-id="70bb7-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="70bb7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="70bb7-111">EXAMPLES</span></span>

### <span data-ttu-id="70bb7-112">Пример 1. Добавление секрета на виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="70bb7-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="70bb7-113">Первая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="70bb7-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="70bb7-114">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="70bb7-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="70bb7-115">Вторая команда создает объект учетных данных с Get-Credential командлета, а затем сохраняет результат в $Credential переменной.</span><span class="sxs-lookup"><span data-stu-id="70bb7-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="70bb7-116">В командной области будет предложено вводить имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="70bb7-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="70bb7-117">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="70bb7-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="70bb7-118">Третья команда использует командлет **Set-AzVMOperatingSystem** для настройки виртуальной машины, $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="70bb7-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="70bb7-119">Четвертая команда назначает исходный ИД хранилища переменной $SourceVaultId для использования в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="70bb7-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="70bb7-120">Предполагается, что переменная $SubscriptionId имеет соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="70bb7-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="70bb7-121">Пятая команда назначает значение переменной $CertificateStore 01 для использования в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="70bb7-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="70bb7-122">Шестая команда назначает URL-адрес для магазина сертификатов.</span><span class="sxs-lookup"><span data-stu-id="70bb7-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="70bb7-123">Седьмой команда добавляет секрет к виртуальной машине, которая хранится в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="70bb7-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="70bb7-124">Параметр SourceVaultId определяет хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="70bb7-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="70bb7-125">Команда указывает имя магазина сертификатов и URL-адрес сертификата.</span><span class="sxs-lookup"><span data-stu-id="70bb7-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="70bb7-126">Вы можете несколько раз запустить **надстройку AzVMSecret,** чтобы добавить секрет других сертификатов.</span><span class="sxs-lookup"><span data-stu-id="70bb7-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="70bb7-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70bb7-127">PARAMETERS</span></span>

### <span data-ttu-id="70bb7-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="70bb7-128">-CertificateStore</span></span>
<span data-ttu-id="70bb7-129">Указывает имя магазина сертификатов на виртуальной машине, на которую работает операционная система Windows.</span><span class="sxs-lookup"><span data-stu-id="70bb7-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="70bb7-130">Этот cmdlet добавляет сертификат в хранилище, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="70bb7-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="70bb7-131">Этот параметр можно указать только для виртуальных машин, работающих в операционной системе Windows.</span><span class="sxs-lookup"><span data-stu-id="70bb7-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="70bb7-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="70bb7-132">-CertificateUrl</span></span>
<span data-ttu-id="70bb7-133">Указывает URL-адрес, который указывает на секрет ключного сейфа, который содержит сертификат.</span><span class="sxs-lookup"><span data-stu-id="70bb7-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="70bb7-134">Сертификат — это кодировки Base64 для следующего объекта нотации объектов JavaScript (JSON), который закодирован в UTF-8: { "data": \<Base64-encoded-file\> " ", "dataType": " ", "password": " " } В настоящее время dataType принимает только \<file-format\> \<pfx-file-password\> PFX-файлы.</span><span class="sxs-lookup"><span data-stu-id="70bb7-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="70bb7-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bb7-135">-DefaultProfile</span></span>
<span data-ttu-id="70bb7-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70bb7-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70bb7-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="70bb7-137">-SourceVaultId</span></span>
<span data-ttu-id="70bb7-138">Определяет ИД ресурса хранилища ключей, который содержит сертификаты, которые можно добавить на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="70bb7-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="70bb7-139">Это значение также является ключом для добавления нескольких сертификатов.</span><span class="sxs-lookup"><span data-stu-id="70bb7-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="70bb7-140">Это означает, что для *SourceVaultId* можно использовать одно и то же значение при добавлении нескольких сертификатов из одного сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="70bb7-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="70bb7-141">-VM</span><span class="sxs-lookup"><span data-stu-id="70bb7-141">-VM</span></span>
<span data-ttu-id="70bb7-142">Определяет объект виртуальной машины, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70bb7-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="70bb7-143">Чтобы получить объект виртуальной машины, используйте [cmdlet Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="70bb7-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="70bb7-144">Для создания объекта виртуальной машины можно использовать [cmdlet New-AzVMConfig.](./New-AzVMConfig.md)</span><span class="sxs-lookup"><span data-stu-id="70bb7-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="70bb7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bb7-145">CommonParameters</span></span>
<span data-ttu-id="70bb7-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70bb7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bb7-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70bb7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bb7-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70bb7-148">INPUTS</span></span>

### <span data-ttu-id="70bb7-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="70bb7-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="70bb7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="70bb7-150">System.String</span></span>

## <span data-ttu-id="70bb7-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="70bb7-151">OUTPUTS</span></span>

### <span data-ttu-id="70bb7-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="70bb7-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="70bb7-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="70bb7-153">NOTES</span></span>

## <span data-ttu-id="70bb7-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70bb7-154">RELATED LINKS</span></span>

[<span data-ttu-id="70bb7-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="70bb7-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="70bb7-156">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="70bb7-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="70bb7-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="70bb7-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
