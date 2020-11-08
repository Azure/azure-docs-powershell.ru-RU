---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e260b32e847705240d93451b32bef9ae31d7fa07
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236177"
---
# <span data-ttu-id="7d706-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d706-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7d706-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d706-102">SYNOPSIS</span></span>
<span data-ttu-id="7d706-103">Отменяет операцию с сертификатом в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="7d706-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="7d706-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d706-104">SYNTAX</span></span>

### <span data-ttu-id="7d706-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d706-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d706-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7d706-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d706-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d706-107">DESCRIPTION</span></span>
<span data-ttu-id="7d706-108">Командлет **Stop-AzKeyVaultCertificateOperation** отменяет операцию с сертификатом в службе хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="7d706-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="7d706-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d706-109">EXAMPLES</span></span>

### <span data-ttu-id="7d706-110">Пример 1: отмена операции с сертификатом</span><span class="sxs-lookup"><span data-stu-id="7d706-110">Example 1: Cancel a certificate operation</span></span>
```powershell
PS C:\> Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force

Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="7d706-111">Эта команда отменяет операцию с сертификатом TestCert02.</span><span class="sxs-lookup"><span data-stu-id="7d706-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="7d706-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d706-112">PARAMETERS</span></span>

### <span data-ttu-id="7d706-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d706-113">-DefaultProfile</span></span>
<span data-ttu-id="7d706-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d706-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d706-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7d706-115">-Force</span></span>
<span data-ttu-id="7d706-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7d706-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d706-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d706-117">-InputObject</span></span>
<span data-ttu-id="7d706-118">Объект Operation</span><span class="sxs-lookup"><span data-stu-id="7d706-118">Operation object</span></span>

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

### <span data-ttu-id="7d706-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d706-119">-Name</span></span>
<span data-ttu-id="7d706-120">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="7d706-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="7d706-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7d706-121">-VaultName</span></span>
<span data-ttu-id="7d706-122">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="7d706-122">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7d706-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d706-123">-Confirm</span></span>
<span data-ttu-id="7d706-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d706-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d706-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d706-125">-WhatIf</span></span>
<span data-ttu-id="7d706-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d706-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d706-127">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d706-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d706-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d706-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d706-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d706-129">CommonParameters</span></span>
<span data-ttu-id="7d706-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d706-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d706-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d706-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d706-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d706-132">INPUTS</span></span>

### <span data-ttu-id="7d706-133">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d706-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7d706-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d706-134">OUTPUTS</span></span>

### <span data-ttu-id="7d706-135">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d706-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7d706-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d706-136">NOTES</span></span>

## <span data-ttu-id="7d706-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d706-137">RELATED LINKS</span></span>

[<span data-ttu-id="7d706-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d706-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="7d706-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d706-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

