---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 423cb695e4dedb978c3902e9c2f2c891a977464c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731984"
---
# <span data-ttu-id="1f45e-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="1f45e-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="1f45e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f45e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f45e-103">Добавляет секрет в VMSS.</span><span class="sxs-lookup"><span data-stu-id="1f45e-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f45e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f45e-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f45e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f45e-105">DESCRIPTION</span></span>
<span data-ttu-id="1f45e-106">Командлет **Add-AzureRmVmssSecret** добавляет секрет в набор масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1f45e-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="1f45e-107">Секрет должен храниться в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="1f45e-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="1f45e-108">Дополнительные сведения о хранилище ключей можно найти в разделе [что такое Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="1f45e-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="1f45e-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="1f45e-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="1f45e-110">Дополнительные сведения о командлетах можно найти в статьях [командлетов Azure Key Vault](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) в сетевой библиотеке разработчиков Microsoft Developer или командлет [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="1f45e-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="1f45e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f45e-111">EXAMPLES</span></span>

### <span data-ttu-id="1f45e-112">Пример 1: Добавление секрета в VMSS</span><span class="sxs-lookup"><span data-stu-id="1f45e-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="1f45e-113">В этом примере в VMSS добавляется секрет.</span><span class="sxs-lookup"><span data-stu-id="1f45e-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="1f45e-114">Первая команда использует командлет Get-AzureRmKeyVault для получения секрета из хранилища с именем ContosoVault и сохраняет результат в переменной с именем $Vault.</span><span class="sxs-lookup"><span data-stu-id="1f45e-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="1f45e-115">Вторая команда использует командлет **New-AzureRmVmssVaultCertificateConfig** для создания конфигурации сертификата хранилища ключей с помощью указанного URL-адреса сертификата из хранилища сертификатов с именем Certificates и сохраняет результаты в переменной с именем $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="1f45e-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="1f45e-116">Третья команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="1f45e-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="1f45e-117">Четвертая команда добавляет секрет в VMSS с помощью секретного ключа хранилища, используя идентификатор ресурса Key и сертификат хранилища, хранящийся в переменных $Vault и $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="1f45e-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="1f45e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f45e-118">PARAMETERS</span></span>

### <span data-ttu-id="1f45e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f45e-119">-DefaultProfile</span></span>
<span data-ttu-id="1f45e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f45e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f45e-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1f45e-121">-SourceVaultId</span></span>
<span data-ttu-id="1f45e-122">Указывает идентификатор ресурса для хранилища ключей, содержащего сертификаты, которые можно добавить на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="1f45e-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="1f45e-123">Это значение также действует в качестве ключа для добавления нескольких сертификатов.</span><span class="sxs-lookup"><span data-stu-id="1f45e-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="1f45e-124">Это означает, что вы можете использовать одно и то же значение для параметра *SourceVaultId* при добавлении нескольких сертификатов из одного и того же хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1f45e-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f45e-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1f45e-125">-VaultCertificate</span></span>
<span data-ttu-id="1f45e-126">Указывает объект **сертификата** хранилища, который содержит URL-адрес сертификата и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="1f45e-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="1f45e-127">Чтобы создать этот объект, можно использовать командлет [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="1f45e-127">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f45e-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1f45e-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1f45e-129">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="1f45e-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="1f45e-130">Чтобы создать этот объект, можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="1f45e-130">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f45e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f45e-131">-Confirm</span></span>
<span data-ttu-id="1f45e-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f45e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f45e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f45e-133">-WhatIf</span></span>
<span data-ttu-id="1f45e-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f45e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f45e-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f45e-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f45e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f45e-136">CommonParameters</span></span>
<span data-ttu-id="1f45e-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f45e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f45e-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f45e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f45e-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f45e-139">INPUTS</span></span>

### <span data-ttu-id="1f45e-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1f45e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="1f45e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1f45e-141">System.String</span></span>

### <span data-ttu-id="1f45e-142">Microsoft. Azure. Management. COMPUTE. Models. VaultCertificate []</span><span class="sxs-lookup"><span data-stu-id="1f45e-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="1f45e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f45e-143">OUTPUTS</span></span>

### <span data-ttu-id="1f45e-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1f45e-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1f45e-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f45e-145">NOTES</span></span>

## <span data-ttu-id="1f45e-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f45e-146">RELATED LINKS</span></span>

[<span data-ttu-id="1f45e-147">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="1f45e-147">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="1f45e-148">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1f45e-148">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
