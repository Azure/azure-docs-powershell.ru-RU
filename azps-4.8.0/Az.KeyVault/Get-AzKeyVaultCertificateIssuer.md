---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 1504d4f18c8ab3baee000c2cf8d873df1dd9a177
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236213"
---
# <span data-ttu-id="9e3d4-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9e3d4-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9e3d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3d4-103">Возвращает поставщика сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="9e3d4-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="9e3d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e3d4-104">SYNTAX</span></span>

### <span data-ttu-id="9e3d4-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e3d4-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9e3d4-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3d4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e3d4-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e3d4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e3d4-108">DESCRIPTION</span></span>
<span data-ttu-id="9e3d4-109">Командлет **Get-AzKeyVaultCertificateIssuer** получает определенного поставщика сертификата или всех поставщиков сертификатов для хранилища ключей в хранилище Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9e3d4-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="9e3d4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e3d4-110">EXAMPLES</span></span>

### <span data-ttu-id="9e3d4-111">Пример 1: получение имени поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="9e3d4-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="9e3d4-112">Эта команда получает издателя сертификата с именем TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="9e3d4-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="9e3d4-113">Пример 2: список поставщиков сертификатов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="9e3d4-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="9e3d4-114">Эта команда получает издателей сертификата, который начинается с "тест".</span><span class="sxs-lookup"><span data-stu-id="9e3d4-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="9e3d4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e3d4-115">PARAMETERS</span></span>

### <span data-ttu-id="9e3d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3d4-116">-DefaultProfile</span></span>
<span data-ttu-id="9e3d4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9e3d4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e3d4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e3d4-118">-InputObject</span></span>
<span data-ttu-id="9e3d4-119">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9e3d4-119">KeyVault object.</span></span>

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

### <span data-ttu-id="9e3d4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e3d4-120">-Name</span></span>
<span data-ttu-id="9e3d4-121">Указывает имя получаемого издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="9e3d4-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="9e3d4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e3d4-122">-ResourceId</span></span>
<span data-ttu-id="9e3d4-123">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9e3d4-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="9e3d4-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9e3d4-124">-VaultName</span></span>
<span data-ttu-id="9e3d4-125">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="9e3d4-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="9e3d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3d4-126">CommonParameters</span></span>
<span data-ttu-id="9e3d4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e3d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3d4-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e3d4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3d4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e3d4-129">INPUTS</span></span>

### <span data-ttu-id="9e3d4-130">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9e3d4-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9e3d4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9e3d4-131">System.String</span></span>

## <span data-ttu-id="9e3d4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e3d4-132">OUTPUTS</span></span>

### <span data-ttu-id="9e3d4-133">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9e3d4-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="9e3d4-134">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9e3d4-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9e3d4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e3d4-135">NOTES</span></span>

## <span data-ttu-id="9e3d4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e3d4-136">RELATED LINKS</span></span>

[<span data-ttu-id="9e3d4-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9e3d4-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="9e3d4-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9e3d4-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


