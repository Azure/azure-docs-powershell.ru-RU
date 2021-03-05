---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: cc607e12873e0b5b738a64d781d16ed73bc72f7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988403"
---
# <span data-ttu-id="f4a94-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="f4a94-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="f4a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4a94-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a94-103">Создает конфигурацию сертификата хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f4a94-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="f4a94-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4a94-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a94-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4a94-105">DESCRIPTION</span></span>
<span data-ttu-id="f4a94-106">Новый **-AzVmssVaultCertificateConfig cmdlet** specifies the secret that that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual Machine Scale Set (VMSS) virtual machine Scale Set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f4a94-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="f4a94-107">Результат этого cmdlet предназначен для использования с этим Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="f4a94-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="f4a94-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4a94-108">EXAMPLES</span></span>

### <span data-ttu-id="f4a94-109">Пример 1. Создание конфигурации сертификата хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="f4a94-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="f4a94-110">Эта команда создает конфигурацию сертификата хранилища ключей с использованием хранилища сертификатов MyCerts, расположенного по указанному URL-адресу сертификата.</span><span class="sxs-lookup"><span data-stu-id="f4a94-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="f4a94-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4a94-111">PARAMETERS</span></span>

### <span data-ttu-id="f4a94-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="f4a94-112">-CertificateStore</span></span>
<span data-ttu-id="f4a94-113">Указывает хранилище сертификатов на виртуальных машинах в наборе масштаба, в который добавляется сертификат.</span><span class="sxs-lookup"><span data-stu-id="f4a94-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="f4a94-114">Это можно сделать только для наборов масштаба виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="f4a94-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="f4a94-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="f4a94-115">-CertificateUrl</span></span>
<span data-ttu-id="f4a94-116">Определяет URI сертификата, храняного в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f4a94-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="f4a94-117">Это базовая кодировки следующего объекта JSON, который закодирован в UTF-8: { "data":" \<Base64-encoded-certificate\> ", "dataType":"pfx", "password":" \<pfx-file-password\> " }</span><span class="sxs-lookup"><span data-stu-id="f4a94-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a94-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a94-118">-DefaultProfile</span></span>
<span data-ttu-id="f4a94-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a94-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4a94-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4a94-120">-Confirm</span></span>
<span data-ttu-id="f4a94-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f4a94-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a94-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a94-122">-WhatIf</span></span>
<span data-ttu-id="f4a94-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4a94-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4a94-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f4a94-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a94-125">CommonParameters</span></span>
<span data-ttu-id="f4a94-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a94-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4a94-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a94-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4a94-128">INPUTS</span></span>

### <span data-ttu-id="f4a94-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f4a94-129">System.String</span></span>

## <span data-ttu-id="f4a94-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4a94-130">OUTPUTS</span></span>

### <span data-ttu-id="f4a94-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f4a94-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="f4a94-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4a94-132">NOTES</span></span>

## <span data-ttu-id="f4a94-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4a94-133">RELATED LINKS</span></span>

[<span data-ttu-id="f4a94-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="f4a94-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
