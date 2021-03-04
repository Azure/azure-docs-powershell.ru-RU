---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: ec07964f62a22385d98c8cd9b8c98ea0b088ec8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969528"
---
# <span data-ttu-id="a13b5-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="a13b5-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="a13b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a13b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a13b5-103">Добавляет секрет в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a13b5-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="a13b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a13b5-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a13b5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a13b5-105">DESCRIPTION</span></span>
<span data-ttu-id="a13b5-106">Этот **cmdlet добавляет** секрет в набор масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a13b5-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a13b5-107">Секрет должен храниться в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="a13b5-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="a13b5-108">Дополнительные сведения, связанные с хранилищем ключей, см. в [подмносях "Что такое хранилище ключей Azure"?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="a13b5-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="a13b5-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="a13b5-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="a13b5-110">Дополнительные сведения о [cmdlets](/powershell/module/az.keyvault/set-azkeyvaultsecret) см. в [cmdlets хранилища](/powershell/module/az.keyvault) ключей Azure или в этом наборе.</span><span class="sxs-lookup"><span data-stu-id="a13b5-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="a13b5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a13b5-111">EXAMPLES</span></span>

### <span data-ttu-id="a13b5-112">Пример 1. Добавление секрета в VMSS</span><span class="sxs-lookup"><span data-stu-id="a13b5-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="a13b5-113">Этот пример добавляет секрет к службам VMSS.</span><span class="sxs-lookup"><span data-stu-id="a13b5-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="a13b5-114">Первая команда использует Get-AzKeyVault для получения секретного сейфа из сейфа ContosoVault и сохраняет результат в переменной с именем $Vault.</span><span class="sxs-lookup"><span data-stu-id="a13b5-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="a13b5-115">Вторая команда использует командлет **New-AzVmssVaultCertificateConfig** для создания конфигурации сертификата хранилища ключей с использованием указанного URL-адреса сертификата из хранилища сертификатов с именем Certificates и хранения результатов в переменной с именем $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="a13b5-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="a13b5-116">Третья команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="a13b5-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="a13b5-117">Четвертая команда добавляет секрет в VMSS с использованием секрета сейфа, используя ключ ресурса и сертификат хранилища, $Vault и $CertConfig переменных.</span><span class="sxs-lookup"><span data-stu-id="a13b5-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="a13b5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a13b5-118">PARAMETERS</span></span>

### <span data-ttu-id="a13b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a13b5-119">-DefaultProfile</span></span>
<span data-ttu-id="a13b5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a13b5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a13b5-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a13b5-121">-SourceVaultId</span></span>
<span data-ttu-id="a13b5-122">Определяет ИД ресурса хранилища ключей, который содержит сертификаты, которые можно добавить на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a13b5-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="a13b5-123">Это значение также является ключом для добавления нескольких сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a13b5-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="a13b5-124">Это означает, что для параметра *SourceVaultId* можно использовать одинаковое значение при добавлении нескольких сертификатов из одного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a13b5-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="a13b5-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a13b5-125">-VaultCertificate</span></span>
<span data-ttu-id="a13b5-126">Указывает объект **сертификата хранилища,** содержащий URL-адрес сертификата и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="a13b5-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="a13b5-127">Для создания этого объекта можно использовать [cmdlet New-AzVmssVaultCertificateConfig.](./New-AzVmssVaultCertificateConfig.md)</span><span class="sxs-lookup"><span data-stu-id="a13b5-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="a13b5-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a13b5-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a13b5-129">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="a13b5-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="a13b5-130">Для создания этого объекта можно использовать [cmdlet New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="a13b5-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="a13b5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a13b5-131">-Confirm</span></span>
<span data-ttu-id="a13b5-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a13b5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a13b5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a13b5-133">-WhatIf</span></span>
<span data-ttu-id="a13b5-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a13b5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a13b5-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a13b5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a13b5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a13b5-136">CommonParameters</span></span>
<span data-ttu-id="a13b5-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a13b5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a13b5-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a13b5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a13b5-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a13b5-139">INPUTS</span></span>

### <span data-ttu-id="a13b5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="a13b5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a13b5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a13b5-141">System.String</span></span>

### <span data-ttu-id="a13b5-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span><span class="sxs-lookup"><span data-stu-id="a13b5-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="a13b5-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a13b5-143">OUTPUTS</span></span>

### <span data-ttu-id="a13b5-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="a13b5-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a13b5-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a13b5-145">NOTES</span></span>

## <span data-ttu-id="a13b5-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a13b5-146">RELATED LINKS</span></span>

[<span data-ttu-id="a13b5-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="a13b5-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="a13b5-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a13b5-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
