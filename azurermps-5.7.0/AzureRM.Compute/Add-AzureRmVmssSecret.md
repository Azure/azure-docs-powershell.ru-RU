---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 7fe1fd25801c2aa02ba6c1506f4792fda99d94de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732036"
---
# <span data-ttu-id="7ebc8-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="7ebc8-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="7ebc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ebc8-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebc8-103">Добавляет секрет в VMSS.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ebc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ebc8-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ebc8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ebc8-105">DESCRIPTION</span></span>
<span data-ttu-id="7ebc8-106">Командлет **Add-AzureRmVmssSecret** добавляет секрет в набор масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="7ebc8-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="7ebc8-107">Секрет должен храниться в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="7ebc8-108">Дополнительные сведения о хранилище ключей можно найти в разделе [что такое Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="7ebc8-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="7ebc8-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="7ebc8-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="7ebc8-110">Дополнительные сведения о командлетах можно найти в статьях [командлетов Azure Key Vault](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) в сетевой библиотеке разработчиков Microsoft Developer или командлет [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="7ebc8-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="7ebc8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ebc8-111">EXAMPLES</span></span>

### <span data-ttu-id="7ebc8-112">Пример 1: Добавление секрета в VMSS</span><span class="sxs-lookup"><span data-stu-id="7ebc8-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="7ebc8-113">В этом примере в VMSS добавляется секрет.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="7ebc8-114">Первая команда использует командлет Get-AzureRmKeyVault для получения секрета из хранилища с именем ContosoVault и сохраняет результат в переменной с именем $Vault.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="7ebc8-115">Вторая команда использует командлет **New-AzureRmVmssVaultCertificateConfig** для создания конфигурации сертификата хранилища ключей с помощью указанного URL-адреса сертификата из хранилища сертификатов с именем Certificates и сохраняет результаты в переменной с именем $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="7ebc8-116">Третья команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="7ebc8-117">Четвертая команда добавляет секрет в VMSS с помощью секретного ключа хранилища, используя идентификатор ресурса Key и сертификат хранилища, хранящийся в переменных $Vault и $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="7ebc8-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ebc8-118">PARAMETERS</span></span>

### <span data-ttu-id="7ebc8-119">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="7ebc8-119">-SourceVaultId</span></span>
<span data-ttu-id="7ebc8-120">Указывает идентификатор ресурса для хранилища ключей, содержащего сертификаты, которые можно добавить на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-120">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="7ebc8-121">Это значение также действует в качестве ключа для добавления нескольких сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-121">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="7ebc8-122">Это означает, что вы можете использовать одно и то же значение для параметра *SourceVaultId* при добавлении нескольких сертификатов из одного и того же хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-122">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebc8-123">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7ebc8-123">-VaultCertificate</span></span>
<span data-ttu-id="7ebc8-124">Указывает объект **сертификата** хранилища, который содержит URL-адрес сертификата и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-124">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="7ebc8-125">Чтобы создать этот объект, можно использовать командлет [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="7ebc8-125">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebc8-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7ebc8-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7ebc8-127">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-127">Specifies the VMSS object.</span></span>
<span data-ttu-id="7ebc8-128">Чтобы создать этот объект, можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="7ebc8-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebc8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ebc8-129">-Confirm</span></span>
<span data-ttu-id="7ebc8-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebc8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebc8-131">-WhatIf</span></span>
<span data-ttu-id="7ebc8-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ebc8-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebc8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebc8-134">CommonParameters</span></span>
<span data-ttu-id="7ebc8-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebc8-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ebc8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebc8-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ebc8-137">INPUTS</span></span>

### <span data-ttu-id="7ebc8-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="7ebc8-138">None</span></span>
<span data-ttu-id="7ebc8-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7ebc8-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ebc8-140">OUTPUTS</span></span>

###  
<span data-ttu-id="7ebc8-141">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7ebc8-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7ebc8-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ebc8-142">NOTES</span></span>

## <span data-ttu-id="7ebc8-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ebc8-143">RELATED LINKS</span></span>

[<span data-ttu-id="7ebc8-144">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="7ebc8-144">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="7ebc8-145">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7ebc8-145">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
