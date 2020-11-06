---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 66c5e949cca8a6f53fdbac89e2745ac7697e14ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568065"
---
# <span data-ttu-id="57faf-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="57faf-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="57faf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57faf-102">SYNOPSIS</span></span>
<span data-ttu-id="57faf-103">Возвращает поставщика сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="57faf-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57faf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57faf-104">SYNTAX</span></span>

### <span data-ttu-id="57faf-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57faf-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57faf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="57faf-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57faf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57faf-107">DESCRIPTION</span></span>
<span data-ttu-id="57faf-108">Командлет **Get-AzureKeyVaultCertificateIssuer** получает определенного поставщика сертификата или всех поставщиков сертификатов для хранилища ключей в хранилище Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="57faf-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="57faf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57faf-109">EXAMPLES</span></span>

### <span data-ttu-id="57faf-110">Пример 1: получение имени поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="57faf-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="57faf-111">Эта команда получает издателя сертификата с именем TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="57faf-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="57faf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57faf-112">PARAMETERS</span></span>

### <span data-ttu-id="57faf-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="57faf-113">-Name</span></span>
<span data-ttu-id="57faf-114">Указывает имя получаемого издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="57faf-114">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57faf-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="57faf-115">-VaultName</span></span>
<span data-ttu-id="57faf-116">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="57faf-116">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57faf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57faf-117">-DefaultProfile</span></span>
<span data-ttu-id="57faf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57faf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57faf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57faf-119">CommonParameters</span></span>
<span data-ttu-id="57faf-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57faf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57faf-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57faf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57faf-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57faf-122">INPUTS</span></span>

## <span data-ttu-id="57faf-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57faf-123">OUTPUTS</span></span>

### <span data-ttu-id="57faf-124">List<Microsoft. Azure. Commands. KeyVault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="57faf-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="57faf-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="57faf-125">NOTES</span></span>

## <span data-ttu-id="57faf-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57faf-126">RELATED LINKS</span></span>

[<span data-ttu-id="57faf-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="57faf-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="57faf-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="57faf-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


