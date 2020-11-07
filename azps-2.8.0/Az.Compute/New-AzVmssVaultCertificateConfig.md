---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0afd599bd1af9b3f597e9753d1be1e8ae710e5bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721812"
---
# <span data-ttu-id="47822-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="47822-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="47822-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47822-102">SYNOPSIS</span></span>
<span data-ttu-id="47822-103">Создание конфигурации сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="47822-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="47822-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47822-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47822-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47822-105">DESCRIPTION</span></span>
<span data-ttu-id="47822-106">Командлет **New-AzVmssVaultCertificateConfig** указывает секрет, который должен быть размещен на виртуальных машинах с установленной масштабируемостью виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="47822-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="47822-107">Выходные данные этого командлета предназначены для использования с командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="47822-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="47822-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47822-108">EXAMPLES</span></span>

### <span data-ttu-id="47822-109">Пример 1: создание конфигурации сертификата для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="47822-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="47822-110">Эта команда создает конфигурацию сертификата хранилища ключей, в которой используется хранилище сертификатов с именем MyCerts, расположенное по указанному URL-адресу сертификата.</span><span class="sxs-lookup"><span data-stu-id="47822-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="47822-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47822-111">PARAMETERS</span></span>

### <span data-ttu-id="47822-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="47822-112">-CertificateStore</span></span>
<span data-ttu-id="47822-113">Указывает хранилище сертификатов на виртуальных машинах в масштабе, где он добавляется.</span><span class="sxs-lookup"><span data-stu-id="47822-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="47822-114">Это допустимо только для наборов масштабирования виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="47822-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="47822-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="47822-115">-CertificateUrl</span></span>
<span data-ttu-id="47822-116">Задает универсальный код ресурса (URI) сертификата, хранящегося в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="47822-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="47822-117">Это кодировка Base64 для следующего объекта JSON, который кодируется в КОДИРОВКе Base64-8: {"Data": "PFX \< -Encoded-Certificate", " \> Password": "XXXX \< -File-password \> "}</span><span class="sxs-lookup"><span data-stu-id="47822-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="47822-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47822-118">-DefaultProfile</span></span>
<span data-ttu-id="47822-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47822-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47822-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47822-120">-Confirm</span></span>
<span data-ttu-id="47822-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47822-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47822-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47822-122">-WhatIf</span></span>
<span data-ttu-id="47822-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47822-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47822-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47822-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47822-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47822-125">CommonParameters</span></span>
<span data-ttu-id="47822-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47822-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47822-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47822-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47822-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47822-128">INPUTS</span></span>

### <span data-ttu-id="47822-129">System. String</span><span class="sxs-lookup"><span data-stu-id="47822-129">System.String</span></span>

## <span data-ttu-id="47822-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47822-130">OUTPUTS</span></span>

### <span data-ttu-id="47822-131">Microsoft. Azure. Management. COMPUTE. Models. VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47822-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="47822-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="47822-132">NOTES</span></span>

## <span data-ttu-id="47822-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47822-133">RELATED LINKS</span></span>

[<span data-ttu-id="47822-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="47822-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
