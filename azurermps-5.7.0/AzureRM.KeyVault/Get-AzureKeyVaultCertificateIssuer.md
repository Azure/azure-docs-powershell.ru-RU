---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561764"
---
# <span data-ttu-id="07bf0-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="07bf0-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="07bf0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="07bf0-103">Возвращает поставщика сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="07bf0-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07bf0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07bf0-104">SYNTAX</span></span>

### <span data-ttu-id="07bf0-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07bf0-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07bf0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="07bf0-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07bf0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07bf0-107">DESCRIPTION</span></span>
<span data-ttu-id="07bf0-108">Командлет **Get-AzureKeyVaultCertificateIssuer** получает определенного поставщика сертификата или всех поставщиков сертификатов для хранилища ключей в хранилище Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="07bf0-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="07bf0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07bf0-109">EXAMPLES</span></span>

### <span data-ttu-id="07bf0-110">Пример 1: получение имени поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="07bf0-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="07bf0-111">Эта команда получает издателя сертификата с именем TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="07bf0-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="07bf0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07bf0-112">PARAMETERS</span></span>

### <span data-ttu-id="07bf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bf0-113">-DefaultProfile</span></span>
<span data-ttu-id="07bf0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="07bf0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07bf0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07bf0-115">-InputObject</span></span>
<span data-ttu-id="07bf0-116">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="07bf0-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07bf0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07bf0-117">-Name</span></span>
<span data-ttu-id="07bf0-118">Указывает имя получаемого издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="07bf0-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07bf0-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="07bf0-119">-VaultName</span></span>
<span data-ttu-id="07bf0-120">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="07bf0-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07bf0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bf0-121">CommonParameters</span></span>
<span data-ttu-id="07bf0-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07bf0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bf0-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bf0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bf0-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07bf0-124">INPUTS</span></span>

### <span data-ttu-id="07bf0-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="07bf0-125">None</span></span>
<span data-ttu-id="07bf0-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="07bf0-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07bf0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07bf0-127">OUTPUTS</span></span>

### <span data-ttu-id="07bf0-128">List<Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuerIdentityItem>, Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="07bf0-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="07bf0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="07bf0-129">NOTES</span></span>

## <span data-ttu-id="07bf0-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07bf0-130">RELATED LINKS</span></span>

[<span data-ttu-id="07bf0-131">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="07bf0-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="07bf0-132">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="07bf0-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


