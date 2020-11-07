---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914142"
---
# <span data-ttu-id="a44ea-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a44ea-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a44ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a44ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a44ea-103">Возвращает поставщика сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a44ea-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a44ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a44ea-104">SYNTAX</span></span>

### <span data-ttu-id="a44ea-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a44ea-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a44ea-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a44ea-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a44ea-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a44ea-107">DESCRIPTION</span></span>
<span data-ttu-id="a44ea-108">Командлет **Get-AzureKeyVaultCertificateIssuer** получает определенного поставщика сертификата или всех поставщиков сертификатов для хранилища ключей в хранилище Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a44ea-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a44ea-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a44ea-109">EXAMPLES</span></span>

### <span data-ttu-id="a44ea-110">Пример 1: получение имени поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="a44ea-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="a44ea-111">Эта команда получает издателя сертификата с именем TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="a44ea-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="a44ea-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a44ea-112">PARAMETERS</span></span>

### <span data-ttu-id="a44ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44ea-113">-DefaultProfile</span></span>
<span data-ttu-id="a44ea-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a44ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a44ea-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a44ea-115">-Name</span></span>
<span data-ttu-id="a44ea-116">Указывает имя получаемого издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="a44ea-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="a44ea-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a44ea-117">-VaultName</span></span>
<span data-ttu-id="a44ea-118">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a44ea-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a44ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44ea-119">CommonParameters</span></span>
<span data-ttu-id="a44ea-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a44ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44ea-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a44ea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44ea-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a44ea-122">INPUTS</span></span>

## <span data-ttu-id="a44ea-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a44ea-123">OUTPUTS</span></span>

### <span data-ttu-id="a44ea-124">List<Microsoft. Azure. Commands. KeyVault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a44ea-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a44ea-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a44ea-125">NOTES</span></span>

## <span data-ttu-id="a44ea-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a44ea-126">RELATED LINKS</span></span>

[<span data-ttu-id="a44ea-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a44ea-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="a44ea-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a44ea-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


