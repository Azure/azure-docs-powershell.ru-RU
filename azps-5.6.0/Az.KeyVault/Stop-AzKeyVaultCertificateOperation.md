---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: c5b5b924968d444890338d8110f0a9cb9e416253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012072"
---
# <span data-ttu-id="c9c2d-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c9c2d-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="c9c2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c2d-103">Отмена операции с сертификатом в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="c9c2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c9c2d-104">SYNTAX</span></span>

### <span data-ttu-id="c9c2d-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9c2d-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c2d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c9c2d-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c2d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9c2d-107">DESCRIPTION</span></span>
<span data-ttu-id="c9c2d-108">Cmdlet **Stop-AzKeyVaultCertificateOperation** отменяет операцию сертификата в службе хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="c9c2d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c9c2d-109">EXAMPLES</span></span>

### <span data-ttu-id="c9c2d-110">Пример 1. Отмена операции с сертификатом</span><span class="sxs-lookup"><span data-stu-id="c9c2d-110">Example 1: Cancel a certificate operation</span></span>
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

<span data-ttu-id="c9c2d-111">Эта команда отменяет операцию сертификата TestCert02.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="c9c2d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9c2d-112">PARAMETERS</span></span>

### <span data-ttu-id="c9c2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c2d-113">-DefaultProfile</span></span>
<span data-ttu-id="c9c2d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c9c2d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9c2d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c9c2d-115">-Force</span></span>
<span data-ttu-id="c9c2d-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c9c2d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9c2d-117">-InputObject</span></span>
<span data-ttu-id="c9c2d-118">Объект Operation</span><span class="sxs-lookup"><span data-stu-id="c9c2d-118">Operation object</span></span>

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

### <span data-ttu-id="c9c2d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c9c2d-119">-Name</span></span>
<span data-ttu-id="c9c2d-120">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="c9c2d-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c9c2d-121">-VaultName</span></span>
<span data-ttu-id="c9c2d-122">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-122">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c9c2d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9c2d-123">-Confirm</span></span>
<span data-ttu-id="c9c2d-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c2d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c2d-125">-WhatIf</span></span>
<span data-ttu-id="c9c2d-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c2d-127">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c2d-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c2d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c2d-129">CommonParameters</span></span>
<span data-ttu-id="c9c2d-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c2d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c2d-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9c2d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c2d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9c2d-132">INPUTS</span></span>

### <span data-ttu-id="c9c2d-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c9c2d-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="c9c2d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9c2d-134">OUTPUTS</span></span>

### <span data-ttu-id="c9c2d-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c9c2d-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="c9c2d-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c9c2d-136">NOTES</span></span>

## <span data-ttu-id="c9c2d-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9c2d-137">RELATED LINKS</span></span>

[<span data-ttu-id="c9c2d-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c9c2d-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="c9c2d-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c9c2d-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

