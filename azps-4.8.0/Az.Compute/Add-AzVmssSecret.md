---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 6f9f1f29f23906442d7c9c8187b9bab3bf41403b
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395261"
---
# <span data-ttu-id="f7e1c-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="f7e1c-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="f7e1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e1c-103">Добавляет секрет в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="f7e1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7e1c-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7e1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e1c-106">Командлет **Add-AzVmssSecret** добавляет секрет в набор масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f7e1c-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f7e1c-107">Секрет должен храниться в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="f7e1c-108">Дополнительные сведения о хранилище ключей можно найти в разделе [что такое Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="f7e1c-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="f7e1c-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="f7e1c-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="f7e1c-110">Дополнительные сведения о командлетах можно найти в статьях [командлетов Azure Key Vault](/powershell/module/az.keyvault) или командлет [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="f7e1c-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="f7e1c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7e1c-111">EXAMPLES</span></span>

### <span data-ttu-id="f7e1c-112">Пример 1: Добавление секрета в VMSS</span><span class="sxs-lookup"><span data-stu-id="f7e1c-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="f7e1c-113">В этом примере в VMSS добавляется секрет.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="f7e1c-114">Первая команда использует командлет Get-AzKeyVault для получения секрета из хранилища с именем ContosoVault и сохраняет результат в переменной с именем $Vault.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="f7e1c-115">Вторая команда использует командлет **New-AzVmssVaultCertificateConfig** для создания конфигурации сертификата хранилища ключей с помощью указанного URL-адреса сертификата из хранилища сертификатов с именем Certificates и сохраняет результаты в переменной с именем $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="f7e1c-116">Третья команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="f7e1c-117">Четвертая команда добавляет секрет в VMSS с помощью секретного ключа хранилища, используя идентификатор ресурса Key и сертификат хранилища, хранящийся в переменных $Vault и $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="f7e1c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7e1c-118">PARAMETERS</span></span>

### <span data-ttu-id="f7e1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e1c-119">-DefaultProfile</span></span>
<span data-ttu-id="f7e1c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7e1c-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f7e1c-121">-SourceVaultId</span></span>
<span data-ttu-id="f7e1c-122">Указывает идентификатор ресурса для хранилища ключей, содержащего сертификаты, которые можно добавить на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="f7e1c-123">Это значение также действует в качестве ключа для добавления нескольких сертификатов.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="f7e1c-124">Это означает, что вы можете использовать одно и то же значение для параметра *SourceVaultId* при добавлении нескольких сертификатов из одного и того же хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="f7e1c-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f7e1c-125">-VaultCertificate</span></span>
<span data-ttu-id="f7e1c-126">Указывает объект **сертификата** хранилища, который содержит URL-адрес сертификата и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="f7e1c-127">Чтобы создать этот объект, можно использовать командлет [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="f7e1c-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="f7e1c-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f7e1c-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f7e1c-129">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="f7e1c-130">Чтобы создать этот объект, можно использовать командлет [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="f7e1c-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="f7e1c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7e1c-131">-Confirm</span></span>
<span data-ttu-id="f7e1c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7e1c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e1c-133">-WhatIf</span></span>
<span data-ttu-id="f7e1c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7e1c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7e1c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e1c-136">CommonParameters</span></span>
<span data-ttu-id="f7e1c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7e1c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e1c-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7e1c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e1c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7e1c-139">INPUTS</span></span>

### <span data-ttu-id="f7e1c-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f7e1c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="f7e1c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f7e1c-141">System.String</span></span>

### <span data-ttu-id="f7e1c-142">Microsoft. Azure. Management. COMPUTE. Models. VaultCertificate []</span><span class="sxs-lookup"><span data-stu-id="f7e1c-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="f7e1c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7e1c-143">OUTPUTS</span></span>

### <span data-ttu-id="f7e1c-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f7e1c-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f7e1c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7e1c-145">NOTES</span></span>

## <span data-ttu-id="f7e1c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7e1c-146">RELATED LINKS</span></span>

[<span data-ttu-id="f7e1c-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="f7e1c-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="f7e1c-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f7e1c-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
