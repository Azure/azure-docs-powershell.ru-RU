---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 432e6ce1562a7f341cc9e121e1012354c5c67a93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910301"
---
# <span data-ttu-id="c4a56-101">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c4a56-101">Get-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="c4a56-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4a56-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a56-103">Возвращает состояние операции с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="c4a56-103">Gets the status of a certificate operation.</span></span>

## <span data-ttu-id="c4a56-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4a56-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4a56-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4a56-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a56-106">Командлет **Get-AzKeyVaultCertificateOperation** получает состояние операции с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="c4a56-106">The **Get-AzKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="c4a56-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4a56-107">EXAMPLES</span></span>

### <span data-ttu-id="c4a56-108">Пример 1: получение состояния операции с сертификатом</span><span class="sxs-lookup"><span data-stu-id="c4a56-108">Example 1: Get the status of a certificate operation</span></span>
```
PS C:\>Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="c4a56-109">Эта команда возвращает состояние операции сертификата для TestCert01 в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="c4a56-109">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="c4a56-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4a56-110">PARAMETERS</span></span>

### <span data-ttu-id="c4a56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a56-111">-DefaultProfile</span></span>
<span data-ttu-id="c4a56-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c4a56-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a56-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4a56-113">-Name</span></span>
<span data-ttu-id="c4a56-114">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="c4a56-114">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a56-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c4a56-115">-VaultName</span></span>
<span data-ttu-id="c4a56-116">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="c4a56-116">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a56-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a56-117">CommonParameters</span></span>
<span data-ttu-id="c4a56-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4a56-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a56-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a56-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a56-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4a56-120">INPUTS</span></span>

### <span data-ttu-id="c4a56-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="c4a56-121">None</span></span>
<span data-ttu-id="c4a56-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c4a56-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4a56-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4a56-123">OUTPUTS</span></span>

### <span data-ttu-id="c4a56-124">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c4a56-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="c4a56-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4a56-125">NOTES</span></span>

## <span data-ttu-id="c4a56-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4a56-126">RELATED LINKS</span></span>

[<span data-ttu-id="c4a56-127">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c4a56-127">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="c4a56-128">Остановить-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c4a56-128">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

