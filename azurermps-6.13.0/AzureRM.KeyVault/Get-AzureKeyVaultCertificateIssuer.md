---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733852"
---
# <span data-ttu-id="70202-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="70202-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="70202-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70202-102">SYNOPSIS</span></span>
<span data-ttu-id="70202-103">Возвращает поставщика сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="70202-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70202-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70202-104">SYNTAX</span></span>

### <span data-ttu-id="70202-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70202-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70202-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="70202-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70202-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="70202-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70202-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70202-108">DESCRIPTION</span></span>
<span data-ttu-id="70202-109">Командлет **Get-AzureKeyVaultCertificateIssuer** получает определенного поставщика сертификата или всех поставщиков сертификатов для хранилища ключей в хранилище Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="70202-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="70202-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70202-110">EXAMPLES</span></span>

### <span data-ttu-id="70202-111">Пример 1: получение имени поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="70202-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="70202-112">Эта команда получает издателя сертификата с именем TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="70202-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="70202-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70202-113">PARAMETERS</span></span>

### <span data-ttu-id="70202-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70202-114">-DefaultProfile</span></span>
<span data-ttu-id="70202-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="70202-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70202-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70202-116">-InputObject</span></span>
<span data-ttu-id="70202-117">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="70202-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70202-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="70202-118">-Name</span></span>
<span data-ttu-id="70202-119">Указывает имя получаемого издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="70202-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70202-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70202-120">-ResourceId</span></span>
<span data-ttu-id="70202-121">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="70202-121">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70202-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="70202-122">-VaultName</span></span>
<span data-ttu-id="70202-123">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="70202-123">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70202-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70202-124">CommonParameters</span></span>
<span data-ttu-id="70202-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70202-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70202-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70202-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70202-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70202-127">INPUTS</span></span>

### <span data-ttu-id="70202-128">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="70202-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="70202-129">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="70202-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="70202-130">System. String</span><span class="sxs-lookup"><span data-stu-id="70202-130">System.String</span></span>

## <span data-ttu-id="70202-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70202-131">OUTPUTS</span></span>

### <span data-ttu-id="70202-132">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="70202-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="70202-133">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="70202-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="70202-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="70202-134">NOTES</span></span>

## <span data-ttu-id="70202-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70202-135">RELATED LINKS</span></span>

[<span data-ttu-id="70202-136">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="70202-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="70202-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="70202-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


