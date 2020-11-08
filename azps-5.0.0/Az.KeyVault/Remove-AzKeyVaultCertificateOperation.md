---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 43b4fae77aa0bf6ed76280ce633d3e1c3397e502
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249051"
---
# <span data-ttu-id="20868-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="20868-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="20868-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20868-102">SYNOPSIS</span></span>
<span data-ttu-id="20868-103">Удаляет операцию с сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="20868-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="20868-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20868-104">SYNTAX</span></span>

### <span data-ttu-id="20868-105">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="20868-105">Default</span></span>
```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20868-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="20868-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20868-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20868-107">DESCRIPTION</span></span>
<span data-ttu-id="20868-108">Командлет **Remove-AzKeyVaultCertificateOperation** удаляет операцию с сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="20868-108">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="20868-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20868-109">EXAMPLES</span></span>

### <span data-ttu-id="20868-110">Пример 1: Удаление операции с сертификатом</span><span class="sxs-lookup"><span data-stu-id="20868-110">Example 1: Remove a certificate operation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force

Id                        : https://contosokv01.vault.azure.net/certificates/testcert01/pending
Status                    : completed
StatusDetails             :
RequestId                 : f5dfd2ae486149a594dc98e800dceaaa
Target                    : https://contosokv01.vault.azure.net/certificates/testcert01
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
                            ==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="20868-111">Эта команда удаляет операцию с сертификатом с именем TestCert01 из хранилища ключей ContosoKV01 без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="20868-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="20868-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20868-112">PARAMETERS</span></span>

### <span data-ttu-id="20868-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20868-113">-DefaultProfile</span></span>
<span data-ttu-id="20868-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="20868-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20868-115">-Force</span><span class="sxs-lookup"><span data-stu-id="20868-115">-Force</span></span>
<span data-ttu-id="20868-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="20868-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20868-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20868-117">-InputObject</span></span>
<span data-ttu-id="20868-118">Объект Operation</span><span class="sxs-lookup"><span data-stu-id="20868-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20868-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20868-119">-Name</span></span>
<span data-ttu-id="20868-120">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="20868-120">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20868-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20868-121">-PassThru</span></span>
<span data-ttu-id="20868-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="20868-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20868-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="20868-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20868-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="20868-124">-VaultName</span></span>
<span data-ttu-id="20868-125">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="20868-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20868-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20868-126">-Confirm</span></span>
<span data-ttu-id="20868-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20868-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20868-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20868-128">-WhatIf</span></span>
<span data-ttu-id="20868-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20868-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20868-130">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20868-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20868-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20868-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20868-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20868-132">CommonParameters</span></span>
<span data-ttu-id="20868-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20868-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20868-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20868-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20868-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20868-135">INPUTS</span></span>

### <span data-ttu-id="20868-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="20868-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="20868-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20868-137">OUTPUTS</span></span>

### <span data-ttu-id="20868-138">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="20868-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="20868-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="20868-139">NOTES</span></span>

## <span data-ttu-id="20868-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20868-140">RELATED LINKS</span></span>

[<span data-ttu-id="20868-141">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="20868-141">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="20868-142">Остановить-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="20868-142">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

