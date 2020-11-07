---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910304"
---
# <span data-ttu-id="25be2-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="25be2-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="25be2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25be2-102">SYNOPSIS</span></span>
<span data-ttu-id="25be2-103">Возвращает поставщика сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="25be2-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="25be2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25be2-104">SYNTAX</span></span>

### <span data-ttu-id="25be2-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25be2-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25be2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="25be2-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25be2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25be2-107">DESCRIPTION</span></span>
<span data-ttu-id="25be2-108">Командлет **Get-AzKeyVaultCertificateIssuer** получает определенного поставщика сертификата или всех поставщиков сертификатов для хранилища ключей в хранилище Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="25be2-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="25be2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25be2-109">EXAMPLES</span></span>

### <span data-ttu-id="25be2-110">Пример 1: получение имени поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="25be2-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="25be2-111">Эта команда получает издателя сертификата с именем TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="25be2-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="25be2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25be2-112">PARAMETERS</span></span>

### <span data-ttu-id="25be2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25be2-113">-DefaultProfile</span></span>
<span data-ttu-id="25be2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="25be2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25be2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25be2-115">-Name</span></span>
<span data-ttu-id="25be2-116">Указывает имя получаемого издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="25be2-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25be2-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="25be2-117">-VaultName</span></span>
<span data-ttu-id="25be2-118">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="25be2-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="25be2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25be2-119">CommonParameters</span></span>
<span data-ttu-id="25be2-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25be2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25be2-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25be2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25be2-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25be2-122">INPUTS</span></span>

### <span data-ttu-id="25be2-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="25be2-123">None</span></span>
<span data-ttu-id="25be2-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="25be2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25be2-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25be2-125">OUTPUTS</span></span>

### <span data-ttu-id="25be2-126">List<Microsoft. Azure. Commands. KeyVault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="25be2-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="25be2-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="25be2-127">NOTES</span></span>

## <span data-ttu-id="25be2-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25be2-128">RELATED LINKS</span></span>

[<span data-ttu-id="25be2-129">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="25be2-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="25be2-130">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="25be2-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


